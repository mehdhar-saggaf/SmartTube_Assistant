# SmartTube Assistant 🎧

![_project_work_ drawio](https://github.com/user-attachments/assets/43192a06-d2bf-4987-b59c-d1cfb5dfb6d2)
---
## A SmartTube Assistant that lets you:
- ▶️ Process any YouTube video
- 📄 Generate regular or tutorial-style summaries
- 💬 Chat with the video content (like ChatGPT)
- 🔄 Export summaries as PDF in multiple languages (Arabic supported)
- 🌙 Toggle between Dark and Light mode
- 📊 Trace interactions using LangSmith
---

## workfloow 
- Extracts audio using `yt-dlp`
- Transcribes video using OpenAI Whisper
- Summarizes using `LangChain + OpenAI`
- Chats via context-aware Q&A with timestamps
- PDF export via `WeasyPrint` with RTL language support
- Full LangSmith tracing integration for summaries and chatbot

---

## 🚧 Requirements

### Python
- Python 3.8+

### Install dependencies
```bash
pip install -r requirements.txt
```

**If you're on Windows and using WeasyPrint:**
```bash
pip install cairocffi
```

---

## 🔢 Environment Setup
Create a `.env` file and include:
```env
OPENAI_API_KEY=your_openai_key
LANGCHAIN_API_KEY=your_langsmith_key
LANGCHAIN_PROJECT=YouTube AI Assistant
LANGCHAIN_TRACING_V2=true
FLASK_SECRET=your_flask_secret
```

---

## 🌐 Run the App
```bash
python app.py
```
Then open in your browser:
```
http://127.0.0.1:5000
```

---

## 📊 Folder Structure & File Descriptions
```
smarttube_assistant/
├── app.py                  # Main Flask app with all routes and server logic
├── requirements.txt        # Required Python packages
├── .env                    # Environment config for API keys and secrets
├── templates/              # HTML templates rendered via Flask
│   ├── base.html           # Base layout with nav, dark mode, and CSS
│   ├── home.html           # Homepage for YouTube URL input and language select
│   ├── choice.html         # Option selection: summary or chatbot
│   ├── summary.html        # Displays and downloads the video summary
│   └── chatbot.html        # Chat UI to ask questions about the video
├── static/                 # Static files like fonts or custom CSS
│   └── fonts/              # Optional Arabic font folder (not needed with WeasyPrint)
├── utils/                  # Utility modules for different tasks
│   ├── youtube_utils.py    # Handles YouTube video/audio download with yt-dlp
│   ├── whisper_utils.py    # Transcribes audio to text using OpenAI Whisper
│   ├── qa_utils.py         # Vector database setup and chatbot chain loading (LangChain)
│   ├── summary_utils.py    # Builds and runs summarization prompts using LangChain
│   └── agent_memory_chain.py # Memory-aware chatbot chain setup for context handling

---
```

## SmartTube Assistant interface 
![home](https://github.com/user-attachments/assets/2b6b1f3e-c17f-4132-a119-ca752f6f052f)
![choise](https://github.com/user-attachments/assets/df0e120f-f53b-4e51-9a17-9133e0fa6c1c)
![summery](https://github.com/user-attachments/assets/e903b5d5-5eef-4157-97d2-4d87419ee029)
![chatboot](https://github.com/user-attachments/assets/14996d34-c995-4682-ad18-6c3512963bca)


---
---

## SmartTube Assistant App live demo video 
Google drive link :(https://drive.google.com/file/d/11Hzg4soncLTOpNudfEnst1TQ_ZQ-drYh/view?usp=drive_link)


---
## 🌐 LangSmith Dashboard
Log in at [smith.langchain.com](https://smith.langchain.com/) to see traces:
- Summarize Transcript
- Load Chatbot QA Chain
- Process and Store Transcript
---



