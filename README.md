# Options-Pricing-Models-and-their-Accuracy-Finsearch
### README Content for GitHub Repository

#### **Project Overview**

This project explores the pricing of European call and put options using two prominent financial models: the Black-Scholes model and Monte Carlo simulations. These models are widely used in the field of quantitative finance for option pricing and risk management. The work presented here is part of my end-term report for Finsearch at IIT Bombay.

The repository contains the code, dataset, and analysis conducted to compare the effectiveness of these models in predicting option prices based on historical market data.

#### **Black-Scholes Model**

The **Black-Scholes model** is a mathematical framework for pricing European call and put options. Developed by Fischer Black, Myron Scholes, and Robert Merton, this model assumes that the price of the underlying asset follows a geometric Brownian motion with constant volatility and interest rates.

Key assumptions of the Black-Scholes model include:
- The market is frictionless (no transaction costs, taxes, or restrictions on trading).
- The underlying asset does not pay dividends during the life of the option.
- The risk-free interest rate and the asset's volatility are constant and known.
- The option can only be exercised at maturity (European option).

The model provides a closed-form solution for calculating the theoretical price of European call and put options, making it a fundamental tool in financial markets.

**Formula:**

$\[ C = S_0 \cdot N(d_1) - K \cdot e^{-rT} \cdot N(d_2) \]$

Where:
- $\( C \)$ is the price of the call option.
- $\( S_0 \)$ is the current price of the underlying asset.
- $\( K \)$ is the strike price of the option.
- $\( r \)$ is the risk-free interest rate.
- $\( T \)$ is the time to maturity.
- $\( N(\cdot) \)$ is the cumulative distribution function of the standard normal distribution.
- $\( d_1 = \frac{\ln(S_0/K) + (r + \sigma^2/2)T}{\sigma\sqrt{T}} \)$
- $\( d_2 = d_1 - \sigma\sqrt{T} \)$
- $\( \sigma \)$ is the volatility of the underlying asset.

In this project, we implement the Black-Scholes model to predict call and put option prices and compare them against actual market data.

#### **Monte Carlo Simulation**

The **Monte Carlo simulation** is a versatile method used to model the probability of different outcomes in a process that cannot easily be predicted due to the intervention of random variables. In the context of option pricing, Monte Carlo simulations are used to estimate the price of options by simulating the underlying asset's price path multiple times and calculating the average payoff.

Monte Carlo simulations do not rely on the closed-form solutions like the Black-Scholes model. Instead, they leverage the law of large numbers to approximate the price by running a large number of simulations, each representing a potential future scenario for the asset price.

**Steps Involved in Monte Carlo Simulation for Option Pricing:**

1. **Simulate the Asset Price Path**: Generate a large number of random paths for the underlying asset's price based on its volatility, risk-free rate, and the time to maturity.
2. **Calculate Payoff**: For each simulated path, calculate the option's payoff at maturity.
3. **Discount Payoff**: Discount the payoff back to the present value using the risk-free interest rate.
4. **Average the Payoffs**: Take the average of all discounted payoffs to estimate the option's price.

Monte Carlo simulations are particularly useful for pricing complex derivatives and options where analytical solutions are not available.

#### **Comparison of Models**

In this project, both the Black-Scholes model and Monte Carlo simulations are used to predict the prices of European call and put options. The accuracy of these predictions is evaluated by comparing them to actual market prices, and the results are visualized through detailed plots. The comparison aims to highlight the strengths and weaknesses of each method, particularly in terms of computational efficiency, accuracy, and applicability to different market conditions.

#### **Conclusion**

The results from this project provide valuable insights into the application of these models in real-world financial scenarios. While the Black-Scholes model offers a quick and efficient solution for pricing European options under certain assumptions, Monte Carlo simulations provide a more flexible approach that can accommodate more complex situations at the cost of increased computational effort.

This repository serves as a comprehensive guide for understanding and implementing these models, offering a practical approach to option pricing and risk management.

#### **How to Use This Repository**

1. **Run the Colab Notebook**: The notebook contains all the necessary code and explanations to reproduce the analysis.
2. **Dataset**: The dataset used for back-testing is included in the repository.
3. **Results and Plots**: The notebook generates plots comparing the predicted option prices with actual market prices, along with accuracy calculations.

