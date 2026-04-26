# ACC102 Mini Project: Tech Stock Risk-Return Analysis
---

## 1. Project Overview & Problem Statement
### What problem are we solving?
Investors often face difficulty comparing the performance and risk profiles of different stocks, especially when dealing with multi-decade historical data. They need clear, data-driven insights to make informed decisions aligned with their risk tolerance.

This project addresses this need by analyzing three major U.S. technology stocks (AAPL, GOOGL, MSFT) to answer:
- Which stock delivered the highest long-term returns?
- Which stock carries the most/least risk (volatility)?
- How do these stocks correlate with each other?
- What investment recommendations can be derived for different types of investors?

### Who is this for?
This analysis is designed for:
- Beginner investors looking to understand risk-return tradeoffs in tech stocks
- Anyone interested in comparing the historical performance of top tech companies

---

## 2. Data Description
### Data Sources
We use historical daily stock price data for three tech giants:
- **Apple Inc. (AAPL)**: Daily OHLC (Open/High/Low/Close) prices, volume, spanning decades
- **Alphabet Inc. (GOOGL)**: Daily OHLC prices, volume, including adjusted close prices
- **Microsoft Corp. (MSFT)**: Daily OHLC prices, volume, with complete historical records

### Key Data Fields
- `Date`: Trading date
- `Open/High/Low/Close`: Daily price range and closing price
- `Adj Close`: Adjusted closing price (for GOOGL)
- `Volume`: Daily trading volume

---

## 3. Analysis Workflow & Methods
The project follows a complete data analysis pipeline:

### Step 1: Data Acquisition
- Sourced historical daily stock price data from reliable financial data platforms
- Collected datasets for AAPL, GOOGL, and MSFT covering their respective listing periods
- Stored data in CSV format for easy processing

### Step 2: Data Cleaning
- Standardized column names across all datasets
- Removed invalid values (e.g., dollar signs in price columns)
- Handled missing dates and outliers
- Calculated daily returns using adjusted closing prices

### Step 3: Key Metrics Calculation
We computed three core financial indicators:
1.  **Daily Return**: `(Today's Close / Previous Close) - 1`
2.  **Cumulative Return**: `(1 + Daily Return).prod() - 1` (total return over the period)
3.  **Annualized Volatility**: `Daily Return.std() * sqrt(252)` (risk measure)

### Step 4: Visualization
Generated charts to illustrate trends and patterns:
1.  Stock Price Trend Comparison
2.  Cumulative Return Comparison
3.  Annualized Volatility Bar Chart
4.  Daily Return Distribution Histograms
5.  30-Day Rolling Volatility
6.  Return Correlation Heatmap

### Step 5: Investment Recommendations
Based on the metrics, we generated tailored advice for different investor profiles:
- Growth-focused investors
- Risk-averse investors
- Balanced investors

---

## 4. Key Findings & Insights
### Risk-Return Summary
| Ticker   | Cumulative Return | Annualized Volatility |
|----------|-------------------|-----------------------|
| AAPL     | 8.4397            | 0.2895                |
| GOOGL    | 80.0241           | 0.3066                |
| MSFT     | 3917.7023         | 0.3307                |

### Main Takeaways
1.  **Long-Term Growth**: MSFT delivered the highest cumulative return (over 3900x), reflecting its decades of growth in the tech sector.
2.  **Risk Profile**: AAPL is the most stable with the lowest volatility, while MSFT and GOOGL show higher price swings.
3.  **Correlation**: All three stocks are highly positively correlated, meaning they tend to move in tandem due to common sector-wide factors.
4.  **Risk-Return Tradeoff**: MSFT offers the highest potential returns but comes with the highest risk, while AAPL provides a balanced mix of growth and stability.

---

## 5. How to Run This Project
### Prerequisites
- Python 3.8+
- Required libraries: `pandas`, `matplotlib`, `numpy`

### Steps to Run
1.  Clone this repository to your local machine
2.  Place your CSV data files in the project directory
3.  Open the Jupyter Notebook file (`ACC102_Stock_Analysis.ipynb`)
4.  Run the cells in order from top to bottom
5.  The charts and metrics table will be generated automatically

---

## 6. Product Link
The complete analysis, including the full code, data, and generated outputs, is available in this GitHub repository:
[GitHub Repository](https://github.com/your-username/ACC102-Miniwork)

---

## 7. Limitations & Future Work
### Limitations
- The analysis only considers historical price data and does not incorporate fundamental factors like earnings, debt, or market sentiment.
- The correlation analysis does not account for external macroeconomic shocks that may affect different stocks differently.
- Recommendations are based on simplified metrics and do not replace professional financial advice.

### Future Work
- Incorporate additional fundamental data (e.g., P/E ratio, revenue growth) for a more holistic view.
- Extend the analysis to include portfolio optimization to find the optimal mix of these three stocks.
- Add real-time data fetching functionality to update the analysis with the latest market data.

---

## Product Link
https://github.com/yutongpeng777/ACC102-Miniwork--Tech-Stock-Market-Performance-Analyzer
---

## License
This project is for educational purposes only.
