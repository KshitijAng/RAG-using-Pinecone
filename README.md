# RAG Pipeline with LangChain 🦜, OpenAI, and Pinecone

![RAG Logo](assets/raglogo.png)
![RAG Pipeline](assets/ragpipeline.png)

## Project Overview
This project implements a Retrieval-Augmented Generation (RAG) pipeline using **LangChain**, **OpenAI**, and **Pinecone**.  
The pipeline enhances the accuracy and relevance of responses by combining powerful language models with a vector database.

**Note:** Requires an OpenAI API Key for embeddings and model itself.

## Key Features
- **LangChain**: Framework to orchestrate prompts, embeddings, and retrieval.
- **OpenAI GPT-3.5-turbo-instruct**: Provides high-quality, instruction-tuned responses with controlled creativity (`temperature=0.5`).
- **Pinecone**: Vector database that efficiently stores and retrieves embeddings for semantic search.

## Workflow
1. **Text Ingestion**  
   - Input documents are chunked into smaller sections.  
   - Each chunk is embedded using `OpenAIEmbeddings`.

2. **Vector Storage**  
   - Embeddings are stored in **Pinecone** with metadata for fast similarity search.  

3. **Query & Retrieval**  
   - A user query is embedded.  
   - Pinecone retrieves the most relevant chunks using cosine similarity.  

4. **Answer Generation**  
   - Retrieved context is passed to the **OpenAI model**.  
   - The model generates a response augmented with retrieved knowledge.  

## Benefits of Using Pinecone
- **Scalability**: Handles millions of vectors with low latency.  
- **High availability**: Fully managed and production-ready.  
- **Optimized retrieval**: Returns the most relevant chunks quickly for real-time applications.  

## Tech Stack
- **Python**  
- **LangChain**  
- **OpenAI GPT-3.5-turbo-instruct**  
- **Pinecone**  
