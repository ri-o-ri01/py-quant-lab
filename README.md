# py-quant-lab

**A flexible experimental lab for quantitative finance.**

---

## 📌 Overview
Ctrl + K V
`py-quant-lab` is a Python framework designed for **prototyping and verifying various pricing models** used in quantitative finance.  
It is structured to handle:

- ✅ **Flexible path generation** (GBM, Heston, Jump Diffusion, etc.)
- ✅ **Backward induction methods** like **LSM** (Longstaff-Schwartz)
- ✅ **Cash flow generation** for diverse derivatives (American, Barrier, Asian, etc.)
- ✅ **Analytical solutions and finite difference methods** for convergence checks
- ✅ **Easy extension and refactoring** — it’s a **lab**, so re-designs are encouraged!

---

## 🏗️ Architecture

This lab organizes its core logic by clearly separating **three main responsibilities** for maintainability and flexibility:

| Component | Responsibility |
| --- | --- |
| **Path Generation** | Generates asset price paths in a vectorized way. |
| **Continuation Value Estimation** | Estimates continuation values using regression methods such as LSM or neural networks. |
| **Cash Flow Calculation** | Computes product-specific cash flows based on paths and estimated continuation values. |
| **Engine / Orchestrator** | Integrates the above components and runs the full pricing workflow. |

---