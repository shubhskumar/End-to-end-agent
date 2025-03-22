# End-to-End RAG Agent using LangChain, LangGraph, and Cassandra

This project demonstrates the construction of an end-to-end **Retrieval-Augmented Generation (RAG)** agent using **LangChain** and **LangGraph**, with vector storage powered by **Cassandra** (via **CassIO**).

---

## Key Features

- **LangChain + LangGraph Integration**  
  Orchestrates complex multi-step reasoning using graph-based workflows.

- **Cassandra Vector Store**  
  Efficiently indexes and retrieves documents using HuggingFace embeddings.

- **Web Data Loader**  
  Ingests real-time content from the web using `WebBaseLoader`.

- **Custom Routing & Retrieval**  
  Implements dynamic question routing and document retrieval pipelines.

- **Typed State Management**  
  Manages intermediate states using strongly-typed classes (`TypedDict`, `BaseModel`).

---

## How it Works

1. **Data Loading**  
   Loads content from web sources and splits it using recursive character text splitting.

2. **Vectorization**  
   Embeds the documents using HuggingFace models.

3. **Indexing**  
   Stores the embedded documents in a Cassandra vector store.

4. **Query Routing**  
   Classifies questions to determine whether to invoke retrieval or use a direct answer.

5. **Graph Execution**  
   Uses LangGraph to orchestrate different agent paths based on user intent.
