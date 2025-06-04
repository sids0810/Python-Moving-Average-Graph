# Financial Market Data Analysis Toolkit: Part 1 - Stock Price & Moving Average Visualizer

**Author:** Siddhant Dhoot
**Date:** June 2, 2025 
**Project Version:** 1.0

## Description

This Python project, implemented in a Jupyter Notebook, provides a toolkit for fetching, analyzing, and visualizing historical stock market data. Specifically, this "Part 1" focuses on:

* Fetching historical daily stock price data for a user-specified ticker symbol and date range using the `yfinance` library.
* Calculating two key technical indicators: the 50-day Simple Moving Average (SMA) and the 200-day Simple Moving Average (SMA) using the `pandas` library.
* Visualizing the stock's closing price alongside these SMAs on a time-series plot using `matplotlib`, allowing for trend identification and analysis.

The notebook is structured to guide the user through the process, from inputting parameters to viewing the final visualization. It also demonstrates how to adjust the data fetching period to ensure accurate calculation of moving averages from the desired start date of analysis.

## Features

* User-defined stock ticker, analysis start date, and end date.
* Automatic adjustment of data fetching window to ensure sufficient historical data for SMA calculation.
* Robust data fetching via Yahoo Finance (`yfinance`).
* Clear calculation of 50-day and 200-day SMAs.
* Clean and informative plot showing:
    * Daily Closing Prices
    * 50-day SMA
    * 200-day SMA

## Technologies & Libraries Used

* **Python 3**
* **Jupyter Notebook**
* **`yfinance`**: For downloading historical market data from Yahoo Finance.
* **`pandas`**: For data manipulation, time-series analysis, and calculating moving averages.
* **`matplotlib.pyplot`**: For creating static, animated, and interactive visualizations.
* **`datetime`**: For handling date and time objects.

## How to Run This Project

1.  **Prerequisites:**
    * Ensure you have Python 3 installed on your system.
    * It's recommended to use a virtual environment.

2.  **Install Necessary Libraries:**
    Open your terminal or command prompt and install the required libraries if you haven't already:
    ```bash
    pip install yfinance pandas matplotlib jupyterlab
    ```

3.  **Obtain the Notebook:**
    * If this project is cloned from a Git repository, navigate to the project folder.
    * Otherwise, ensure the `.ipynb` notebook file is in your desired working directory.

4.  **Launch Jupyter:**
    In your terminal, navigate to the project directory and launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    ```
    or
    ```bash
    jupyter lab
    ```

5.  **Open and Run the Notebook:**
    * In the Jupyter interface that opens in your web browser, find and open the notebook file (e.g., `moving_average_graph.ipynb`).
    * You can modify the `input_stock`, `start_date`, and `end_date` variables in the relevant code cell to analyze different stocks or time periods.
    * Run the cells sequentially (e.g., by selecting a cell and pressing `Shift + Enter`, or using the "Run" menu).

## Example Output

The script will generate a line chart visualizing the stock's closing price, its 50-day SMA, and its 200-day SMA over the specified time period. An example for a given stock (e.g., "GS" or "JPM" as seen in development) would show these three lines plotted against time.

## Practical Uses of This Code

This toolkit, even in its current "Part 1" stage, has several practical applications for individuals interested in financial markets, learning data analysis, or developing trading strategies:

1.  **Trend Identification:**
    * **Visualizing Trends:** Moving averages help smooth out price data to identify the underlying trend direction (uptrend, downtrend, or sideways). The 50-day SMA shows the medium-term trend, while the 200-day SMA indicates the long-term trend.
    * **Support and Resistance:** SMAs can act as dynamic levels of support (in an uptrend) or resistance (in a downtrend). Traders often watch how price interacts with these levels.

2.  **Generating Trading Signals (Basic):**
    * **Moving Average Crossovers:** A common strategy involves looking for crossovers:
        * **Golden Cross:** When the 50-day SMA crosses above the 200-day SMA, it's often considered a bullish signal.
        * **Death Cross:** When the 50-day SMA crosses below the 200-day SMA, it's often considered a bearish signal.
    * **Price vs. SMA Crossovers:** When the price crosses above an SMA, it can be a buy signal; when it crosses below, it can be a sell signal (though these are very basic and often used with other indicators).

3.  **Understanding Market Sentiment:**
    * The relationship between the price and its long-term moving averages (like the 200-day SMA) is often used as a gauge of overall market sentiment for a particular stock. A stock consistently trading above its 200-day SMA is generally viewed as being in a healthy long-term uptrend.

4.  **Educational Tool:**
    * Provides a hands-on way to learn about stock market data, technical indicators, and data visualization using Python.
    * Serves as a foundational script that can be expanded with more complex indicators, analysis techniques, or even backtesting capabilities.

5.  **Portfolio Monitoring (Basic):**
    * Investors can quickly visualize the trend health of stocks in their portfolio.

6.  **Foundation for More Complex Analysis:**
    * This script can be the starting point for adding other technical indicators (RSI, MACD, Bollinger Bands), volatility analysis, or correlation studies with other assets.

## Future Enhancements (Ideas for "Part 2" and beyond)

* Add more technical indicators.
* Implement interactive plots (e.g., using `plotly` or `bokeh`).
* Allow for comparison of multiple stocks on the same chart.
* Incorporate volume data into the analysis.
* Develop a simple backtesting framework for SMA crossover strategies.

