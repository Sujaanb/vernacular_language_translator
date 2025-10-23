# Access Multiple LLMs

This project provides a unified interface to access multiple Large Language Models (LLMs) such as **Mistral**, **Gemini**, and **OpenAI**, with support for local models as well. It enables seamless switching between providers for experimentation, prototyping, or integration.

---

## 📋 Prerequisites

Make sure you have the following installed:

* Python **3.8+**
* Git
* A code editor like **VSCode**, **Cursor**, or **WindSurf**

---

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Sujaanb/access-multiple-llm.git
cd access-multiple-llm
```

### 2. Create and Activate a Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate environment
# For Windows (PowerShell):
./venv/Scripts/Activate

# For macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Get API Keys

Obtain free API keys from the following providers:

* [Mistral](https://console.mistral.ai/api-keys)
* [Google Gemini](https://aistudio.google.com/app/apikey)
* (Optional) [OpenAI](https://platform.openai.com/account/api-keys)

### 5. Create a `.env` File

Create a `.env` file in the root directory with the following structure:

```ini
llm_provider = "mistral"  # Options: "mistral", "gemini", "openai"

mistral_api_key = ""      # Your Mistral API key (optional)

gemini_api_key = ""       # Your Gemini API key (optional)

openai_api_key = ""       # Your OpenAI API key (optional)

local_model_url = "http://localhost:11434"  # URL for local model (if used)
```

> **Note:** You can leave API keys empty if you don't have access to certain providers.
> The application will use the `llm_provider` you specify, as long as a valid API key is provided for it.
> Select the `llm_provider` as required among the three currently given options.

---

## ▶️ Run the Project

To execute a basic test using your selected provider:

```bash
python test_run.py
```

---

## ✅ Supported LLM Providers

* [x] Mistral
* [x] Gemini
* [x] OpenAI
* [x] Local Model (via Ollama)

---

## 🧩 Extending Support

Support for additional LLM providers can be **easily extended** if required.
Feel free to contribute or open an issue to request integration with other APIs.

---
