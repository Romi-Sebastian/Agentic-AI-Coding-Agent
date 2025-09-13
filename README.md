# Agentic AI Coding Agent

A simple **agentic coding agent** in Python, powered by the **Gemini Flash API**.  
The agent runs in a command-line interface. It can inspect code, make changes, and re-run it in an iterative loop using **tool calling**.

## Features
- Uses the Gemini Flash API for reasoning and task execution
- Implements an **agentic loop** for iterative improvements
- Four core tools:
  - List files in a directory
  - Read file contents (with truncation safeguards)
  - Write/overwrite files
  - Execute Python code
- Comes with a sample **calculator app** for the agent to debug and fix
  - Make sure to change the **hardcoded project directory values** from call_function.py and tests.py 
- Built with [UV](https://github.com/astral-sh/uv) for dependency management

## Requirements
- Python 3.10+
- [UV package manager](https://github.com/astral-sh/uv)
- Unix-like shell (bash/zsh or WSL on Windows)
- Gemini API key from [Google AI Studio](https://ai.google.dev/)

## Setup
1. Clone the repository
2. Install dependencies with `uv`
3. Add your Gemini API key to a `.env` file: GEMINI_API_KEY=your_api_key_here
4. Run the agent:
```bash
uv run main.py "Fix my calculator app"
