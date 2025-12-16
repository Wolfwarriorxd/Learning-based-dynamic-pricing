# Learning-based-dynamic-pricing
# Learning-Based Dynamic Pricing using Bandit Algorithms

This project implements a learning-based dynamic pricing framework for an e-commerce seller who does not know customer willingness-to-pay in advance. The goal is to learn optimal prices online using only purchase feedback and maximize cumulative revenue.

## Problem Setting
- Customers arrive sequentially.
- The seller chooses a price from a discrete set.
- Each customer decides probabilistically whether to buy.
- The seller observes only buy / no-buy feedback.
- Customer willingness-to-pay is unknown and stochastic.

This setting reflects real-world online pricing problems under uncertainty.

## Methodology
Pricing is modeled as a **multi-armed bandit** problem, where each price level is treated as an arm.

The following strategies are implemented and compared:
- Random Pricing (baseline)
- Epsilon-Greedy
- Upper Confidence Bound (UCB)
- Thompson Sampling (Gaussian, revenue-based)

Customer demand is modeled using:
- A non-uniform willingness-to-pay distribution
- Smooth, probabilistic purchase behavior

An oracle benchmark (best fixed price with known demand) is estimated using Monte Carlo simulation.

## Results
Learning-based methods significantly outperform random pricing.
UCB achieves near-oracle performance with less than 1% regret under realistic stochastic demand.

Key plots and numerical results are stored in the `results_DP/` directory.

## Files
- `dynamic_pricing_smoothed_demand.ipynb` — main implementation and analysis
- `results_DP/` — saved plots and final results
- `requirements.txt` — required Python packages

## Tools Used
- Python
- NumPy
- Matplotlib
- Jupyter Notebook

## Motivation
This project was undertaken as a preparatory study for research in **optimal dynamic pricing using learning-based approaches**.
