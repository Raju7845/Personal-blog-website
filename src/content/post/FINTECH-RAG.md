---
layout: ../../layouts/post.astro
title: Understanding Retrieval-Augmented Generation (RAG)
description: A simple explanation of how RAG helps LLMs use external knowledge.
dateFormatted: Mar 05, 2026
---

Large Language Models are powerful, but they often struggle with **outdated knowledge or hallucinations**.  
This is where **Retrieval-Augmented Generation (RAG)** becomes useful.

RAG is a technique that allows an LLM to retrieve relevant information from external sources before generating an answer. Instead of relying only on the model’s training data, the system searches a knowledge base and feeds the relevant context to the model.

A typical RAG pipeline looks like this:

1. **Data Ingestion** – Documents such as PDFs, websites, or CSV files are collected and processed.
2. **Text Chunking** – Large documents are split into smaller chunks.
3. **Embeddings** – Each chunk is converted into vector embeddings.
4. **Vector Database** – The embeddings are stored in a vector database for fast similarity search.
5. **Retrieval** – When a user asks a question, the system retrieves the most relevant chunks.
6. **Generation** – The LLM uses this context to generate a more accurate answer.

Some popular tools used in RAG systems include:

- [LangChain](https://www.langchain.com/)
- [LlamaIndex](https://www.llamaindex.ai/)
- [ChromaDB](https://www.trychroma.com/)
- [FAISS](https://github.com/facebookresearch/faiss)

I recently experimented with RAG while building a project called **FinRAG**, which allows users to query Indian mutual fund datasets using natural language.

You can explore the project here:

<https://github.com/Raju7845/FINTECH-RAG>