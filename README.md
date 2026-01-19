
This README provides a clear overview of the project, which allows users to interact with three different LLM providers (Ollama, Gemini, and Groq) through a unified Gradio interface.

**
Multi-LLM Streaming Interface**

A lightweight Python application that provides a unified Gradio web interface to interact with multiple Large Language Models (LLMs). This project demonstrates how to implement real-time streaming responses from Ollama (Local), Google Gemini, and Groq using a single, cohesive codebase.

**
🚀 Features**

Multi-Model Support: Seamlessly switch between Gemini, Groq, and local Ollama models.

Real-time Streaming: Responses are yielded token-by-token for a smooth, interactive user experience.

Unified Interface: A clean Gradio UI with a dropdown selector for models and a Markdown-supported output area.

OpenAI Compatibility: Utilizes the OpenAI Python SDK to interact with all three backends (leveraging the OpenAI-compatible endpoints for Gemini and Groq).

**
🛠️ Tech Stack**

Frontend: **Gradio**

LLM Orchestration: OpenAI Python SDK

**Models Supported:**

Google Gemini: via Google Generative AI OpenAI-compatible endpoint.

Groq: High-speed inference for Llama 3.3.

Ollama: Local model execution (Gemma 3).

📋 Prerequisites
Before running the application, ensure you have the following:

Python 3.10+

Ollama Installed: Download Ollama and ensure it's running locally with the gemma3 model pulled:

Bash
ollama pull gemma3
API Keys:

Get a Google Gemini API Key.

Get a Groq API Key.

🔧 Setup & Installation
Clone the repository:

Bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Install dependencies:

Bash
pip install openai python-dotenv gradio google-generativeai groq
Configure Environment Variables: Create a .env file in the root directory and add your keys:

Code snippet
GOOGLE_API_KEY=your_gemini_api_key_here
GROQ_API_KEY=your_groq_api_key_here
📂 Usage
Run the Notebook/Script: Open the Multiple_model.ipynb file in your Jupyter environment or export it to a .py script and run it.

Access the UI: Once launched, Gradio will provide a local URL (usually http://127.0.0.1:7860).

Interacting:

Type your prompt in the Your message textbox.

Select your desired model from the Select model dropdown.

Click Submit to see the streaming Markdown response.

📝 Code Structure
Gemini_call(prompt): Handles the streaming logic for Google's models.

Ollama_call(prompt): Manages the connection to the local Ollama instance.

Groq_call(prompt): Interfaces with the Groq cloud API for high-speed inference.

stream_model(prompt, model): A routing function that directs the input to the appropriate LLM provider based on the UI selection.

gd.Interface: The Gradio configuration that defines the layout and behavior of the web app.
