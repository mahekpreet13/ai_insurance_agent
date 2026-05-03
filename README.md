# 🛡️ Life Insurance Coverage Advisor

A sleek, AI-powered Streamlit application that helps users estimate how much life insurance coverage they need and suggests relevant term-life insurance options.

This tool combines financial modeling with real-time product research to provide personalized, explainable recommendations.

---

## 🚀 Features

* 📊 **Coverage Calculation**

  * Uses discounted cash flow (annuity method) to estimate income replacement needs
  * Factors in debts, savings, and existing insurance

* 🤖 **AI Agent Integration**

  * Uses OpenAI for reasoning
  * E2B for deterministic financial calculations
  * Firecrawl for real-time insurance product research

* 📈 **Transparent Breakdown**

  * Step-by-step math explanation
  * Clear assumptions and methodology

* 🌐 **Localized Recommendations**

  * Suggests insurance providers based on user location


---

## 🧱 Tech Stack

* **Frontend**: Streamlit
* **AI Model**: OpenAI (GPT-5 Mini)
* **Computation Engine**: E2B (Python execution)
* **Web Search**: Firecrawl
* **Language**: Python 3.9+

---



## 🔑 Prerequisites

You will need API keys for:

* OpenAI → https://platform.openai.com/api-keys
* Firecrawl → https://www.firecrawl.dev/app/api-keys
* E2B → https://e2b.dev

---

## ⚙️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/life-insurance-advisor.git
cd life-insurance-advisor
```

2. **Create a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the App

```bash
streamlit run app.py
```

The app will open in your browser automatically.

---

## 🧠 How It Works

### Step 1: User Input

User provides:

* Age
* Income
* Dependents
* Debt
* Savings
* Existing insurance
* Coverage duration

---

### Step 2: Coverage Calculation

The app computes:

* Discounted income replacement using:

[
Income \times \frac{1 - (1 + r)^{-n}}{r}
]

Where:

* `r` = real discount rate (default 2%)
* `n` = years of income replacement

Then:

```
Recommended Coverage =
  Discounted Income
+ Total Debt
- Savings
- Existing Insurance
```

---

### Step 3: AI Agent Workflow

The agent:

1. Uses **E2B** to run Python code for exact calculations
2. Uses **Firecrawl** to search for relevant insurance products
3. Returns structured JSON with:

   * Coverage amount
   * Breakdown
   * Assumptions
   * Recommendations

---


## 🧪 Example Use Case

| Input              | Example Value |
| ------------------ | ------------- |
| Annual Income      | $85,000       |
| Debt               | $200,000      |
| Savings            | $50,000       |
| Existing Insurance | $100,000      |
| Years              | 10            |

➡️ Output: Estimated coverage needed + recommended insurers


---

## 💡 Disclaimer

This tool is for educational purposes only and does not provide licensed financial advice. Always consult a professional before making financial decisions.

---
