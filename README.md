# Domain Aware AI-Document-Chatbot
--- 
## Summary 
Developed an AI-powered document intelligence platform: upload reports, chat with them using voice/text, and get domain-expert answers grounded in your data. Includes RAG retrieval, vector embeddings, FastAPI backend, Docker deployment, and analytics-driven improvement.
Upload documents → Ask domain questions → Chat with voice → Get grounded, citation-backed answers.
Built with LangChain · OpenAI Embeddings · FastAPI · Streamlit · Docker · GitHub Actions · Evidently AI / PromptLayer.

---

## 🚀 Overview
This project is an AI-powered knowledge assistant that lets you:
- Upload PDFs, reports, notes, or datasets
- Automatically index them using LangChain + OpenAI embeddings
- Chat conversationally about your documents
- Ask domain-specific questions (Finance, Product Technical Support, Research, ML)
- Speak your questions → voice recognition → chatbot responds
- See which document chunks were used (citations)
- Continuously improve retrieval quality via query logs + analytics
The entire application is packaged with FastAPI backend, Streamlit frontend, Dockerized services, and CI/CD deployment pipeline powered by GitHub Actions.

--- 

## 🧬 How It Works End-to-End
1️⃣ Upload Documents
1. Text extracted
2. Cleaned + chunked
3. Embedded + stored

2️⃣ Ask Questions (Text or Voice)
1. Converts to embedding
2. Retrieves top-k chunks
3. LLM generates grounded answer
4. Shows citations + sources

3️⃣ Everything is Logged
1. Query logs stored
2. Drift analysis with Evidently AI
3. Helps refine the pipeline

--- 

## Features 
🔍 1. Smart Document Ingestion Pipeline
- Upload PDFs, Word files, or text.
- Automatic preprocessing:
  - Text extraction
  - Cleaning & normalization
  - Chunking with LangChain
- Embed using OpenAI embeddings.
- Store embeddings in a local or hosted Vector Database (Chroma/Pinecone).

🧠 2. RAG-Based Conversational Chatbot
- Retrieval-Augmented Generation pipeline using LangChain.
- Answers grounded strictly in your documents.
- Domain-aware reasoning:
  - AI behaves like an expert in the domain you choose
(e.g., Finance Analyst, Cybersecurity Specialist, Medical Researcher, etc.)
- Provides citations:
  - For example “This answer comes from page 14 of report_A.pdf”

🎤 3. Voice Recognition Chat Interface
- Ask questions via microphone.
- Speech → text conversion (Whisper / browser API).
- Chatbot responds with text (optional TTS add-on).
- Useful for accessibility, hands-free mode, or research browsing.

🖥️ 4. Full Web App Using FastAPI + Streamlit

- FastAPI backend: chat, embeddings, ingestion, logging.
- Streamlit frontend: document upload, chat, voice input, citations.
- Real-time updates.
- Easy local or cloud deployment.

🔄 5. CI/CD Pipeline (GitHub Actions)
- Auto-building Docker images.
- Auto-linting + tests.
- Auto-deploy to:
  - Render
  - Railway
  - Azure Container Apps

📊 6. Query Logging + Retrieval Analytics
- Integrated with:
  - PromptLayer (prompt + usage tracking) OR
  - Evidently AI (retrieval drift detection, data quality monitoring)
- This enables:
  - Tracking most common questions
  - Identifying poor retrieval queries
  - Improving chunking, prompt engineering, or embedding settings over time
 
---

## 🏆 What Makes This Project Unique
Most RAG chatbots stop at “upload and ask.”
This project adds:
1. Domain expertise persona
→ Ask: “Explain this annual report like a financial auditor.”
2. Voice-enabled search
→ Converse with your documents naturally.
3. Retrieval quality analytics
→ The chatbot improves over time.
4. Production infrastructure
→ Docker + FastAPI + CI/CD, not just notebooks.
This makes it impressive for interviews, portfolio, and real-world use.

--- 

## 🧪 Tech Stack
1. Document Processing --> LangChain
2. Embeddings	--> OpenAI
3. Backend --> FastAPI
4. Frontend --> Streamlit
5. Voice Recognition --> Whisper / WebRTC
6. Storage --> ChromaDB / Pinecone
7. Deployment --> Docker + GitHub Actions
8. Logging --> PromptLayer / Evidently AI

--- 

## 📈 Future Enhancements
1. Add memory-based conversation history
2. Semantic filtering by document type
3. Themed UI for domain personas
4. Deploy vector DB to Pinecone for scalability
5. Add full TTS for spoken answers
6. Add multi-agent analysis (summaries, comparisons, contradictions detector)
