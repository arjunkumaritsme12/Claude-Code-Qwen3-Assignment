# Claude Code + Qwen3:4B — Pre-Masterclass Assignment

This repo is my submission for the **"Building Agentic Systems with Claude Code and MCP"** Masterclass by GLA University. The assignment covers setting up a local LLM pipeline from scratch — installing Ollama, pulling the Qwen3:4B model, and querying it through a Python script.

---

## What's Inside

```
claude-code-qwen-assignment/
├── app.py              # Python script to query the local Qwen model
├── screenshots/        # All task screenshots
│   ├── Screenshot 1 (claude-code-installed).png
│   ├── Screenshot 2 (ollama-version).png
│   ├── Screenshot 3 (qwen-model-list).png
│   ├── Screenshot 4 (model-chat-response).png
│   └── Screenshot 5 (python-app-response).png
├── .gitignore          # Ignores venv and cache files
└── README.md           # This file
```

---

## Steps I Followed

### 1. Installed Claude Code
Installed Claude Code globally via npm:
```bash
npm install -g @anthropic-ai/claude-code
```

### 2. Installed Ollama
Downloaded Ollama from [ollama.com](https://ollama.com) and verified the installation:
```bash
ollama --version
```

### 3. Pulled the Qwen3:4B Model
```bash
ollama pull qwen3:4b
```
Verified it showed up in the model list:
```bash
ollama list
```

### 4. Ran the Model Directly
Had a quick chat with the model to test it:
```bash
ollama run qwen3:4b
```
Asked: *What is Machine Learning?* — got a detailed response.

### 5. Python Integration
Built `app.py` to interact with the model via the Ollama REST API:
```bash
pip install requests
python app.py
```
Asked: *What is Generative AI?* — worked perfectly.

---

## How to Run

Make sure Ollama is running in the background, then:

```bash
# Install dependency
pip install requests

# Run the script
python app.py
```

You'll be prompted to enter any question — the script sends it to the local Qwen3:4B model and prints the response.

---

## Stack

| Tool | Purpose |
|------|---------|
| Claude Code | Agentic coding CLI |
| Ollama | Running LLMs locally |
| Qwen3:4B | The language model |
| Python + Requests | Querying the model via API |
| Git + GitHub | Version control |

---

## Notes

- Model runs fully **offline** on local machine — no API key needed
- Ollama exposes the model at `http://localhost:11434`
- Response time depends on your system specs (CPU vs GPU)