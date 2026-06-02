# 🤖 Building with Claude API — Anthropic

> A hands-on project repository covering core concepts and practical implementations using the **Anthropic Claude API**.

![Claude API](https://img.shields.io/badge/Claude-API-orange?style=for-the-badge&logo=anthropic)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📚 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Modules](#modules)
- [Tech Stack](#tech-stack)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository contains all the code built while following Anthropic's **"Building with Claude API"** course. It progressively covers everything from simple text completions to advanced use cases like tool use, streaming, vision, multi-turn conversations, and more — all using the official [Anthropic Python SDK](https://github.com/anthropic/anthropic-sdk-python).

---

## Project Structure

```
building-with-claude-api/
│
├── 01_basic_completions/
│   ├── hello_claude.py               # First API call — simple text generation
│   ├── prompt_engineering.py         # Prompt design best practices
│   └── system_prompts.py             # Using system prompts to set Claude's behavior
│
├── 02_messages_api/
│   ├── messages_basics.py            # Core Messages API usage
│   ├── multi_turn_conversation.py    # Building a multi-turn chat session
│   └── conversation_history.py      # Managing and trimming message history
│
├── 03_streaming/
│   ├── basic_streaming.py            # Stream responses token by token
│   └── streaming_with_tools.py      # Streaming combined with tool use
│
├── 04_tool_use/
│   ├── basic_tool_use.py             # Defining and invoking tools
│   ├── multi_tool_agent.py           # Chaining multiple tools in a workflow
│   ├── tool_result_handling.py       # Handling tool results and feeding back to Claude
│   └── computer_use_demo.py         # Claude computer use demo (beta)
│
├── 05_vision/
│   ├── image_understanding.py        # Sending images to Claude (base64 & URL)
│   ├── document_analysis.py          # Analyzing PDFs and documents
│   └── multimodal_chat.py            # Multi-turn chat with images
│
├── 06_structured_outputs/
│   ├── json_mode.py                  # Prompting Claude to return valid JSON
│   ├── pydantic_extraction.py        # Structured data extraction with Pydantic models
│   └── schema_validation.py         # Validating Claude outputs against a schema
│
├── 07_prompt_caching/
│   ├── basic_caching.py              # Using prompt caching to reduce latency & cost
│   └── caching_with_tools.py        # Caching with tool definitions
│
├── 08_batch_api/
│   ├── batch_requests.py             # Sending batch requests via the Message Batches API
│   └── batch_results.py             # Polling and processing batch results
│
├── 09_embeddings_and_rag/
│   ├── rag_pipeline.py               # Retrieval-Augmented Generation with Claude
│   ├── vector_store_setup.py         # Setting up a simple vector store
│   └── contextual_retrieval.py      # Anthropic's contextual retrieval technique
│
├── 10_agents/
│   ├── simple_agent.py               # Building a basic agentic loop
│   ├── tool_calling_agent.py         # Full agent with tools and memory
│   └── multi_agent_workflow.py       # Orchestrating multiple Claude agents
│
├── 11_safety_and_guardrails/
│   ├── content_moderation.py         # Using Claude for content moderation
│   └── prompt_injection_defense.py  # Defending against prompt injection attacks
│
├── utils/
│   ├── client.py                     # Shared Anthropic client setup
│   ├── helpers.py                    # Common utility functions
│   └── token_counter.py             # Counting tokens before sending requests
│
├── .env.example                      # Environment variable template
├── requirements.txt                  # Python dependencies
└── README.md                         # This file
```

---

## Getting Started

### Prerequisites

- Python 3.9+
- An [Anthropic API key](https://console.anthropic.com/)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/building-with-claude-api.git
cd building-with-claude-api

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up your environment variables
cp .env.example .env
# Edit .env and add your ANTHROPIC_API_KEY
```

### Environment Setup

Create a `.env` file in the root directory:

```env
ANTHROPIC_API_KEY=sk-ant-your-key-here
```

### Run a Module

```bash
python 01_basic_completions/hello_claude.py
```

---

## Modules

| # | Module | Key Concepts |
|---|--------|-------------|
| 01 | **Basic Completions** | API calls, system prompts, prompt engineering |
| 02 | **Messages API** | Message structure, multi-turn chat, history management |
| 03 | **Streaming** | Token streaming, real-time output |
| 04 | **Tool Use** | Function calling, multi-tool agents, computer use |
| 05 | **Vision** | Image input, document analysis, multimodal chat |
| 06 | **Structured Outputs** | JSON mode, Pydantic extraction, schema validation |
| 07 | **Prompt Caching** | Caching large contexts, cost & latency optimization |
| 08 | **Batch API** | Async bulk requests, batch result processing |
| 09 | **RAG** | Retrieval-Augmented Generation, contextual retrieval |
| 10 | **Agents** | Agentic loops, tool-calling agents, multi-agent systems |
| 11 | **Safety** | Content moderation, prompt injection defense |

---

## Tech Stack

- **[Anthropic Python SDK](https://github.com/anthropic/anthropic-sdk-python)** — Official SDK for Claude API
- **[Python-dotenv](https://github.com/theskumar/python-dotenv)** — Environment variable management
- **[Pydantic](https://docs.pydantic.dev/)** — Data validation and structured output parsing
- **[httpx](https://www.python-httpx.org/)** — Async HTTP client (used under the hood by the SDK)

---

## Key Learnings

- ✅ How to structure effective prompts using system and user messages
- ✅ How to build stateful multi-turn conversations
- ✅ How to extend Claude's capabilities using **Tool Use** (function calling)
- ✅ How to handle **vision/multimodal** inputs (images + text)
- ✅ How to use **streaming** for real-time applications
- ✅ How to reduce costs using **prompt caching** and the **Batch API**
- ✅ How to build **autonomous agents** with memory and tool loops
- ✅ How to apply **safety patterns** to production applications

---

## Resources

- 📖 [Anthropic Docs](https://docs.anthropic.com/)
- 🧪 [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
- 💬 [Claude API Reference](https://docs.anthropic.com/en/api/getting-started)
- 🛠️ [Anthropic Python SDK](https://github.com/anthropic/anthropic-sdk-python)

---

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to open a PR or issue.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">Built with ❤️ using the <a href="https://www.anthropic.com/">Anthropic Claude API</a></p>
