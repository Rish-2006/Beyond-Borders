# Project: LifeCoach
> **Company:** Personal / Group Project
> **Vertical:** Personal Productivity
> **Type:** Prototype
> **Status:** Beginner Level Completed

---

## Project Summary

LifeCoach is a private, offline AI-powered daily clarity companion built on Google Gemma 4, running 100% on the user's device. It helps users organize their thoughts, make decisions, and reflect on their day through three auto-detected interaction modes: Morning Mode (priority setting), Decision Mode (guided self-reflection), and Evening Mode (daily review). All conversations remain strictly confidential and never leave the user's computer.

---

## Motivation

Most AI assistants send your thoughts and personal reflections to remote servers, creating privacy risks for sensitive mental clarity and decision-making conversations. LifeCoach fills this gap by providing a structured, private, and offline alternative — combining the power of a large language model with a zero-data-exposure guarantee, all wrapped in a lightweight desktop interface accessible to non-technical users.

---

## Goals

- Deliver a fully offline AI coaching experience with no data leaving the user's device
- Provide structured, mode-based interactions (Morning / Decision / Evening) for daily mental clarity
- Keep the setup simple enough for non-developers via a single `setup.bat` script on Windows

---

## Technical Approach

LifeCoach is built using a local inference stack powered by **Ollama** running **Google Gemma 4 (e4b)**. A custom `Modelfile` defines the system prompt and three behavioural modes (Morning, Decision, Evening) with strict response constraints (under 120 words per reply, one question at a time). The desktop GUI is built with **Python + Tkinter**, communicating with Ollama's local REST API (`http://localhost:11434`) via the `requests` library with streaming support. A `setup.bat` script automates model download, model build, dependency installation, and app launch for Windows users.

**Key Components:**
- `Modelfile` — custom system prompt and model parameters (temperature 0.7, context 8192 tokens)
- `app.py` — Python/Tkinter GUI with chat bubble rendering and streaming response display
- `setup.bat` — one-click Windows setup and launcher
- Ollama — local inference engine

---

## Milestones

| Milestone | Description | Target Date |
|---|---|---|
| M1 | Define system prompt, modes, and Modelfile; validate Gemma 4 locally | Completed |
| M2 | Build Python/Tkinter desktop GUI with streaming chat and bubble UI | Completed |
| M3 | Write `setup.bat` automation, README, and demo script; final testing | Completed |

---

## How to Contribute

Github Repository: https://github.com/Rish-2006/LifeCoach

This is a completed group prototype. Contributions that extend platform support, improve the GUI, or add new coaching modes are welcome.

**Skills Needed:**
- Python (Tkinter, `requests`)
- Prompt engineering / LLM Modelfile authoring
- Shell scripting (Batch for Windows, Bash for macOS/Linux)

**Getting Started:**
1. Clone the repository and run `setup.bat` (Windows) to verify the full stack works locally
2. Read `DEMO_SCRIPT.md` to understand the intended user experience and mode behaviour
3. Open an issue or pull request describing your proposed change before starting work

---

## Current Contributors

| Name | GitHub | Role |
|---|---|---|
| Rishit Dev |  Rish-2006 | |
| Selva Vignesh |   |  |
| Ajaydev  |  ajaydevgit |  |
| vedha |  vedhavk |  |
| akshay | Akshayvs-Tech  |  |


---

## Related Problem Statements

- Privacy risks in cloud-based AI mental wellness tools
- Lack of structured, offline-first daily reflection companions for personal productivity

---

## Resources

- [Ollama](https://ollama.com) — Local LLM inference engine
- [Google Gemma 4 Model](https://ollama.com/library/gemma4) — Underlying open-weights language model
- [Apache License 2.0](./LICENSE) — Project license
- [`DEMO_SCRIPT.md`](./DEMO_SCRIPT.md) — Guided walkthrough of all three modes

---

*Part of Beyond Borders by The Purple Movement.*