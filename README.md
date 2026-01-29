# Explainable AI for Credit Risk Modeling

This project applies **Explainable Artificial Intelligence (XAI)** techniques to a
binary credit risk classification task using the **German Credit Dataset**.

The goal is to balance **predictive performance**, **interpretability**, and
**fairness analysis** in high-stakes financial decision-making.

---

## Problem Statement
Modern machine learning models often act as black boxes.
In credit risk modeling, this lack of transparency limits trust,
regulatory compliance, and human accountability.

This project addresses that challenge by:
- Training multiple ML models
- Selecting the best-performing model
- Applying **post-hoc explainability techniques**
- Auditing bias and fairness

## ⚠️ Notebook Rendering Notice

Due to interactive visualizations (SHAP, LIME, JavaScript widgets),
GitHub may not render the `.ipynb` file correctly.

### ✅ How to view the project:
- 📌 **Recommended**: Open `Explainable_AI_Credit_Risk.html`
- ▶️ Run the notebook directly in **Google Colab**
- ⬇️ Download the `.ipynb` and run locally

This is a known GitHub limitation and does not affect reproducibility.
---

## Models Used
- Logistic Regression
- Decision Tree
- Random Forest
- Multi-Layer Perceptron (MLP)
- **XGBoost (Best Performer)**

Evaluation metric:
- **ROC-AUC (cross-validated)**

---

## Explainability Methods
- **SHAP (TreeExplainer)**
  - Global feature importance
  - Local explanations
  - Waterfall & decision plots
- **LIME**
  - Instance-level explanations
  - Human-interpretable feature effects

---

## Bias & Fairness Audit
Fairness was evaluated across:
- Personal Status / Sex (proxy)
- Foreign Worker status
- Age groups

Both **prediction rates** and **SHAP contribution patterns**
were analyzed to detect indirect bias.

---

## Counterfactual Analysis
"What needs to change for a different decision?"

Small improvements in:
- Savings
- Account status

were shown to measurably increase approval probability,
supporting actionable explanations.

---

## Dataset
- **German Credit Dataset**
- Source: UCI Machine Learning Repository

---

## 🚀 How to Run

```bash
git clone https://github.com/your-username/explainable-credit-risk.git
cd explainable-credit-risk
pip install -r requirements.txt
jupyter notebook

