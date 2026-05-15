# Investment Portfolio Analyzer

Investment Portfolio Analyzer is a Python-based project for analyzing the profitability of an investment portfolio and comparing its performance against the Ibovespa benchmark index (`^BVSP`).

The project reads portfolio allocation data from a text file, retrieves historical market prices from Yahoo Finance, calculates individual asset returns, estimates the portfolio’s overall performance, and compares the result with the Brazilian stock market benchmark.

> This project is intended for educational and portfolio purposes. It does not provide financial advice or investment recommendations.

---

## Overview

This project automates a basic investment portfolio performance analysis workflow.

The application uses a portfolio input file containing asset tickers and invested values. Based on this data, it retrieves historical price information, calculates asset-level profitability, computes the weighted portfolio return, and compares the final result with the Ibovespa index.

The goal is to provide a simple and practical way to understand how a portfolio performed over a selected period.

---

## Features

- Reads portfolio data from a `carteira.txt` file
- Structures assets and invested values for analysis
- Retrieves historical price data from Yahoo Finance
- Calculates individual asset returns
- Calculates total portfolio profitability based on asset weights
- Compares portfolio performance against the Ibovespa index (`^BVSP`)
- Displays the initial and final portfolio values
- Shows portfolio and benchmark returns in percentage format
- Indicates whether the portfolio outperformed, matched, or underperformed the benchmark

---

## Tech Stack

- **Python**
- **pandas**
- **yfinance**
- **datetime**

---

## How It Works

The project follows a simple portfolio analysis flow:

1. **Portfolio Input**

   The application reads asset tickers and invested values from a `carteira.txt` file.

2. **Portfolio Structuring**

   The input data is organized into a dictionary where:

   - the key represents the asset ticker;
   - the value represents the initial amount invested.

3. **Market Data Retrieval**

   Historical adjusted prices are collected from Yahoo Finance for:

   - each portfolio asset;
   - the Ibovespa benchmark index (`^BVSP`).

4. **Return Calculation**

   The project calculates the return of each asset based on its initial and final prices during the selected period.

5. **Portfolio Performance Calculation**

   The total portfolio return is calculated using the weight of each asset and its respective performance.

6. **Benchmark Comparison**

   The portfolio return is compared against the Ibovespa return for the same period.

7. **Result Output**

   The application displays the portfolio’s initial value, final value, percentage return, benchmark return, and relative performance.

---

## Input File

The project expects a file named:

```text
carteira.txt
```

This file should contain the portfolio assets and their respective invested values.

Example format:

```text
PETR4.SA - 1000
VALE3.SA - 1500
ITUB4.SA - 1200
```

> Adjust the tickers according to the format supported by Yahoo Finance.

---

## Project Structure

Based on the current project proposal, the expected structure is:

```text
investment-portfolio-analyzer/
├── README.md
├── carteira.txt
└── main.py
```

### Main Files

- `README.md`  
  Project documentation.

- `carteira.txt`  
  Input file containing asset tickers and invested values.

- `main.py`  
  Python script responsible for reading the portfolio, retrieving market data, calculating returns, and displaying the final comparison.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/lucaspc6/investment-portfolio-analyzer.git
```

Access the project directory:

```bash
cd investment-portfolio-analyzer
```

Install the required Python libraries:

```bash
pip install pandas yfinance
```

---

## Running the Project

After configuring the `carteira.txt` file, run the Python script responsible for the analysis:

```bash
python main.py
```

> If the main script has a different filename in your local version, replace `main.py` with the correct file name.

---

## Example Output

The project is expected to display results similar to:

```text
Initial portfolio value: R$ 3,700.00
Final portfolio value: R$ 4,120.00

Portfolio return: 11.35%
Ibovespa return: 8.42%

Result: The portfolio outperformed the Ibovespa index.
```

---

## Financial Disclaimer

This project is for educational and portfolio demonstration purposes only.

It does not provide:

- investment recommendations;
- financial advice;
- buy or sell signals;
- risk assessment;
- portfolio optimization;
- guaranteed return projections.

Past performance does not guarantee future results. Market data may be incomplete, delayed, unavailable, or inaccurate depending on the data provider.

---

## Limitations

- The analysis depends on Yahoo Finance data availability.
- The project does not account for taxes, brokerage fees, dividends, inflation, or currency conversion.
- The project focuses on historical profitability, not risk-adjusted return.
- The project does not perform portfolio optimization.
- The project does not provide investment recommendations.

---

## Future Improvements

Potential improvements for this project include:

- Add a sample `carteira.txt` file
- Add charts comparing portfolio performance against Ibovespa
- Add error handling for unavailable tickers
- Add support for custom analysis dates
- Add dividend-adjusted analysis
- Add automated tests for return calculations
- Add a `requirements.txt` file
- Improve project structure by separating data loading, market data retrieval, calculation, and reporting logic

---

## Author

**Lucas Carvalho**

GitHub: [@lucaspc6](https://github.com/lucaspc6/)
