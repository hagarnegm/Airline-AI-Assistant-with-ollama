# FlightAI Chat Assistant

This project implements a simple airline chatbot using Gradio and a local Ollama LLM (model `llama3.2`). The assistant provides short, accurate answers about ticket prices to specific destinations.

---

## Features

- Connects to a local Ollama API for LLM completions
- Provides ticket price information via a tool function
- Responds courteously with concise answers (max one sentence)
- Handles user input and maintains chat history
- Gradio chat interface for easy interaction

---

## Setup

1. Ensure Ollama is running locally and accessible at `http://localhost:11434/v1`.
2. Install required packages:
```bash
pip install gradio openai
```
3. Run the script.

---

## Code Summary

- Defines a system prompt to control assistant behavior.
- Maintains a dictionary of ticket prices.
- Implements a tool function to fetch prices based on destination.
- Chat function checks for city mentions and returns prices or otherwise queries the model.
- Uses `gr.ChatInterface` for the UI.

---

## Usage

Run the script and interact with the chatbot in the web UI. Ask about ticket prices for London, Paris, Tokyo, or Berlin.

---

## Notes

- The API key for Ollama is a placeholder (`'ollama'`) since local usage does not require a real key.
- Responses are limited to one sentence and prioritize accuracy.
- Unknown destinations return "Unknown".
