# Credit Risk Modeling: Linear Probability, Logit, and Probit Models

## Overview
This project explores the determinants of **credit default risk** using three econometric approaches:
1. **Linear Probability Model (LPM)**
2. **Logit Model**
3. **Probit Model**

The goal is to understand how borrower characteristics affect the likelihood of default and to compare model performance using statistical criteria (AIC, BIC) and predictive accuracy.

---

## Project Summary
The analysis is based on a dataset of 1,000 loan applicants, containing demographic and financial information such as gender, marital status, homeownership, citizenship, job qualification, loan amount, and loan duration.

The study evaluates how these variables influence the probability of loan default and compares the explanatory power and interpretability of each model. The **Probit model** achieves the best overall fit, followed closely by the Logit model.

---

## Key Results

| Model | AIC | BIC | Fit Summary |
|--------|-----|-----|-------------|
| Linear Probability | 1237.8 | 1286.9 | Weak fit; probabilities outside [0,1] |
| Logit | 1180.7 | 1224.9 | Good fit |
| **Probit** | **1180.4** | **1224.6** | Best fit overall |

**Significant predictors:**
- **Homeownership** → reduces default probability by ≈ 37-40%  
- **Foreign citizenship** → increases default risk (≈ 3.5× higher odds)  
- **Loan amount** → larger loans increase default probability  
- **Duration** → longer repayment terms slightly reduce risk  

---

## Predictive Scenarios
A highly qualified, single, foreign female borrower with a €3,000 loan over 18 months:
- **Without homeownership:** ~49% predicted default probability  
- **With homeownership:** ~37%  
→ Homeownership reduces default risk by about **12 percentage points**.

---

## Tools and Methods
- **Language:** R  
- **Key functions:** `lm()`, `glm()`, `AIC()`, `BIC()`, `predict()`  
- **Packages:** `stats`, `stargazer`, `pander`, `ggplot2`  
- **Techniques:** Binary regression, MLE, model selection, interpretability analysis

---

## Repository Structure
├── Credit-Risk-Modeling.Rmd # R Markdown script

├── credit_data.csv # Dataset

├── docs/

│ └── index.html # Knitted report (viewable online)

└── README.md


---

## How to View
For an interactive and readable report:
- View the rendered HTML file directly:  
  👉 [https://nlinh03101-art.github.io/Credit-Risk-Modelling/]

The R Markdown source file (`.Rmd`) is included for reproducibility.

---

## Author
**Ngoc Linh Dao**  
*MSc in Management, Economics and Data Science*  
Focus: Applied analytics, econometrics, and data-driven decision optimization.  
🔗 [Main Portfolio](https://github.com/nlinh03101-art/Linh_portfolio)

---

## License
This repository is shared under the **MIT License**, allowing academic and educational reuse with attribution.
