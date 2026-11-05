# AI-Powered Conversational Interview Assistant

## About the Project

The AI-Powered Conversational Interview Assistant is a web-based application that helps users practise mock interviews using AI.

Users can select an interview subject, answer questions through voice recordings, and receive AI-generated feedback based on their answers. The application maintains conversation history and generates relevant follow-up questions to create a more interactive interview experience.

## Features

- Select an interview subject:
  - Self Introduction
  - Generative AI
  - Python
  - English
  - HTML
  - CSS
- AI-powered interview questions using Google Gemini.
- Voice-based answers using audio recording.
- Speech-to-text conversion using AssemblyAI.
- Text-to-speech responses using Murf AI.
- Conversation memory to maintain interview context.
- Contextual follow-up questions based on previous answers.
- AI-generated interview feedback and improvement suggestions.
- Interview completion after five questions.

## Technologies Used

**Frontend**
- HTML
- CSS
- JavaScript
- MediaRecorder API
- getUserMedia API

**Backend**
- Python
- Flask

**AI and Supporting Technologies**
- LangChain
- LangGraph
- Google Gemini
- Murf AI
- AssemblyAI

## Installation

Install the required Python packages one by one:

**1. Install Flask**
```bash
pip install flask
```

**2. Install LangChain, LangGraph and Google Gemini integration**
```bash
pip install langchain langgraph langchain-google-genai
```

**3. Install Python dotenv**
```bash
pip install python-dotenv
```

**4. Install Flask CORS**
```bash
pip install flask-cors
```

**5. Install AssemblyAI for speech-to-text**
```bash
pip install assemblyai
```

## API Configuration

Create a `.env` file in the project and configure the following API keys:

```env
GOOGLE_API_KEY=your_google_api_key
MURF_API_KEY=your_murf_api_key
ASSEMBLYAI_API_KEY=your_assemblyai_api_key
```

Replace the placeholder values with your actual API keys.

## Running the Backend

Start the Flask backend server from the project root directory:

```bash
python ./backend/app.py
```

If Flask debug mode is enabled, the server automatically restarts whenever you save code changes.

## Application Workflow

1. Select an interview subject.
2. The AI interviewer greets the user and asks the first question.
3. Record and submit an answer using the microphone.
4. AssemblyAI converts the recorded audio into text.
5. LangChain and LangGraph maintain conversation context and generate relevant follow-up questions.
6. Murf AI converts the AI response into speech.
7. After five questions, the interview is completed.
8. The application generates feedback, a candidate score, and areas for improvement.

## Backend API Endpoints

| Endpoint | Method | Description |
|---|---|---|
| `/start-interview` | POST | Starts an interview and generates the first question. |
| `/submit-answer` | POST | Accepts recorded audio, transcribes the answer, and generates a follow-up question. |
| `/get-feedback` | POST | Generates interview feedback and a candidate score. |

## Feedback Details

At the end of the interview, the AI generates:

- Subject
- Candidate Score (1–5)
- Feedback
- Areas of Improvement

## Conclusion

This project combines conversational AI, voice recognition, text-to-speech, and conversation memory to provide an interactive mock interview experience. It helps users practise interview skills and identify areas for improvement.
