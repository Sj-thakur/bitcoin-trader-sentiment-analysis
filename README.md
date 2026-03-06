# Bitcoin Trader Behavior vs Market Sentiment

## Overview

This project analyzes how **Bitcoin market sentiment (Fear vs Greed)** affects trader behavior and performance using historical trading data and the Fear & Greed Index.

The goal is to identify patterns in trader performance, leverage usage, trade sizes, and profitability under different market sentiment conditions.

---

# Dataset

Two datasets were used:

### 1️⃣ Fear & Greed Index

Contains daily Bitcoin sentiment classification.

Columns:

* Date
* Classification (Fear / Neutral / Greed)

### 2️⃣ Historical Trader Data

Contains trading activity from Hyperliquid.

Key fields:

* account
* symbol
* execution price
* size
* side
* time
* closedPnL
* leverage

---

# Methodology

1. **Data Cleaning**

   * Converted timestamps
   * Merged sentiment data with trading records

2. **Feature Engineering**

   * Trade size in USD
   * Win/Loss classification
   * Long vs Short positions
   * Sentiment encoding

3. **Exploratory Analysis**

   * Win rate by sentiment
   * Mean PnL by sentiment
   * Trade size distribution
   * Leverage analysis
   * Long/Short behavior
   * Daily trading activity

4. **Segment Analysis**
   Traders segmented into:

   * High leverage
   * Low leverage

5. **Machine Learning Model**

   * Model: Random Forest Classifier
   * Task: Predict profitable trades
   * Metrics: Confusion matrix & feature importance

---

# Key Insights

### 1️⃣ Traders perform best during **Greed markets**

* Highest mean PnL per trade

### 2️⃣ Fear markets still produce strong profitability

* Lower win rate but larger gains

### 3️⃣ Neutral markets show lowest trading activity

* Reduced opportunity and smaller profits

### 4️⃣ Low leverage traders outperform high leverage traders

* Higher mean PnL
* Better win consistency

### 5️⃣ Most important predictive features

1. Historical account win rate
2. Fear & Greed score
3. Coin trading frequency
4. Leverage

---

# Visualizations

The analysis includes:

* Trader performance by sentiment
* Trade size distributions
* Trading behavior patterns
* Leverage analysis
* Cumulative profitability over time
* Segment performance heatmaps
* ML model evaluation

All figures are stored in the **outputs/** directory.

---


# Project Structure

```
data/        -> datasets
notebooks/   -> analysis notebook
outputs/     -> visualizations
dashboard/   -> Streamlit dashboard
```

---

# Author

Shivam Jadon
B.Tech CSE
Data Science Enthusiast
