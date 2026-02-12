# Hybrid RAG: Vector and Graph-Based Retrieval

This repository contains two Jupyter notebooks demonstrating different approaches to Retrieval-Augmented Generation (RAG) systems.

## 📚 Notebooks Overview

### 1. Basic RAG Example (`RAG_basic_example.ipynb`)
A foundational implementation of a RAG system using vector embeddings and similarity search.

**Key Features:**
- Text document processing and chunking
- Vector embeddings using sentence transformers
- FAISS vector database for efficient similarity search
- Integration with Llama 3.2 1B Instruct model for answer generation
- Example queries on "The Little Prince" text

**Technologies Used:**
- `sentence-transformers` (all-MiniLM-L6-v2)
- `faiss-cpu` for vector indexing
- `transformers` with Llama 3.2 1B Instruct
- PyTorch

### 2. Graph RAG with Vector Search (`Graph_RAG_vector.ipynb`)
An advanced RAG implementation combining knowledge graphs with vector embeddings for more sophisticated query answering.

**Key Features:**
- Neo4j graph database integration
- Hybrid retrieval: Graph queries + Vector similarity search
- Cypher query generation using LLMs
- Research publication dataset with researchers, articles, and topics
- Complex relationship queries (collaborations, co-authorship, topic analysis)

**Technologies Used:**
- Neo4j graph database
- LangChain for RAG orchestration
- `GraphCypherQAChain` for natural language to Cypher translation
- Llama 3.2 3B Instruct for query understanding
- HuggingFace embeddings

## 🚀 Getting Started

### Prerequisites

```bash
# Install required packages
pip install langchain
pip install langchain-community
pip install neo4j
pip install sentence-transformers
pip install faiss-cpu
pip install transformers
pip install torch
pip install accelerate
```

### For Basic RAG:
1. Prepare your text document
2. Run the notebook cells sequentially
3. Modify the query text to ask different questions

### For Graph RAG:
1. Set up a Neo4j instance (local or cloud)
2. Configure connection credentials in the notebook
3. Load the sample research dataset
4. Run queries combining graph traversal and semantic search

## 💡 Use Cases

### Basic RAG
- Document Q&A systems
- Knowledge base search
- Content retrieval from large text corpora
- Educational applications

### Graph RAG
- Research paper analysis
- Collaboration network discovery
- Multi-hop reasoning queries
- Complex relationship mapping
- Academic citation networks

## 📊 Sample Queries

### Basic RAG Example
```
"What are the two pictures the narrator knows how to draw?"
"Who is the little prince?"
```

### Graph RAG Example
```
"Which researcher has collaborated with the most peers?"
"How many articles has Emily Chen published?"
"Are there any pair of researchers who have published more than three articles together?"
"Which topics does Sarah Lee focus on?"
```

## 🔧 Configuration

### Basic RAG Configuration
- **Chunk Size**: Configurable text splitting
- **Embedding Model**: all-MiniLM-L6-v2 (384 dimensions)
- **LLM**: Llama 3.2 1B Instruct
- **Top K Results**: Adjustable number of retrieved chunks

### Graph RAG Configuration
- **Neo4j Connection**: URI, username, password required
- **Embedding Model**: HuggingFace embeddings
- **LLM**: Llama 3.2 3B Instruct
- **Cypher Generation**: Automated with error handling

## 📝 Notes

- Both notebooks are designed to run in Google Colab
- GPU acceleration recommended for faster inference
- The Graph RAG example includes a synthetic research dataset
- Modify prompts and parameters to suit your specific use case

## 🤝 Contributing

Feel free to extend these examples with:
- Different embedding models
- Alternative LLMs
- Custom datasets
- Enhanced retrieval strategies
- Evaluation metrics

## 📄 License

These notebooks are provided for educational and research purposes.

## 🔗 Resources

- [LangChain Documentation](https://python.langchain.com/)
- [Neo4j Graph Database](https://neo4j.com/)
- [Sentence Transformers](https://www.sbert.net/)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/)
- [FAISS Vector Search](https://faiss.ai/)

---

## Author: 

**Mohammed Bari**  

---

⭐ Star this repo if you find it helpful.
