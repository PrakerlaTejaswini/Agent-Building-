# 🎮 Agentic Game-Builder AI

An agentic AI system that converts ambiguous natural-language game ideas into a fully playable HTML/CSS/JavaScript game using a structured multi-phase workflow.

---

## 🚀 Features

- Accepts natural-language game ideas
- Asks clarifying questions before coding
- Creates an internal implementation plan
- Generates runnable game files:
  - `index.html`
  - `style.css`
  - `game.js`
- Runs fully inside Docker
- Supports Gemini LLM API

---

## 🧠 Agent Architecture

The agent follows a **3-phase agentic workflow**:

### 1. Clarification Phase
- Analyzes the user's game idea
- Asks targeted follow-up questions
- Stops only when requirements are clear

### 2. Planning Phase
- Defines:
  - Game mechanics
  - Controls
  - Win/loss conditions
  - File structure
- Chooses Vanilla JavaScript for reliability

### 3. Execution Phase
- Generates:
  - `index.html`
  - `style.css`
  - `game.js`
- Ensures the game runs locally in a browser

### 4. Evaluation (Lightweight)
- Verifies required files exist
- Confirms output structure

---

## 🗂️ Project Structure


agentic-game-builder/
│
├── agent.py
├── llm.py
├── phases/
│ ├── clarify.py
│ ├── plan.py
│ ├── generate.py
│
├── evaluation/
│ └── metrics.py
│
├── Dockerfile
├── requirements.txt
└── README.md


