# 🩺 MedQuAD Medical Q&A Chatbot

A **domain-specific chatbot** for answering medical and health-related questions using the **NIH MedQuAD dataset**. The chatbot combines **semantic search** and a **contextual question-answering model** to provide accurate, refined answers.

---

## 🌟 Features

* **Domain-specific Q&A**: Focused on medical questions.
* **Semantic Search**: Retrieves the most relevant Q&A entries using **sentence embeddings** and **FAISS similarity search**.
* **Contextual Answer Refinement**: Enhances the retrieved answer using a **RoBERTa-based QA model**.
* **Interactive Interface**: Built with **Gradio**, providing a user-friendly chat interface.
* **Lightweight & Efficient**: Uses `all-MiniLM-L6-v2` for embeddings and `deepset/roberta-base-squad2` for QA.

---

## 🛠️ Tech Stack

* **Python**
* **Pandas & NumPy** – data manipulation
* **Sentence-Transformers** – semantic embeddings
* **FAISS** – similarity search
* **Transformers (Hugging Face)** – question-answering pipeline
* **Gradio** – web-based interactive interface

---

## 📂 Dataset

* **NIH MedQuAD**: A curated dataset of medical question-answer pairs.
* Required columns: `Question`, `Answer`

---

## ⚡ How It Works

1. Load and preprocess the **MedQuAD dataset**.
2. Encode all questions into **sentence embeddings**.
3. Build a **FAISS index** for fast semantic similarity search.
4. For a user query:

   * Find the most similar question(s) from the dataset.
   * Refine the retrieved answer using a **RoBERTa QA model**.
5. Return the **original answer**, **refined answer**, and **source**.

---

## 💬 Example

**Query:** "What are the early signs of diabetes?"
**Answer:** "Refined answer based on MedQuAD dataset context."
**Source:** "NIH MedQuAD"

---
