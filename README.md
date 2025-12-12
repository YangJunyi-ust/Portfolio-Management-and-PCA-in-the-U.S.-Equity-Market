# Portfolio-Management-and-PCA-in-the-U.S.-Equity-Market
Portfolio Management and Systemic Risk Monitoring via Principal Component Analysis in the U.S. Equity Market 
# Portfolio-Management-and-PCA-in-the-U.S.-Equity-Market
Portfolio Management and Systemic Risk Monitoring via Principal Component Analysis in the U.S. Equity Market 

---

## 📖 Project Overview
We investigate how **Principal Component Analysis (PCA)** can be applied to:
- **Systemic risk monitoring**: Using the variance explained by the first principal component (PC1) as a proxy for market-wide co-movement.
- **Portfolio construction**: Building orthogonal principal portfolios and testing allocation strategies against benchmarks.

By integrating **Yahoo Finance (yfinance)** data with **WRDS CRSP** records, we mitigate survivorship bias and capture the true investment universe across multiple regimes.

---

## ⚙️ Methodology
- **Data**: Daily adjusted returns for S&P 500 constituents (2010–2025).
- **Rolling PCA**: 2-year window, weekly step.
- **Systemic Risk Indicator**: PC1 variance spikes during crises (COVID-19 crash, 2022 bear market).
- **Allocation Strategies**:
  - Equal-weight across stocks
  - Equal-weight across principal portfolios
  - Risk-parity variants
- **Dimensionality Reduction**: Jolliffe’s backward deletion (thresholds 0.7–0.1).
- **Industry Exposure**: PCA portfolios tilt toward defensive sectors, underweight technology and financials.

---

## 📊 Key Results
- **Systemic Risk**: PC1 variance averaged ~25%, peaking at 41% during COVID-19.
- **Performance**: PCA portfolios reduce volatility and drawdowns but sacrifice upside returns.
- **Stock Selection**:
  - Threshold 0.2 → 108 stocks, correlation 0.9720, tracking error 4.86%.
  - Threshold 0.1 → 199 stocks, correlation 0.9836, tracking error 3.75%.
- **Dynamic WRDS Selection**: Adaptive pruning yields strong fidelity (correlation 0.9733, tracking error 2.67%).
- **Industry Biases**: Overweight consumer defensive, underweight tech/financials → resembles low-volatility or quality factors.

---

## 📂 Repository Structure
- `data/` – Processed datasets (yfinance + WRDS)
- `codes/` – PCA implementation, rolling analysis, and backtests
- `images/` – Charts and plots (systemic risk indicator, stock selection validation, industry exposure)
- `README.md` – Project overview

---

## 📚 Reference
Jolliffe, I. T. (2002). *Principal Component Analysis* (2nd ed.). Springer.

---

## 🔗 Data Availability
- Yahoo Finance via [yfinance](https://pypi.org/project/yfinance/)
- WRDS CRSP & Compustat (institutional access required)
- Fama–French factors via [Kenneth R. French Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)

---

## 👩‍💻 Authors
- **Fuxian Zhao**, HKUST  
- **Junyi Yang**, HKUST
