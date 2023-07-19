# QuantumFinance

This repository contains code to estimate European call option prices using quantum computing techniques. We utilize Qiskit, a quantum computing SDK, and related libraries to perform quantum amplitude estimation for pricing options.

Table of Contents

- Introduction
- Installation
- Usage
- Results
- License

Introduction

A European call option is a financial contract that grants the holder the right, but not the obligation, to buy an underlying asset (usually a stock) at a predetermined strike price on or before the option's expiration date. Estimating the fair price of a European call option is essential for investors and traders in the financial market.

This project aims to estimate the fair prices of European call options using quantum computing techniques. The estimation algorithm leverages Qiskit and related components to implement quantum circuits representing the option's payoff function and apply amplitude estimation to find the expected value.

Installation

To run the code in this repository, ensure you have the following prerequisites:

1. Python 3.x
2. Qiskit SDK (with all required dependencies)
3. Jupyter Notebook or any Python IDE

To install Qiskit and other dependencies, you can use pip:

pip install qiskit matplotlib pandas numpy

Additionally, you'll need to set up your IBM Quantum account credentials if you plan to use IBM Quantum devices for computation.

Usage

In this repository, we provide a Python script that estimates European call option prices using quantum amplitude estimation. The script is located in the main directory.

Here's a brief overview of the key components of the script:

1. Quantum Circuit Construction: The script constructs a quantum circuit representing the payoff function of a European call option. This involves defining a log-normal distribution for the underlying asset's price and a piecewise linear objective function for the option's payoff.

2. Amplitude Estimation: The constructed quantum circuit is used as input to the quantum amplitude estimation algorithm provided by Qiskit. This algorithm estimates the expected value of the payoff function, which corresponds to the fair price of the European call option.

3. Estimation and Sampling: The script then randomly samples European call option parameters (e.g., spot price, volatility, interest rate, maturity) and performs quantum amplitude estimation for each sample to estimate the fair price.

4. Data Visualization: The resulting estimated fair prices and the corresponding true fair prices are plotted on a graph. The closer the estimated prices are to the true prices, the more accurate the quantum estimation.

Results

After running the script, you should see a graph showing the scatter plot of estimated fair prices against the true fair prices. Ideally, the points on the graph should align closely along a straight line, indicating that the quantum estimates are accurate.

Additionally, the script calculates and prints the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) between the estimated fair prices and the true fair prices. These metrics provide an assessment of the accuracy of the quantum estimation.

License

The code in this repository is provided under the MIT License, allowing you to use, modify, and distribute it freely for both commercial and non-commercial purposes.

Feel free to explore, experiment, and adapt the code to suit your needs. If you find any issues or have suggestions for improvement, we welcome contributions and feedback.

Happy quantum option pricing!

---
