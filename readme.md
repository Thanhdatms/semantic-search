# Semantic Search Engine for E-commerce

## Description
The semantic search engine can serve customers' demands for searching products based on descriptions, memories, or any patterns in the products.

### First Version
- Used the **All-MiniLM-L6-v2** model to convert descriptions, colors, brand names, and product names into vectors.
- Stored the vectors in a vector database, **Pinecone**.

### Second Version
- Used the **CLIP** model, employing **BM25** to encode text information into vectors.
- Used the **CLIP ViT-B-32** model to encode images into vectors.
- Stored these vectors in **Pinecone**.

### Functionality
When customers send a prompt to the server, their prompt is converted into a vector. Using a metric (cosine similarity in version 1, dot product in version 2), the system calculates the similarity between the customers' needs and the product patterns.

## Technologies
- **Models**: CLIP-model, BM25 model, CLIP ViT-B-32, All-MiniLM-L6-v2
- **Database**: Vector database Pinecone

## Prerequisites
- Python 3.12
- pip (Python package installer)
- GPU (Optional, recommended for faster processing)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/tienvtt/big-data-project.git