Retrieval-Augmented Generation (RAG) System
Using a Fictional Football Team Knowledge Base

Michael Tamirat

Overview:

I have created a project that implements a Retrieval-Augmented Generation (RAG) system using a small, custom knowledge base about a fictional football team: The Redwood City Ravens.
The goal is to demonstrate:
How to construct a knowledge base
How to embed and index text
How to retrieve relevant chunks
How to generate grounded answers using a Large Language Model
How retrieval reduces hallucination compared to a raw LLM
All work was executed in a Python notebook included in this repository.

Models Used:
Embedding Model
Model: sentence-transformers/all-MiniLM-L6-v2
Framework: Hugging Face Transformers
Backend: PyTorch (no TensorFlow/Keras)
LLM Used for Generation:
Model: google/flan-t5-small
A lightweight instruction-tuned model suitable for RAG experiments.

Retrieval Process
The KB is split into 3 chunks, each corresponding to a paragraph.
We retrieve the top-2 chunks using cosine similarity between the query embedding and the KB embeddings.

Analysis of the results:
Yes in every case, retrieval grounded the model’s output.
