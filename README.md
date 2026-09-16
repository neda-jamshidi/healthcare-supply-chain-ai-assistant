# Healthcare Supply Chain AI Assistant

A privacy-conscious, locally deployed conversational AI system for healthcare
supply-chain decision support, combining a local Large Language Model,
Retrieval-Augmented Generation (RAG), hybrid SQL/vector retrieval, specialized
query components, operational analytics, and intelligent routing.

<p align="center">
  <img src="AI-assistant.png"
       alt="Healthcare Supply Chain AI Assistant"
       width="700">
</p>

<p align="center">
  <em>
    Conceptual interface illustration created for portfolio purposes.
    No real operational data, production interface, or organization-specific information is shown.
  </em>
</p>

---

## Overview

Healthcare supply-chain operations involve heterogeneous information related
to products, suppliers, orders, availability, operational status, and
procurement activities.

Accessing this information efficiently can require users to navigate multiple
data sources, manually inspect records, and perform different types of
structured and analytical queries.

This project addresses this problem through a conversational AI assistant that
provides natural-language access to healthcare supply-chain information and
decision-support functionality.

The system combines structured data processing, a SQLite backend, semantic
retrieval, Retrieval-Augmented Generation (RAG), specialized query and
analysis components, intelligent routing, and a locally deployed Large
Language Model within a Streamlit application.

The project was developed in the context of a professional research internship
in the public healthcare sector.

---

## Key Features

- Natural-language interaction with healthcare supply-chain information
- Fully local LLM inference
- Specialized query and analysis components
- Intelligent query routing
- Structured SQL-based retrieval
- Embedding-based semantic retrieval
- Retrieval-Augmented Generation (RAG)
- Hybrid SQL + vector retrieval
- Supplier and order analysis
- Operational analytics
- Decision-support and prioritization
- Interactive Streamlit interface
- Privacy-conscious local architecture

---

## System Architecture

The system combines deterministic structured retrieval with semantic retrieval
and local LLM inference.

```text
                 Healthcare Operational Data
                            │
                            ▼
                 Processing & Integration
                            │
                ┌───────────┴───────────┐
                │                       │
                ▼                       ▼
             SQLite                 Embeddings
                │                       │
                ▼                       ▼
       Structured Retrieval          ChromaDB
                │                       │
                │                       ▼
                │              Semantic Retrieval
                │                       │
                └───────────┬───────────┘
                            │
                            ▼
                       Query Router
                            │
                            ▼
              Specialized Query & Analysis
                       Components
                            │
                            ▼
                  Retrieved Context
                            │
                            ▼
               Qwen2.5-Coder-3B-Instruct
                            │
                       LM Studio
                            │
                            ▼
                Conversational Assistant
                            │
                            ▼
              Healthcare Decision Support
