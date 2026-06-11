# MedGraphRAG 🧬

Biomedical Question Answering using Knowledge Graphs and GraphRAG

## Overview

This project builds a GraphRAG (Graph Retrieval-Augmented Generation) pipeline for biomedical question answering, combining Knowledge Graphs with LLM-based retrieval to improve reasoning over structured medical data.

Motivated by the limitations of keyword-based retrieval (explored in a prior BM25-based biomedical search engine project), this system leverages semantic relationships between biomedical entities to enhance answer quality.

## Architecture

```
PubMedQA Dataset → Entity Extraction (spaCy) → Knowledge Graph (Neo4j)
                                                        ↓
User Query → RAG Pipeline (LlamaIndex + ChromaDB) → GraphRAG → Answer
```

## Features

- **Dataset**: 1,000 labeled PubMedQA question-answer pairs
- **Entity Extraction**: Biomedical NER using spaCy
- **Knowledge Graph**: Neo4j graph database with entity relationships
- **RAG Pipeline**: ChromaDB vector store + LlamaIndex
- **Evaluation**: Vanilla RAG vs GraphRAG comparison

## Project Structure

## Status

- [x] Data loading and exploration
- [x] Entity extraction pipeline
- [x] Knowledge Graph construction (Neo4j)
- [x] RAG pipeline (LlamaIndex + ChromaDB)
- [x] GraphRAG integration
- [x] Evaluation and comparison

## Tech Stack

Python • spaCy • LlamaIndex • ChromaDB • Neo4j • HuggingFace • PyTorch

## Dataset

[PubMedQA](https://huggingface.co/datasets/qiaojin/PubMedQA) — 1,000 labeled biomedical question-answer pairs from PubMed abstracts.
