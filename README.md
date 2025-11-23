# AI Health Chatbot 🩺

A health assistant chatbot powered by AI models (MedBERT and BioGPT) with a FastAPI backend and Streamlit frontend.

## Features

- 🤖 AI-powered health information assistant
- 🔐 User authentication (register/login)
- 💬 Chat interface with history
- 🌓 Light/Dark mode toggle
- 📊 Conversation history tracking
- 🔒 JWT-based authentication

## Prerequisites

- Python 3.8+
- Virtual environment (included as `env/`)

## Installation

1. **Activate the virtual environment:**
   ```powershell
   .\env\Scripts\Activate.ps1
   ```

2. **Install dependencies:**
   ```powershell
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   Create a `.env` file in the project root:
   ```env
   SECRET_KEY=your-secret-key-here
   API_BASE_URL=http://localhost:8000
   ```

## Running the Application

### 1. Start the FastAPI Backend
```powershell
uvicorn app:app --reload --host 0.0.0.0 --port 8000
```

### 2. Start the Streamlit Frontend
Open a new terminal and run:
```powershell
.\env\Scripts\Activate.ps1
streamlit run streamlit_app.py
```

The application will be available at:
- **Backend API:** http://localhost:8000
- **Frontend UI:** http://localhost:8501

## Project Structure

```
AI-CHATBOT/
├── app.py                 # FastAPI backend
├── streamlit_app.py       # Streamlit frontend
├── requirements.txt       # Python dependencies
├── health_chatbot.db      # SQLite database (auto-created)
├── env/                   # Virtual environment
└── Models/                # AI models (MedBERT, BioGPT)
```

## API Endpoints

- `POST /auth/register` - Register new user
- `POST /auth/login` - User login
- `POST /healthbot` - Chat with the AI assistant
- `GET /chat_history` - Retrieve chat history

## Disclaimer

⚠️ **Important:** This application is for informational purposes only and is not a substitute for professional medical advice. Do not enter sensitive or personal information.

## Technologies Used

- **Backend:** FastAPI, SQLite, JWT, bcrypt
- **Frontend:** Streamlit, Requests
- **AI Models:** MedBERT, BioGPT
- **Other:** Python-dotenv, BeautifulSoup4
