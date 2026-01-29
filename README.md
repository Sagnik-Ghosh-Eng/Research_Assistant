# 📄 Research Paper Assistant

A paper-centric research assistant that ingests a single academic paper and enables strictly grounded, citation-based question answering.

---

## 📌 Project Overview

The Research Paper Assistant allows a user to enter the title of a research paper and receive a fixed, structured understanding of the paper, 
followed by an interactive question-answering interface.

Unlike general AI chatbots, this system never hallucinates:
- All answers are derived only from the given paper
- If information is not present, the system explicitly responds:

> “Not found in this paper.”

This makes the assistant suitable for academic research, paper review, and study assistance.

---

## 🎯 Objectives

- Enable structured understanding of a research paper
- Provide citation-based and paper-grounded answers
- Prevent hallucinations using single-paper grounding
- Maintain full chat history for transparency

---

## 🧠 Key Features

### 1️⃣ Paper-Title-Based Ingestion
- User enters the title of a research paper
- The system fetches and processes the paper (PDF / text)
- A vector index is created only for that paper

---

### 2️⃣ Fixed Initial Outputs (Mandatory)

After ingestion, the system always generates:

1. Authors
2. Paper topic
3. One-line description of the topic
4. Concise paper summary
5. Related papers

These outputs provide immediate structured understanding.

---

### 3️⃣ Paper-Grounded Follow-Up Q&A

- Users can ask follow-up questions related to the paper
- Answers are generated solely from the ingested paper
- Each answer includes citations or quoted sections
- If the answer is absent:  Not found in this paper.
  This guarantees academic integrity.


---

### 4️⃣ Chat History Preservation

- All user queries and responses are stored
- Full chat history is displayed at all times
- Ensures transparency and traceability

---

## 🔒 Design Constraints (Non-Negotiable)

- ❌ No external knowledge beyond the paper
- ❌ No speculative answers
- ❌ No multi-paper mixing
- ✅ Explicit “Not found in this paper” responses
- ✅ Single-paper context per session

---

## 🏗️ System Architecture & Workflow

User enters paper title │ ▼ Paper Fetching & Parsing │ 
▼ Text Chunking │ ▼ Embedding Generation │ ▼ Single-Paper Vector Store │ 
▼ Fixed Initial Outputs │ ▼ User Follow-Up Questions 
│ ▼ Paper-Only Retrieval │ ▼ Answer + Citation OR "Not found in this paper"

---

## 🧪 Example Interaction

User:  
What dataset is used in this paper?

Assistant:  
The paper uses the XYZ dataset for evaluation (Section 4.2).

OR

Not found in this paper.

---

## 🛠️ Technologies Used

- LLM API for generation
- Embedding model for semantic search
- Vector database for retrieval
- PDF/Text processing pipeline
- Python-based backend

---

## 👥 Team Structure

This project was developed by a team of five members.
  * Sagnik Ghosh(Team Leader)
  * Aditi Sen
  * Kaushal Kishore
  * Pritam Maity
  * Sneha Roy



---

## 🚀 Future Enhancements

- Support K paper fetching related to a general question and implementation of RAG on all K papers
- Multi-paper comparison
- Section-wise exploration
- PDF citation highlighting
- Support for multiple academic sources


---

## ✅ Conclusion

The Research Paper Assistant demonstrates responsible use of LLMs in academia by enforcing strict grounding, 
transparency, and citation-based reasoning. The system prioritizes reliability over creativity, making it suitable for research and educational use.
