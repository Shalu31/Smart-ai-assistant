# Smart-ai-assistant
 A GenAI-powered assistant that reads PDF/TXT documents, summarizes content, answers free-form questions, and poses logic-based challenges — all with contextual justification — built with Streamlit and LangChain.
 
 ## Features
📄 Upload PDF/TXT documents

🧠 Ask Anything: context-aware Q&A from document

🎯 Challenge Me: system-generated questions + evaluation

📝 Auto-summary in ≤150 words

🔍 Justified answers with reference to document sections

🌐 Web app built with Streamlit
## 🧠 How It Works
The application processes your queries through the following steps:

PDF Loading
Reads and extracts text from one or more uploaded PDF/TXT documents.

Text Chunking
Splits the extracted text into manageable chunks to ensure better processing and context handling.

Embedding Generation
Uses a language model to convert text chunks into numerical embeddings that capture their semantic meaning.

Similarity Matching
When a user asks a question, the app compares the query embedding with the document chunks to find the most relevant ones.

Response Generation
The most similar chunks are fed into the language model to generate an accurate, context-aware answer backed by the original document.
## Architecture
[User Uploads Document] 
        ↓
[Text Extracted via PyPDF2]
        ↓
[Split & Embed → FAISS Vector Store] ← Uses HuggingFace / OpenAI Embeddings
        ↓
[Two Modes] → "Ask Anything" | "Challenge Me"
        ↓
[LangChain QA Chain / Question Generator] → Evaluates & Responds
        ↓
[Justification Engine] → Highlights or references context
## Installation
cd smart-assistant-research-summarizer
pip install -r requirements.txt
streamlit run main.py
## Sample.env
HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_key
OPENAI_API_KEY=your_openai_key
## Folder Structure
.
├── main.py
├── htmlTemplate.py
├── requirements.txt
├── .env.example
└── README.md
## Author
Shalu Verma


