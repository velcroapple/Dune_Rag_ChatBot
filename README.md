# Dune RAG Chatbot

A Retrieval-Augmented Generation (RAG) system built over the *Dune* universe from https://dune.fandom.com/wiki/Dune_Wiki 

This project implements an end-to-end pipeline for domain-specific question answering by combining semantic search with language model generation.

---

## Overview

Instead of relying purely on an LLM’s internal knowledge, this system retrieves relevant context from a curated Dune corpus before generating answers.

This enables:

- grounded responses
- domain-aware answers
- reduced hallucination

---

## Architecture
User Query

Query Embedding

FAISS Vector Search

Relevant Context Retrieval

Prompt Augmentation

LLM Generation

Final Answer


---

## Project Structure

| File | Purpose |
|------|--------|
| `getallarticles.py` | Collects raw Dune text corpus |
| `extract.py` | Cleans and prepares text |
| `embed.py` | Generates vector embeddings |
| `main.py` | Query → Retrieve → Generate pipeline |
| `faiss_index.index` | Vector similarity index |
| `faiss_metadata.pkl` | Chunk metadata |
| `requirements.txt` | Dependencies |

---

## Pipeline

### 1. Corpus Creation
Articles from the Dune universe are collected and preprocessed.

### 2. Embedding
Text chunks are converted into semantic vector representations.

### 3. Storage
Embeddings are stored using **FAISS** for efficient similarity search.

### 4. Retrieval
User queries are matched against the vector store.

### 5. Generation
Relevant context is injected into the LLM prompt to produce grounded responses.

---
## Skills Demonstrated

### Retrieval-Augmented Generation (RAG)
Built an end-to-end pipeline combining semantic search with LLM-based generation for grounded responses.

### Vector Databases & Similarity Search
Implemented document retrieval using FAISS for efficient high-dimensional search.

### Embedding-Based NLP
Used Sentence Transformers to convert text into semantic vector space.

### LLM-Oriented System Design
Integrated retrieval context into prompts for improved answer quality.

### Data Ingestion & Processing
Collected and cleaned domain-specific corpus using BeautifulSoup and structured parsing.

### Text Chunking & Preprocessing
Applied splitting strategies using LangChain text splitters for optimal retrieval.

### API Integration
Managed external calls using requests / urllib pipelines.

### Environment & Config Management
Used python-dotenv for secure configuration handling.

### Interactive Deployment
Streamlit-based interface for real-time querying.

---

## How to Run

Install dependencies:

```bash
pip install -r requirements.txt
