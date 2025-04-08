# 🧠 Crash Course in Causality – Wine Quality Prediction

A hands-on causal inference project exploring **causal relationships** vs **correlations** in the context of predicting wine quality. This project goes beyond traditional predictive modeling by answering the *“What causes what?”* question using advanced causal inference frameworks.

---

## 🔍 Objective

While standard machine learning models tell us **what predicts wine quality**, this project aims to answer:

> ✅ What **features cause** changes in wine quality?

This subtle shift from correlation to causation is critical for **decision-making systems**, **interventions**, and **policy-level insights** — especially in fields like healthcare, marketing, and social sciences.

---

## 📦 Key Tools & Libraries

- **Python 3.10+**
- [`DoWhy`](https://github.com/microsoft/dowhy) – Causal inference using graphical models
- [`EconML`](https://github.com/microsoft/EconML) – Heterogeneous treatment effect estimation
- `pandas`, `matplotlib`, `scikit-learn` – Data analysis & visualization
- `networkx` – For visualizing causal graphs
- Jupyter Notebooks

---

## 🧪 Methodology

### 1. 📊 Baseline Prediction
- Built a regression model to predict wine quality using physiochemical attributes.
- Evaluated R² score and feature importances.

### 2. 🔗 Causal Graph Modeling
- Created a **Directed Acyclic Graph (DAG)** based on domain knowledge to represent hypothesized causal relationships.
- Identified confounders and treatment variables.

### 3. 🧮 Causal Inference with DoWhy
- Defined treatment (`alcohol`, `volatile acidity`, etc.)
- Used backdoor criterion to identify valid adjustment sets
- Estimated Average Treatment Effect (ATE) via multiple estimators (Linear Regression, Stratification, Reweighting)

### 4. 📐 Heterogeneous Treatment Effects with EconML
- Applied **Doubly Robust Learners**, **Causal Forest**, and **Orthogonal Random Forests** to estimate individual-level causal effects.
- Visualized conditional effects and confidence intervals.

---

## 📈 Key Results

- Some features (like `alcohol`) show strong correlation but not a high **causal effect** when confounders are accounted for.
- Estimated **true causal impact** of controllable attributes on wine quality.
- Demonstrated how naive interpretations from correlation-based models can be misleading.

---

## 🎯 Takeaways

- Causality helps us move from *observational insights* to *actionable interventions*.
- ML + causal inference offers a powerful framework for robust decision-making.
- Tools like DoWhy and EconML make causal analysis accessible and reproducible.

---
