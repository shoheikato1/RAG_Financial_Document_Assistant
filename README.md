# Financial Analyst RAG Assistant

This project demonstrates a prototype Retrieval-Augmented Generation (RAG) system designed to assist financial analysts in extracting competitive insights from 10-K reports across multiple insurance carriers.

## What It Does
- Parses and embeds multiple 10-K PDFs
- Retrieves relevant chunks of information using FAISS
- Generates company-specific financial analysis using GPT-4
- Presents traceable insights with source citations (company + page)

## Target Use Case
This system is tailored for financial analysts in the insurance industry who:
- Conduct comparative competitive research
- Need structured insights across multiple filings
- Seek faster synthesis of key financial indicators and risks

## Key Features

- **Smart Retrieval**: Organized by company, chunked for accuracy
- **Traceable Output**: Source citations with page numbers
- **Conversational Interface**: Iterative querying and memory support
- **Multi-company Comparison**: Handles multiple carriers in a single prompt

## Project Structure

├── code/ │ └── RAG_Financial_Analyzer.ipynb ├── documentation/ │ ├── Product_Requirements_Doc.pdf │ ├── Architecture_Diagram.pdf │ └── Screenshots.pdf

## Tech Stack

- **LLM API**: OpenAI GPT-4
- **Embedding**: `sentence-transformers` (MiniLM)
- **Vector DB**: FAISS (L2 distance)
- **PDF Parsing**: PyPDF2 (can swap with PDFPlumber)
- **Interface**: Jupyter Notebook (for PoC simplicity)

## Tradeoffs and Design Decisions

- Unified GPT-4 API usage for consistency (vs. multi-model architecture)
- Local FAISS DB for simplicity (vs. Pinecone/Weaviate)
- In-memory context (vs. persistent context DB)
- Hybrid chunking (narrative + table-aware) for financial integrity

## Running the Notebook

1. Install dependencies:
```bash pip install -r requirements.txt```
2. Run the notebook and follow the instructions to upload 10k PDFs
3. Ask your analytical question and review the generated response with sources

## Disclaimer
This is a personal project to showcase product design and technical implementation of a RAG system for financial analysis. All data used are publicly available and no proprietary or confidential information is included.
