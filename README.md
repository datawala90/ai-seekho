# AI Seekho Notebooks

This repository contains a few example notebooks demonstrating basic Amazon Bedrock usage and a simple local RAG (Retrieval Augmented Generation) workflow.

## Notebooks

### 1. `1-br-call.ipynb`
Checks your AWS region and caller identity, then lists available Bedrock foundation models using `boto3`.

### 2. `2-easy-rag.ipynb`
Shows a lightweight RAG pipeline built with local embeddings (Sentence Transformers), FAISS for vector search and a small open model (`flan-t5-small`) for generation. No AWS services are involved.

### 3. `3-br-rag.ipynb`
Implements a RAG workflow using Amazon Bedrock for both embedding and text generation. Requires access to the Titan models in Bedrock.

## Prerequisites
- Python 3.10+ with the following packages:
  - `boto3`
  - `sentence-transformers`
  - `faiss-cpu`
  - `langchain`
  - `transformers`
  - `accelerate`
  - `pytest` (optional for running tests)
- AWS credentials configured locally with permission to call STS and Amazon Bedrock (for notebooks 1 and 3).
- A Jupyter environment (e.g., `jupyter notebook`) or any tool capable of executing `.ipynb` files.

## Running the notebooks
1. Install the required Python packages:
   ```bash
   pip install boto3 sentence-transformers faiss-cpu langchain transformers accelerate
   ```
2. Ensure your AWS credentials are available (via environment variables or configured profile).
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open the desired notebook and run the cells in order.

Notebook `2-easy-rag.ipynb` can be run entirely offline, while `1-br-call.ipynb` and `3-br-rag.ipynb` need network access to AWS services and valid credentials.

