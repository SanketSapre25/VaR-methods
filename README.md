# VaR-methods
Value At Risk Simulator

## Purpose

This repository explores multiple methodologies to measure and visualize **Value at Risk (VaR)** for a portfolio of simulated financial instruments. It showcases how a risk consultant can develop transparent and modular risk engines across:

- Historical (Quantile) VaR
- Conditional VaR (Expected Shortfall)
- Stressed VaR (Worst rolling window)
- Variance-Covariance (Parametric) VaR
- Monte Carlo Simulation-Based VaR (optional extension)

Each method is visualized and explained using Python, offering both conceptual clarity and hands-on illustration of risk modeling best practices.

---

## Why This Project Matters

In practice, VaR isn’t about a single number — it’s a **layered view of risk**. By comparing methodologies side-by-side, this project provides insight into:

- The shape and tail behavior of return distributions  
- Where parametric simplifications might understate tail risk  
- How stressed periods amplify risk beyond normal expectations  
- The power of visualizing these thresholds for stakeholder communication

  This project reflects my continued investment in upskilling and translating real-world experience into open, explainable tools for the risk, treasury, and RegTech space. Also, this would help me lay the foundation for future Product Leadership in Risk Technology.
---

## Included Models

| Method | Description | Confidence |
|--------|-------------|------------|
| **Historical VaR** | Uses empirical quantiles from portfolio returns | 99% |
| **Expected Shortfall (CVaR)** | Averages losses beyond VaR threshold — tail damage | 99% |
| **Stressed VaR** | Finds maximum VaR over worst-case rolling window (e.g. 60 days) | 99% |
| **Variance-Covariance VaR** | Uses analytical formula: portfolio volatility × Z-score × √t | 95% / 99% |

---

## Visual Output

The notebook plots include:

- Return histogram of the portfolio  
- Red line: Historical VaR  
- Orange line: Expected Shortfall  
- Navy line: Stressed VaR
  ![Portfolio Return Distribution with VaR Layers](https://github.com/user-attachments/assets/e3a09f81-36df-43fb-aaa1-7b805800e606)


- Parametric VaR values printed with analytical derivation
![Parametric Simulation Based VaR](https://github.com/user-attachments/assets/89f8ee2a-8e69-4454-9699-0ce14b81041c)

---

## Tech Stack

- Python: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`
- Jupyter Notebook format (`.ipynb`)
- Class-based or modular design for extensibility

---

## How to Use

1. Clone the repo  
2. Launch `Portfolio_VaR_Layers.ipynb`  
3. Run through each section:
    - Simulate or load returns
    - Apply chosen VaR method(s)
    - View overlayed chart with each risk metric
4. Adjust confidence levels, window size, portfolio weights, or volatility assumptions

---

## Author

[Sanket Sapre](https://www.linkedin.com/in/sanket-sapre-483a102a/), a Senior Consutant in Model Risk and Regulatory Reporting, currently upskilling into Risk Data Product Management. This project is part of a broader portfolio of open prototypes aimed at modernizing capital and treasury risk workflows through product-led thinking.

---

## Next Steps

- Integrate real asset return data via `yfinance` or API
- Layer in liquidity-adjusted VaR or IMA/FRTB metrics
