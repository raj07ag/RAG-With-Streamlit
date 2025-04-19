# Retrieval-Augmented Generation (RAG) Powered Q&A Application
## Overview
This project demonstrates a full-fledged Retrieval-Augmented Generation (RAG) based Question Answering (Q&A) application that leverages large language models (LLMs) with external knowledge sources. It enables users to upload text, PDFs, DOCX files, or provide website links, and ask context-aware questions. The app efficiently processes inputs, generates embeddings, stores them in a vector database, and retrieves the most relevant chunks to generate high-quality, accurate answers using LLMs.

## Tools & Frameworks Used
### LangChain – Framework to manage the RAG pipeline.

### groq – For LLMs inferencing(e.g., meta-llama/llama-3.1-8b-instant).

### Chroma – used for vector storage and retrieval.

### Streamlit – For building the interactive web UI.

### Google Colab – For development environment.

### PyPDF / python-docx / TextLoader / WebBaseLoader – To load and extract content from various formats.

## Project Workflow
### 1. User Input Interface (Streamlit)

Accepts input via Text, PDF, DOCX, or Web Links.

Dynamically renders input boxes or upload fields based on selection.

### 2. Document Loading and Preprocessing

Loads content using appropriate loaders (PDFReader, TextLoader, WebBaseLoader).

Uses RecursiveCharacterTextSplitter to break large documents into smaller, overlapping chunks.

### 3. Embeddings & Vector Storage

Converts chunks into vector embeddings using Sentence Transformers.

Stores embeddings in Chroma for efficient similarity search.

### 4. Retrieval & Generation

Queries are processed through LangChain’s chain.

Retrieves top relevant chunks from vectorstore.

Uses groq-API for inferencing (e.g., llama-3.1-8b-instant) for generating precise, factual answers.

### 5. Output Rendering

Displays answers directly on the Streamlit interface.


## Key Features & Benefits
Handles various input types (PDF, DOCX, links, or raw text).

Uses open-source and cost-effective alternatives to OpenAI.

Embeds external knowledge seamlessly with language models.

Scalable, modular, and easily extendable RAG architecture.


*The application was tested with resumes, research papers, company reports, web limks and general summaries — showcasing its versatility across domains.*
