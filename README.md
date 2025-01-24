# Python-In-Finance

##Short Rate Model Implementation

This repository demonstrates how to implement and calibrate a Black-Derman-Toy (BDT) short-rate model in Python using real-world data:

##Data Sources

poland_bonds_yield.csv: Polish bond yield data mapped to maturities and converted into zero-coupon bond (ZCB) prices. Source: https://pl.investing.com/rates-bonds/poland-government-bonds
stopy_procentowe_archiwum.xml: Historical central bank rates (NBP). Source: https://nbp.pl/en/monetary-policy/mpc-decisions/interest-rates/

##BDT Model & Calibration

A binomial tree of short rates is built, with each step’s volatility calibrated so that model-implied bond prices match market prices.
The code uses Python’s scipy.optimize to minimize the sum of squared errors between model prices and observed ZCB prices.

##Monte Carlo Simulation & Visualization

Random short-rate paths (up/down moves) are generated from the binomial tree.
Plots show the tree structure, the fit to market bond prices, and simulated short-rate trajectories over time.

In addition to the basic binomial-tree approach, the notebook includes:

Helper Functions to parse CSV/XML data and construct zero-coupon bond prices from yields.
Backward Induction for pricing ZCBs in the tree.
Graphs illustrating the calibrated rates, bond price comparisons, and Monte Carlo paths.
