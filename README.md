# Investment-Strategy
# Investment Strategy - Monte Carlo Simulation

A Python-based Monte Carlo simulation tool for analyzing long-term investment growth scenarios. This project simulates potential investment outcomes over time using probabilistic modeling to help understand the range of possible returns.

## Overview

This simulation models investment growth by generating random annual returns based on specified mean return and volatility parameters. It runs multiple trials (Monte Carlo method) to provide statistical insights into potential investment outcomes, including mean, median, and percentile-based projections.

## Features

- **Monte Carlo Simulation**: Runs thousands of simulations to model various investment scenarios
- **Statistical Analysis**: Calculates mean, median, and percentile values (10th and 90th) for final portfolio values
- **Visualization**: Optional plotting of investment growth paths over time (requires matplotlib)
- **Configurable Parameters**: Easily adjustable investment parameters for different scenarios

## Requirements

### Required
- Python 3.x
- NumPy

### Optional
- Matplotlib (for visualization)

## Installation

1. Ensure Python 3.x is installed on your system
2. Install required dependencies:

```bash
pip install numpy
```

3. (Optional) Install matplotlib for plotting:

```bash
pip install matplotlib
```

## Usage

Simply run the script:

```bash
python Investment_Strategy.py
```

## Configuration

You can modify the following parameters in the script to customize your simulation:

- **`initial_investment`**: Starting investment amount (default: $1,000)
- **`years`**: Investment time horizon in years (default: 30)
- **`mean_return`**: Expected annual return as a decimal (default: 0.07 = 7%)
- **`volatility`**: Standard deviation of returns as a decimal (default: 0.15 = 15%)
- **`num_simulations`**: Number of Monte Carlo trials to run (default: 1,000)

### Example Parameter Adjustments

```python
initial_investment = 5000      # Start with $5,000
years = 20                     # 20-year investment horizon
mean_return = 0.08             # 8% expected annual return
volatility = 0.12              # 12% volatility (lower risk)
num_simulations = 5000         # More simulations for better accuracy
```

## Output

The script provides:

1. **Console Output**: Statistical summary including:
   - Mean final portfolio value
   - Median final portfolio value
   - 10th percentile (conservative/bad case scenario)
   - 90th percentile (optimistic/good case scenario)

2. **Visualization** (if matplotlib is installed):
   - A plot showing 100 random investment growth paths over time
   - Helps visualize the range of possible outcomes

## How It Works

1. **Random Return Generation**: For each year and each simulation, generates a random annual return based on a normal distribution with the specified mean and volatility
2. **Growth Calculation**: Applies the returns sequentially to calculate portfolio value over time
3. **Statistical Analysis**: Analyzes all simulation outcomes to compute summary statistics
4. **Visualization**: Plots sample growth paths to illustrate the variability in outcomes

## Example Output

```
After 30 years:
Mean final value: $7,612.34
Median final value: $7,234.56
10th percentile (bad case): $3,456.78
90th percentile (good case): $12,345.67
```

## Notes

- The simulation assumes returns follow a normal distribution, which is a simplification of real market behavior
- Past performance does not guarantee future results - this is a modeling tool, not financial advice
- Consider adjusting parameters based on your risk tolerance and investment goals
- Higher volatility increases the range of possible outcomes (both positive and negative)

## License

This project is provided as-is for educational and personal use.

