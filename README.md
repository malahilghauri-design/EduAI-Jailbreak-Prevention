# Extending SHAPE Benchmark: DeepSeek-R1 as a Pedagogical Guard 🎓

## 📖 Academic Research Context
**Inspired by:** *SHAPE: Unifying Safety, Helpfulness and Pedagogy for Educational LLMs* (Accepted at ACL 2026).

### 🚨 The Research Problem (Identified Gap)
The **SHAPE benchmark** identified a massive flaw in current Educational AI: standard LLMs score remarkably low on the "Pedagogy" metric (typically <0.80). When students apply pressure—such as claiming they are running out of time in an exam—standard LLMs experience a **"Pedagogical Jailbreak"**. They prioritize being helpful and immediately surrender the direct answer, completely failing their role as a tutor that should scaffold learning.

### 💡 My Proposed Research Solution
To bridge this critical gap, I propose a novel architecture that utilizes the internal reasoning capabilities of **DeepSeek-R1** (released Jan 2025). Rather than modifying the training data, my research introduces a **Pedagogical Guard** step. By leveraging the `<think>` block, the model internally evaluates the student's intent against pedagogical rules *before* drafting a response. It recognizes the jailbreak attempt and deliberately forces educational scaffolding instead of giving away the answer.

---

## 🛠️ Project Implementation
This repository contains the Python script demonstrating how internal reasoning dramatically improves pedagogical robustness.

### Files Included:
- `pedagogical_tutor.py`: The code comparing a standard helpful LLM against the DeepSeek-R1 pedagogical guard.
- `results_comparison.md`: Analysis showing the prevention of the pedagogical jailbreak.
- `requirements.txt`: Dependencies.

### How to Run:
```bash
pip install -r requirements.txt
python pedagogical_tutor.py
```
