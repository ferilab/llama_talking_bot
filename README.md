# llama_talking_bot

# An AI-powered Voice-Interactive Chatbot (LLaMA 3 + AssemblyAI + ElevenLabs) that talks to you!

This package provides a real-time voice-interactive AI assistant. Speak to it using your microphone, and it will respond with both spoken and written answers. It leverages:

- AssemblyAI (https://www.assemblyai.com/) for real-time speech-to-text
- Ollama (https://ollama.com/) with LLaMA 3 for generating responses
- ElevenLabs (https://www.elevenlabs.io/) for realistic text-to-speech

---

## Package structure

llama_taking_bot
├── constants.py # Your personal API keys go here
├── chatbot.py # The main chatbot script (voice input + AI + voice output)
├── testmic.py # A microphone test script to verify your audio input
├── requirements.txt
├── __init__.py


## Install dependencies

pip onstall -r requirements.txt

OR

1. pip install ollama
2. ollama pull llama3
3. Make sure to install `apt install portaudio19-dev` (Debian/Ubuntu) or `brew install portaudio` (MacOS)
4. pip install "assemblyai[extras]"
5. pip install elevenlabs
6. pip install PyAudio   # provides Python bindings for PortAudio v19, the cross-platform audio I/O library.
7. brew install mpv


## Required API keys

You will need to sign up for the following services:

AssemblyAI – for real-time speech-to-text via https://www.assemblyai.com/
Note: Real-time transcription requires a paid account with a credit card on file.

ElevenLabs – for voice generation via https://www.elevenlabs.io/

Once you have both API keys, add them in the constants.py file in the project root like this:

assemblyai_api_key = "your_assemblyai_api_key_here"
elevenlabs_api_key = "your_elevenlabs_api_key_here"

## Test Your Microphone

Before running the chatbot, use the following command to test if your microphone is working:

python testmic.py

You should hear your voice playback after 5 seconds of recording.

## Run the Chatbot

Start the voice-enabled chatbot with:

python chatbot.py

You can now start speaking! The bot will:

- Transcribe your voice,
- Generate a smart response using LLaMA 3,
- Reply back to you both via voice and in text.