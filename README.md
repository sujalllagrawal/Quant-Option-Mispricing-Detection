

# Overview

This project is a quantitative options analytics system that identifies potentially mispriced options by comparing **live market prices** with **Black-Scholes theoretical prices** and validating the results using **historical volatility** and **statistical analysis**.

The application fetches live option chain data from the **Upstox API**, extracts option Greeks, computes theoretical option prices using the Black-Scholes model, compares them with market prices, analyzes historical volatility using Yahoo Finance, and generates quantitative trading signals.

---

# Key Features

## Live Market Data

- Live Option Chain using Upstox API
- User-selected Stock/Index
- User-selected Expiry Date
- Automatic ATM Strike Detection
- ATM + OTM Option Filtering

---

## Option Analytics

- Black-Scholes Fair Price Calculation
- Market Price Comparison
- Mispricing Percentage
- Overvalued / Undervalued Detection

---

## Greeks Extraction

The project extracts the following option Greeks:

- Delta
- Gamma
- Theta
- Vega
- Implied Volatility (IV)

---

## Volatility Analysis

Historical price data is downloaded using Yahoo Finance.

The project calculates:

- Daily Returns
- 20-Day Historical Volatility
- Historical Volatility Distribution
- Mean Historical Volatility
- Standard Deviation
- Z-Score
- 95% Confidence Interval

---

## Statistical Decision Framework

Current Implied Volatility

↓

Historical Volatility

↓

Statistical Analysis

↓

Quantitative Trading Signal

---

# Project Workflow

```text
User Input
      │
      ▼
Select Stock / Index
      │
      ▼
Select Expiry
      │
      ▼
Download Live Option Chain
      │
      ▼
Detect ATM Strike
      │
      ▼
Filter ATM + OTM Options
      │
      ▼
Extract Greeks
      │
      ▼
Black-Scholes Pricing
      │
      ▼
Calculate Fair Price
      │
      ▼
Calculate Mispricing %
      │
      ▼
Download Historical Data
      │
      ▼
Calculate Historical Volatility
      │
      ▼
Generate Volatility Distribution
      │
      ▼
Calculate Z-Score
      │
      ▼
Generate Quantitative Signal
```

---

# Mathematical Methodology

## Black-Scholes Model

The theoretical option price is calculated using the following inputs:

| Symbol | Description |
|---------|-------------|
| S | Spot Price |
| K | Strike Price |
| T | Time to Expiry |
| r | Risk-Free Interest Rate |
| σ | Implied Volatility |

The theoretical value is compared against the live market price to estimate option mispricing.

---

# Statistical Analysis

The project performs statistical analysis on historical volatility by computing:

- Rolling 20-Day Historical Volatility
- Mean Historical Volatility
- Standard Deviation
- Z-Score
- 95% Confidence Interval

Current Implied Volatility is then compared against this historical distribution to determine whether market volatility is relatively cheap or expensive.

---

# Sample Output

 <img width="575" height="211" alt="Screenshot 2026-06-19 134802" src="https://github.com/user-attachments/assets/9c2500b0-b279-4358-95bf-acc619e61bfe" />

    
   
---

# Visualizations

The project generates the following visualizations:

- Historical Volatility Histogram
- Volatility Distribution
- Current Implied Volatility Position
- 95% Confidence Interval Visualization

---

# Repository Structure

```text
Quantitative-Option-Mispricing-Analysis/

│── Quant_Option_Mispricing.ipynb
│── README.md
│── requirements.txt
│── LICENSE

├── images/
│     histogram.png
│     normal_distribution.png
│     scanner_output.png

├── output/
│     final_output.csv
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Requests
- SciPy
- Matplotlib
- py_vollib
- Upstox API
- Yahoo Finance

---

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```text
Quant_Option_Mispricing.ipynb
```

---

# Results

The project successfully:

- Retrieved live option chain data from Upstox API.
- Automatically detected the At-The-Money (ATM) strike.
- Filtered ATM and Out-of-the-Money (OTM) option contracts.
- Extracted option Greeks for quantitative analysis.
- Calculated theoretical prices using the Black-Scholes model.
- Identified overvalued and undervalued options.
- Computed historical volatility using Yahoo Finance.
- Compared implied volatility with historical realized volatility.
- Performed statistical analysis using Z-Scores and confidence intervals.
- Generated quantitative trading signals.

---

# Screenshots

## Option Scanner


 <img width="575" height="211" alt="Screenshot 2026-06-19 134802" src="https://github.com/user-attachments/assets/53366627-31b8-4d62-bfed-c8ac290d57aa" />

---

## Historical Volatility Distribution


<img width="1980" height="1499" alt="histogram" src="https://github.com/user-attachments/assets/cf1d8c0b-bebf-4477-bb94-365dc89f0b8a" />


---

## Statistical Volatility Analysis

  <img width="1980" height="1499" alt="normal_distribution" src="https://github.com/user-attachments/assets/344a8b1b-480e-4e05-a90e-680d93f7c4d0" />


---

# Limitations

Current version limitations include:

- Black-Scholes assumptions (constant volatility and European-style options).
- Historical volatility is calculated using daily closing prices.
- Trading signals are rule-based and are not yet validated through predictive machine learning.

---

# Future Improvements

Planned enhancements include:

- Machine Learning-based Volatility Forecasting
- Random Forest
- XGBoost
- LightGBM
- Intraday Option Chain Collection
- Volatility Surface Construction
- IV Smile Analysis
- Backtesting Engine
- Streamlit Dashboard
- Real-Time Trading Alerts

---

# Skills Demonstrated

This project demonstrates practical experience in:

- Quantitative Finance
- Options Pricing
- Black-Scholes Model
- Statistical Analysis
- Volatility Modeling
- Python Programming
- Financial Data Analysis
- REST API Integration
- Data Visualization

---

# Author

**Sujal Agrawal**

B.Tech, Electrical Engineering  
Malaviya National Institute of Technology (MNIT) Jaipur

### Areas of Interest

- Quantitative Research
- Options & Derivatives
- Algorithmic Trading
- Machine Learning in Finance
- Statistical Modeling
- Financial Engineering

---

# License

This project is licensed under the MIT License.
