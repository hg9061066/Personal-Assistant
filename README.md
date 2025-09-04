# Personal-Assistant
A smart Personal Assistant powered by Python that helps automate daily tasks, manage reminders, search the web, organize notes, and more—all using simple commands. This project integrates multiple productivity features in a minimal, easy-to-use interface.
# Features
Conversational Q&A: Asks your name, prompts for questions, and responds interactively.
Web Search Integration: Uses Google Gemini to fetch concise, intelligent answers.
Text-to-Speech: Reads answers aloud (using gTTS) for a hands-free experience.
Personal & Device Query Handling: Basic logic to handle device-related or personal questions.
Colab-Ready: Secure API key handling using Google Colab’s userdata.

# Setup
Install the requirements:
In your Colab notebook:
python
pip install -q -U google-generativeai
!pip install gTTS
API Key:
Store your Gemini API key securely in Colab:
python
from google.colab import userdata
GOOGLE_API_KEY = userdata.get('GeminiApiKey')
Run the assistant:
Just run the provided code cells in order. The assistant will prompt you for your name and start interacting!

# Usage
The assistant asks your name and then repeatedly prompts, "What do you want?"
Device commands (like “set alarm”, “reminder”, etc.) will reply that the assistant can’t handle device tasks yet.
Personal questions (“Who are you?”, “Who created you?”) will trigger custom responses.
All other questions use Gemini to get an answer (max 40 words), which is also read aloud via gTTS.

# Code Structure
ask_question(name): Prompts user for a question.
classify_question(ques): Classifies if input is device-related or personal.
ask_gemini(ques): Calls Gemini API for a brief text answer.
speak(answer): Speaks the answer using gTTS.

Python 3 (Colab recommended)
google-generativeai
gTTS

# Author
Created by Harshit
For demo or educational purposes.
