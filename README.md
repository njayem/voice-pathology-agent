# Voice Pathology Agent

A multi-agent clinical AI pipeline for Parkinson's disease detection from speech. Audio input is processed through an acoustic feature extractor and classifier, then passed through a modular LLM explanation chain with RAG over clinical research papers. Benchmarks GPT-4o, Claude, and Gemini on clinical output quality.

## Pipeline

audio input → Whisper STT → acoustic features → PD classifier → Agent 1: Structurer → Agent 2: Explainer (GPT / Claude / Gemini) → Agent 3: RAG retrieval → ElevenLabs TTS → voice output

## Stack

- **Agents:** LangGraph, OpenAI Agents SDK
- **RAG:** LangChain, ChromaDB, OpenAI embeddings
- **Speech:** Whisper STT, ElevenLabs TTS
- **LLMs:** GPT-4o, Claude 3.5, Gemini 1.5 Pro
- **Observability:** LangSmith
- **UI:** Gradio

## Setup

1. Clone the repo
2. Create a `.env` file and add your API keys (see `.env.example`)
3. Install dependencies: `pip install -r requirements.txt`
4. Run: `python app.py`

## Status

🚧 In progress