# 🎯 Automata & Compiler Visualizer

A full-stack web application for visualizing and working with **Finite Automata (NFA, DFA)** and **Context-Free Grammars (CFG)**.

Built with **React, D3.js, FastAPI, and Python**, this project provides an interactive platform to understand core concepts of **Automata Theory** and **Compiler Design** through visualization and algorithm implementation.

---

## 📌 Overview

The **Automata & Compiler Visualizer** is designed as an educational tool for students and developers. It combines theoretical algorithms with graphical visualization to make complex formal language and compiler concepts easier to understand.

The system supports:

- ✅ Regular Expression → NFA conversion  
- ✅ NFA → DFA conversion  
- ✅ DFA Minimization  
- ✅ FIRST set computation  
- ✅ FOLLOW set computation  
- ✅ LL(1) Predictive Parsing Table generation  

The backend performs all algorithmic computations, while the frontend provides interactive graph-based visualization.

---

## 🚀 Features

### 🔄 Automata Operations

### 1️⃣ Regex to NFA
- Implements **Thompson’s Construction Algorithm**
- Supports operators: `*`, `+`, `|`, `()`, `ε`
- Automatically handles epsilon transitions
- Interactive graph visualization

### 2️⃣ NFA to DFA
- Uses **Subset Construction Algorithm**
- Computes epsilon-closure
- Converts non-deterministic automata into deterministic automata
- Displays resulting DFA visually

### 3️⃣ DFA Minimization
- Implements **State Partitioning Algorithm**
- Merges equivalent states
- Reduces automata size while preserving language recognition

### 🎨 Interactive Graph Features
- Draggable nodes
- Zoom & pan functionality
- Color-coded states:
  - 🟢 Start state  
  - 🔵 Accept states  
  - ⚪ Normal states  

---

## 📐 Context-Free Grammar Tools

### 1️⃣ FIRST Set Computation
- Handles epsilon productions
- Supports recursive rules
- Uses fixed-point iteration

### 2️⃣ FOLLOW Set Computation
- Computes valid terminal symbols following non-terminals
- Uses FIRST sets internally
- Correct epsilon handling

### 3️⃣ Predictive Parsing Table
- Generates LL(1) parsing table
- Detects grammar conflicts
- Displays structured parsing matrix

---

## 🧠 Algorithms Implemented

| Algorithm | Purpose |
|------------|----------|
| Thompson’s Construction | Regex → NFA |
| Subset Construction | NFA → DFA |
| State Partitioning | DFA Minimization |
| FIRST Set Algorithm | Compute FIRST sets |
| FOLLOW Set Algorithm | Compute FOLLOW sets |
| LL(1) Table Construction | Build Predictive Parsing Table |

---

## 🛠 Tech Stack

### 🔹 Frontend
- React.js  
- D3.js (Graph Visualization)  
- Tailwind CSS  
- Vite  
- Axios  

### 🔹 Backend
- FastAPI  
- Python 3.8+  
- Pydantic  
- Uvicorn  

---

## 📂 Project Structure
(
```
automata-visualizer/
│
├── backend/ # FastAPI backend (API + Algorithms)
│ ├── main.py # Application entry point
│ ├── requirements.txt # Python dependencies
│ │
│ ├── automata/ # Core algorithm implementations
│ │ ├── regex_parser.py # Regex → NFA
│ │ ├── nfa.py # NFA → DFA
│ │ ├── dfa.py # DFA implementation
│ │ ├── minimizer.py # DFA minimization
│ │ └── cfg_tools.py # FIRST, FOLLOW, Parsing table
│ │
│ └── models/ # Optional database models
│
├── frontend/ # React frontend
│ ├── src/
│ │ ├── components/
│ │ │ ├── Controls.jsx # Input controls
│ │ │ ├── GraphView.jsx # D3 visualization
│ │ │ └── CFGView.jsx # CFG result display
│ │ ├── App.jsx # Main application
│ │ ├── api.js # API communication
│ │ └── main.jsx # React entry point
│ │
│ ├── package.json
│ └── vite.config.js
│
└── README.md


---
)

## ⚙️ Installation & Setup

### 🔹 Backend Setup

```bash
cd backend
python -m venv venv
venv\Scripts\activate        # Windows
# or
source venv/bin/activate     # Mac/Linux

pip install -r requirements.txt
python main.py


Backend runs at:

http://localhost:8000


API Documentation:

http://localhost:8000/docs

🔹 Frontend Setup
cd frontend
npm install
npm run dev


Frontend runs at:

http://localhost:5173

📡 API Endpoints

POST /regex/to-nfa

POST /nfa/to-dfa

POST /dfa/minimize

POST /cfg/first-follow

POST /cfg/predictive-table

🎓 Educational Purpose

This project is ideal for:

Automata Theory courses

Compiler Design courses

Academic demonstrations

Algorithm visualization practice

Understanding formal languages

It bridges the gap between theory and practical implementation.

🔮 Future Enhancements

Step-by-step automata simulation

String validation for automata

Export automata as JSON/PNG/SVG

LR/SLR/LALR parsing support

Project saving & user authentication

Dark mode support


