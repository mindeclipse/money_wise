# MoneyWise 💰🤖

MoneyWise is an end-to-end autonomous financial AI agent designed to parse unstructured user queries, orchestrate analytical workflows, and deliver precise financial insights. By leveraging the power of Large Language Models and strict tool-calling architectures, the agent completely eliminates common LLM mathematical hallucinations.

## 🚀 Core Features

- **Autonomous Orchestration:** Uses an agentic loop to break down complex financial questions into sequential logical steps.
- **Strict Tool Calling (Function Calling):** Explicitly binds the LLM to localized Python functions for numerical data processing, preventing factual and computational errors.
- **Advanced Data Manipulation:** Integrates with powerful data science libraries to compute, filter, and structure financial data dynamically.
- **Structured Logging:** Tracks the internal reasoning path of the agent for transparent auditing and rapid system debugging.

## 🛠️ Built With (Tech Stack)

- **Language:** Python 3.10+
- **Framework:** LangChain (Agentic orchestration & memory)
- **LLM Engine:** Gemini 1.5 Flash-lite (via Google AI Studio / Gemini API)
- **Data Engineering:** Pandas, NumPy
- **Environment Management:** Dotenv, Git

## 📐 System Architecture & Logic

Unlike traditional chat bots that attempt to calculate results directly within their text generation parameters, **MoneyWise** operates via a strict separation of concerns:

1. **User Input:** The user submits a raw, unformatted prompt (e.g., *"Calculate the net profit margin trend based on last quarter's CSV sheets"*).
2. **Reasoning Loop:** LangChain structures the prompt and passes it to the Gemini model to decide *which* mathematical or data-parsing tool needs to be invoked.
3. **Deterministic Execution:** The agent triggers local Python tools powered by **Pandas** and **NumPy**. The execution happens within a safe environment, ensuring mathematical validity.
4. **Synthesis:** The precise output of the tool is fed back into the LLM, which compiles a clean, human-readable financial report.

## 📦 Installation & Setup

Follow these steps to run MoneyWise locally on your machine:

### 1. Clone the Repository
```bash
git clone https://github.com/mindeclipse/money_wise.git
cd moneywise
