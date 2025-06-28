# Optimization-Model

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: DEEP GHEEWALA

*INTERN ID*: CT04DF578

*DOMAIN*: DATA SCIENCE

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTOSH

# 🧠 Business Optimization using Linear Programming (LP) | CodTech Internship

This repository contains **Task 4** of the CodTech Virtual Internship for Data Science. The task focuses on solving a **real-world business optimization problem** using **Linear Programming (LP)** techniques implemented in Python via the `PuLP` library. The objective is to maximize profit for an online retailer operating under limited warehouse space and product demand constraints.

---

## 📦 Problem Statement

An online retail company wants to determine the optimal number of three types of products—**Laptops**, **Headphones**, and **Keyboards**—to store in a warehouse to **maximize total profit**. Each product occupies a different amount of space and has a different profit per unit. Additionally, there are constraints on the **maximum demand** for each item and the **total available warehouse space** (100 cubic meters).

The task is to model and solve this business scenario using **linear optimization**, find the best combination of products to store, and derive actionable business insights from the solution.

---

## 📊 Data & Assumptions

The problem assumes the following product-level data:

| Product     | Space Required (m³) | Profit per Unit (₹) | Maximum Demand |
|-------------|----------------------|----------------------|----------------|
| Laptops     | 3                    | 4000                 | 20             |
| Headphones  | 1                    | 1500                 | 50             |
| Keyboards   | 2                    | 2000                 | 30             |

- Total warehouse space available: **100 m³**
- Minimum 1 unit of each product must be stored to ensure product diversity

---

## 🧮 Methodology

The problem is formulated as a **Linear Programming model** with:
- **Objective Function**: Maximize total profit = `4000x + 1500y + 2000z`
- **Decision Variables**:
  - `x`: number of Laptops to store
  - `y`: number of Headphones to store
  - `z`: number of Keyboards to store
- **Constraints**:
  - `3x + 1y + 2z ≤ 100` (total warehouse space)
  - `x ≤ 20`, `y ≤ 50`, `z ≤ 30` (demand limits)
  - `x ≥ 1`, `y ≥ 1`, `z ≥ 1` (minimum presence)

The model is solved using the **`PuLP` library**, a powerful linear optimization tool in Python. The result provides the optimal values of `x`, `y`, and `z` that maximize the profit while satisfying all constraints.

---

## 📈 Visualizations

To improve interpretability and enhance presentation, the notebook includes:

1. **A product summary table** displaying all inputs in a structured format (via `pandas`)
2. **A bar chart** (via `matplotlib`) that visually shows how many units of each product should be stored to reach maximum profitability

These additions make the notebook more insightful and help communicate the results effectively.

![Image](https://github.com/user-attachments/assets/de02f957-f952-4beb-9d42-ec67711a06fb)

---

## ✅ Results

The LP solver provided the following optimal solution:

- **Laptops to store**: 17 units  
- **Headphones to store**: 49 units  
- **Keyboards to store**: 1 unit  
- **Maximum Profit**: ₹1,41,500

This configuration utilizes the warehouse space efficiently and satisfies all constraints while yielding the **highest possible profit**.

---

## 🧠 Business Insights

- **Headphones** have the highest profit-to-space ratio, hence prioritized most.
- **Laptops**, while bulkier, contribute significantly due to their high profit.
- **Keyboards** are stored minimally to fulfill the "at least one" requirement.

This solution can help businesses plan their inventory and warehouse strategy more scientifically, making the best use of limited resources.

---

## 🚀 How to Run

1. Clone the repository or download the notebook `task_4.ipynb`
2. Make sure Python is installed with the following libraries:
   ```bash
   pip install pulp pandas matplotlib
   ```
3. Run the notebook using Jupyter or any compatible Python IDE.
