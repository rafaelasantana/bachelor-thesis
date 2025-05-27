# 🎓 Bachelor Thesis: Reducing Hallucinations in LLMs with Prompt Engineering

This repository contains the full implementation and results for the bachelor thesis:

> **Comparing Chain-of-Thought, Chain-of-Verification and Self-Refine in Solving Brazilian University Entrance Exams**  
> _Rafaela Rolim Santana · University of Applied Sciences Technikum Wien · 2025_

📄 [Read the final thesis PDF](./BachelorThesisFinal.pdf)

## 🧠 Overview

Large Language Models (LLMs) like ChatGPT are popular learning aids, but they often generate misleading or false answers — a problem known as **hallucination**. This project investigates whether simple **prompting techniques** can reduce hallucinations without requiring fine-tuning or external tools.

Three prompting strategies were compared:

- 🔗 **Chain-of-Thought (CoT)** – guides the model through step-by-step reasoning.
- ✅ **Chain-of-Verification (CoVe)** – verifies and revises the initial answer.
- 🔁 **Self-Refine** – applies iterative self-feedback loops to refine output.

All techniques were evaluated on **180 ENEM 2024** questions (Brazil’s national university entrance exam), using **GPT-3.5 Turbo**, with **40 runs per question** to assess accuracy and consistency.

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/rafaelasantana/bachelor-thesis.git
cd bachelor-thesis
````

### 2. Install Python packages
Create and activate a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Alternatively, you can install Jupyter via Homebrew and run notebooks outside the venv:

```bash
brew install jupyterlab
```

### 3. Provide your OpenAI API key
Save your OpenAI API key in a file named openai-key.txt in the Notebooks/ folder.

## 🚀 How to Run the Notebooks
Run the Jupyter notebooks in this order:

📌 RunTests.ipynb
➤ Runs all 3 prompting methods on 180 questions × 40 runs each

🧼 CleanData.ipynb
➤ Aggregates raw outputs, computes accuracy and consistency

📊 CompareResults.ipynb
➤ Performs Kruskal–Wallis and McNemar tests and generates plots

