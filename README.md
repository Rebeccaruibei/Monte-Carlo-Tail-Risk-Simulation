# Monte-Carlo-Tail-Risk-Simulation
Python Monte Carlo model for simulating heavy-tailed insurance losses, estimating tail-risk measures, and analysing reinsurance-style risk-transfer payoffs.

# Aim
The aim of this project is to model aggregate insurance losses using Monte Carlo simulation and assess the impact of heavy-tailed loss behaviour on portfolio risk. The model estimates key tail-risk metrics such as Value at Risk(VaR) and Tail Value at Risk(TVaR), while also analysing how risk-transfer structures, such as reinsurance layers, affect retained losses and recoveries.

This project is intended to demonstrate how stochastic simulation can be used to understand extreme loss outcomes, qualify downside risk, and evaluate the effectiveness of reinsurance-style protection.

# Overview
Insurance losses are often uncertain, volatile, and heavy-tailed. Traditional averages may not fully capture the risk of rare but severe events. This project uses Monte Carlo simulation to generate many possible loss scenarios under different frequency and severity assumptions.

This model simulates aggregate losses, calculate gross and net loss distributions, estimates tail-risk measures, and compares outcomes before and after applying risk-transfer structures.

# Key Features
- Simulates insurance loss events using Monte Carlo methods.
- Models aggregate losses under frequency and severity assumptions.
- Supports heavy-tailed severity distributions.
- Estimates Value at Risk and Tail Value at Risk.
- Analyses reinsurance-style payoff structures.
- Compare gross losses, recoveries, and retained losses.
- Provides a framework for stress testing and sensitivity analysis

# Model Approach
The simulation follows a standard insurance loss modelling process:
1. Simulate the number of loss events using a frequency distribution.
2. Simulate individual loss severities.
3. Aggregate losses across each simulation trial.
4. Apply risk-transfer or reinsurance payoff rules.
5. Calculate retained losses and recoveries.
6. Repeat the process across many simulations.
7. Summarise the resulting loss distributions and tail-risk metrics.

# Risk Metrics
 # Value at Risk
 Value at Risk estimates the loss level that is not expected to be exceeded at a selected confidence level.

 For example, a 99% VaR represents the loss threshold exceeded in only 1% of simulated scenarios.

 # Tail Value at Risk
Tail Value at Risk estimates the average loss in the tail beyond the VaR threshold.

TVaR is useful for understanding the severity of extreme losses once the VaR level has been breached.

# Reinsurance and Risk Transfer
The model can be used to analyse simple risk-transfer structures by comparing losses before and after applying protection.

Typical outputs include:
- Gross aggregate loss
- Reinsurance or risk-transfer recovery
- Net retained loss
- Reduction in VaR
- Reduction in TVaR
- Payoff under different attachment points and limits.

Example excess-of-loss payoff:
Recovery = min(max(Loss-Attachment Point, 0), Limit)
Net Loss = Loss - Recovery






