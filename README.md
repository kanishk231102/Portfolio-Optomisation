Here's a sample README file for your project:

---

# Portfolio Optimization and Analysis

This project is designed to perform portfolio optimization and analysis using historical stock data. It downloads data for selected tickers, calculates important financial metrics, optimizes the portfolio based on the Sharpe ratio, and visualizes the results.

## Features

- Download historical stock data for specified tickers
- Calculate log returns and covariance matrix
- Optimize the portfolio to maximize the Sharpe ratio
- Visualize the optimal portfolio weights
- Plot high and low prices per year
- Display hypothetical returns on an initial investment

## Requirements

To run this project, you need the following Python packages:

- `yfinance`
- `pandas`
- `numpy`
- `scipy`
- `fredapi`
- `matplotlib`
- `certifi`
- `ssl`

You can install these packages using pip:

```bash
pip install yfinance pandas numpy scipy fredapi matplotlib certifi
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/portfolio-optimization.git
cd portfolio-optimization
```

2. Run the script:

```bash
python portfolio_optimization.py
```

## Project Structure

- `portfolio_optimization.py`: The main script that performs the analysis and optimization.
- `requirements.txt`: The list of required packages.

## Explanation of the Script

### Imports

The script imports necessary libraries for data download, manipulation, and visualization.

### Configuration

SSL context is configured to use certifi's bundle to avoid SSL certificate verification issues.

### Data Download

The script defines tickers and a time range, then downloads adjusted close prices, high prices, and low prices for the specified tickers.

### Calculations

- **Log Returns**: The script calculates log-normal returns for each ticker.
- **Covariance Matrix**: The covariance matrix of the returns is calculated.
- **Performance Metrics**: Functions are defined to calculate standard deviation, expected return, and the Sharpe ratio.
- **Risk-Free Rate**: The script fetches the 10-year Treasury rate from the FRED API and uses it as the risk-free rate.

### Optimization

The portfolio is optimized by minimizing the negative Sharpe ratio using the `scipy.optimize.minimize` function.

### Visualization

- **Optimal Portfolio Weights**: The script plots the optimized portfolio weights.
- **Annual High and Low Prices**: The script plots the high and low prices per year for each ticker.
- **Hypothetical Investment Returns**: The script calculates and plots the hypothetical return on a $1000 investment over the specified period.

### Example Output

- Optimal weights for each asset in the portfolio
- Annual high and low prices for each asset
- Hypothetical growth of a $1000 investment over 5 years

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License.

## Contact

If you have any questions or feedback, feel free to contact me at kanishkpareek80@gmail.com .

