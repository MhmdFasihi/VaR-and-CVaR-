# VaR-and-CVaR-
Calculating VaR and CVaR with 3 methods of historical, parametric, and monte carlo
Sure! Here is a detailed and comprehensive `README.md` file for your GitHub repository:

---

# VaR and CVaR Calculation for Cryptocurrencies

This repository contains a Python script to calculate Value at Risk (VaR) and Conditional Value at Risk (CVaR) for cryptocurrencies. The script allows you to choose between different calculation methods (historical, parametric, Monte Carlo) and time frequencies (daily, weekly, monthly).

## Features

- Fetch historical price data for a specified cryptocurrency.
- Calculate log returns based on daily, weekly, or monthly frequencies.
- Compute VaR and CVaR using:
  - Historical Method
  - Parametric Method
  - Monte Carlo Simulation
- Visualize the log returns and the distribution of returns with VaR and CVaR thresholds.
- Supports different confidence levels (e.g., 95%, 99%).

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/crypto-var-cvar.git
   cd crypto-var-cvar
   ```

2. **Install the required packages:**
   ```
   pandas
   numpy
   matplotlib
   yfinance
   scipy
   ```

## Usage

1. **Modify User Inputs:**
   Edit the `main()` function in the script to specify the cryptocurrency ticker, start and end dates, frequency, confidence level, and calculation method:
   ```python
   ticker = 'BTC-USD'  # Ticker for Bitcoin
   start_date = '2019-01-01'  # Start date for data retrieval
   end_date = '2023-01-01'  # End date for data retrieval
   frequency = 'daily'  # Options: 'daily', 'weekly', 'monthly'
   confidence_level = 95  # Options: 95, 99
   method = 'historical'  # Options: 'historical', 'parametric', 'monte carlo'
   ```

2. **Run the script:**
   ```bash
   python crypto_var_cvar.py
   ```

3. **Output:**
   The script will print the calculated VaR and CVaR values and display visualizations of the log returns and the return distribution with VaR and CVaR thresholds.

## Example Output

```
Data for BTC-USD from 2019-01-01 to 2023-01-01 with daily frequency:
         Adj Close
count  1439.000000
mean   120.456781
std    0.054321
min    -0.097654
25%    0.012345
50%    0.034567
75%    0.056789
max    0.123456

Daily VaR and CVaR for BTC-USD at 95% confidence level using Historical method:
VaR: 0.0344
CVaR: 0.0398
```


## Methods

### Historical Method
Uses historical returns to calculate the VaR and CVaR. It sorts the returns and uses the percentile values to compute the risk measures.

### Parametric Method
Assumes returns follow a normal distribution and uses the mean and standard deviation to calculate VaR and CVaR.

### Monte Carlo Simulation
Generates simulated returns based on the historical mean and standard deviation and uses these simulations to calculate VaR and CVaR.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.
