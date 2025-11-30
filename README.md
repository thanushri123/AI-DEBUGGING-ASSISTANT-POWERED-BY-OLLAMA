# 🤖 AI DEBUGGING ASSISTANT - POWERED BY OLLAMA

---

A fast, local, privacy-focused AI debugging companion built with FastAPI, Ollama, and a modern interactive chat UI. This project gives the experience of ChatGPT-style debugging, completely offline, using locally-running LLM models. The AI Debugging Assistant helps developers troubleshoot code, logs, errors, and stack traces in real time.
It behaves like a senior debugging engineer — answering questions, guiding troubleshooting, and suggesting fixes with clean explanations and code examples.

---

### 💬 CHAT UI SCREENSHOTS -

---

<img width="1893" height="882" alt="Screenshot 2025-11-27 124809" src="https://github.com/user-attachments/assets/4395313b-49bb-47d9-b6f6-1304972e9e74" />

---

<img width="1891" height="887" alt="Screenshot 2025-11-27 125030" src="https://github.com/user-attachments/assets/eaf72648-85fa-4055-8c37-d3673e785939" />

---

<img width="1886" height="873" alt="Screenshot 2025-11-27 125100" src="https://github.com/user-attachments/assets/5afb3986-5ab2-4f38-8e32-2171d9de6925" />

---

<img width="1885" height="876" alt="Screenshot 2025-11-27 125233" src="https://github.com/user-attachments/assets/3f621778-ad4c-4835-84d7-2b3d45fb50af" />

---

<img width="1890" height="877" alt="Screenshot 2025-11-27 125310" src="https://github.com/user-attachments/assets/0fbe6a54-cab1-481e-9c6c-cad40740577e" />

---

<img width="1891" height="878" alt="image" src="https://github.com/user-attachments/assets/c056b25f-8812-42a7-a8a4-b011265034b4" />

---

<img width="1890" height="874" alt="image" src="https://github.com/user-attachments/assets/197d37bc-43b2-410f-908d-6ec89bb3db1d" />

---

<img width="1891" height="874" alt="Screenshot 2025-11-27 130024" src="https://github.com/user-attachments/assets/ac2aee02-9f9e-4f2e-a28b-edf08484fd20" />

---

<img width="1891" height="882" alt="Screenshot 2025-11-27 130137" src="https://github.com/user-attachments/assets/700c5e55-428a-4c30-9b41-ee8e8661e9be" />

---

### 🚀 FEATURES -

---

🧠 ChatGPT-like conversational debugging

🔍 Understands logs, errors, stack traces, configurations

💡 Provides fixes, explanations, and next steps

👨‍💻 Generates corrected code, refactors, and debugging snippets

🤝 Multi-turn conversation (context-aware)

🔄 Model Switching with animation + sound cue

📦 Supports multiple Ollama models:

    - qwen2.5-coder:1.5b

    - deepseek-coder:1.3b

    - llama3.2:1b

    - qwen2.5:0.5b


📦 Code blocks with copy button

🔐 100% local — no cloud, no external API

⚡ Built for speed using FastAPI + HTTPX + async pipelines

---

### 🛠️ INSTALLATION GUIDE -

This project requires:

   - Python 3.10+

   - Node NOT required (pure JS)

   - Ollama installed → https://ollama.ai/download

   - Download at least one model:

           ollama pull qwen2.5-coder:1.5b
           ollama pull deepseek-coder:1.3b
           ollama pull llama3.2:1b
           ollama pull qwen2.5:0.5b

     or install only what you plan to use.

---

### 🚀 SETUP AND RUN INSTRUCTIONS -

---

1️⃣ Install dependencies

        cd backend
        
        pip install -r requirements.txt

---

2️⃣ Start Ollama

Make sure the service is running:

        ollama serve

---

3️⃣ Start the Backend Server

Run FastAPI with auto-reload:

        uvicorn backend.app:app --host 127.0.0.1 --port 8000 --reload
    
If you placed app.py differently, update the path accordingly.

You should see:
 
        Uvicorn running on http://127.0.0.1:8000

---

4️⃣ Start the Frontend

        frontend/index.html

Just double-click it, or use Live Server in VS Code.

---

### 🔥 HOW TO USE -

---

1. Select the model from the dropdown

2. Watch live model-switch animation + sound cue

3. Ask anything related to:

  - Debugging logs

  - Fixing errors

  - Understanding stack traces

  - Code rewriting

  - Backend/frontend issues

The AI responds with formatted markdown, step headings, emojis, and copy-ready code blocks.

---

### 🧠 HOW DOES IT WORK -

---

1. User enters a debugging question

2. Frontend sends message + selected LLM model

3. FastAPI sends structured messages to the Ollama Chat endpoint

4. Ollama generates debugging instructions, fixes, or code

5. Response is rendered with markdown, code blocks, and animations

--

### 📦 PROJECT STRUCTURE -

---

         /backend
            app.py
         /frontend
            index.html
            chat.js
            style.css
         requirements.txt
         README.md

---

### 📁 REQUIREMENTS.TXT -

---

Install them using:

         pip install -r requirements.txt

```bash

        fastapi
        uvicorn
        httpx
        pydantic
