# 📘 llm-course-assistant

A smart Q&A system that allows users to "chat" with their PowerPoint lectures. Instead of manually searching through dozens of slides, you can now ask questions in natural language and get instant, accurate answers with source citations.

This project builds a complete Retrieval-Augmented Generation (RAG) pipeline from scratch using LangChain, ChromaDB, and Sentence Transformers.

---

## 🛠️ Tech Stack

**Core:** Python, LangChain

**LLM:** OpenAI / Groq

**Vector Store:** ChromaDB

**Embeddings:** Sentence Transformers (all-MiniLM-L6-v2)

**Data Handling:** python-pptx (for text extraction), tiktoken

---

## 🧠 Workflow Overview

## Ingestion: 
Extracts all text from .ppt slides in the ppt -files directory.

## Chunking: 
Splits the raw text into smaller, overlapping chunks (500 characters, 120 overlap) for better semantic meaning.

## Embedding: 
Creates vector representations for each chunk using the all-MiniLM-L6-v2 model.

## Storage: 
Loads the embeddings and their text content into a ChromaDB vector database.

## RAG Pipeline: 
When a user asks a question, the system retrieves the most relevant chunks, passes them (and the question) to an LLM, and generates a final, context-aware answer.

---

## ▶️ How to Run

## **1. Clone the Repository**
git clone https://github.com/vishnuP2712/llm-course-assistant.git
cd llm-course-assistant

## **2. Install Dependencies**
pip install python-pptx langchain langchain-community chromadb sentence_transformers faiss-cpu transformers accelerate tiktoken

## **3.Add your API Key**
Open the notebook and find the section for the API key (e.g., OPENAI_API_KEY or GROQ_API_KEY).
Paste your own API key.

## **4.Add your Data**
Place your own .ppt or .pptx files into the ppt -files directory.

## **5.Run the Notebook**
Open IR_project_LLM (3).ipynb in VS Code, Google Colab, or Jupyter.
Run the cells in order from top to bottom.

