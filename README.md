<h1 align="center">TEAP: Time Entity Adaptation on Panel Data Forecasting via Meta-Learning</h1>

(Codes on Private Repository)
- Panel Data: Data with observations for multiple entities like firms, individuals, or devices over time / time-series data on the entity or individual unit in a specific domain
- Problem: when new entities are added (insufficient amount of data + distribution shift)
- Meta-learning based approach: general feature extraction (meta-knowledge) across entities and times
- Novel data split method: entities over time


## Use of MAML
Authors: Chelsea Finn, Pieter Abbeel, Sergey Levine
Code: https://github.com/cbfinn/maml

### Abstract

- Model that is applicable to gradient-descent-based models to a variety of different learning problems like classification, regression, reinforcement learning
- The goal of meta-learning is to train a model on a variety of learning tasks to solve new learning tasks
- The parameters of the model are explicitly trained such that a small number of gradient steps with a small amount of training data from a new task will produce good generalization performance on that task

### Introduction

> “Learning to learn”
> 
- Goal: to quickly learn a new task from a small amount of new data
- Key idea: to train the model’s initial parameter
- Dynamical systems standpoint: Maximizing the sensitivity of the loss functions of new tasks with respect to the parameters


## Panel Data
- Panel Data: Data that consists of observations about different cross sections across time. Here, a cross-section is an Entity, for example, firms, individuals, or demographic groups
- An axis with only time data from panel data is referred as **Time Series data**
- An axis with only entity data from panel data is referred as **Cross-Sectional data**

[Introduction to the Fundamentals of Panel Data - Aptech](https://www.aptech.com/blog/introduction-to-the-fundamentals-of-panel-data/)

- Time series data properties are:
    - Trends, Volatility, Seasonality, Abberation, Nonlinearity

### Balanced Panel Data vs Unbalanced Panel Data

- Balanced: Have the same number of observations for all groups
- Unbalanced: have missing values at some time observations for some of the groups

→ for unbalanced data, it should include only the consecutive periods for which there are observations for all individuals in the cross-section

### Heterogeneity

- As panel data series modeling centers around addressing the likely dependence across data observations with the same group, it can also address the heterogeneities of each individual and introduce individual-specific effects.
- Homogeneous (or pooled): model parameters are common across individuals
- Heterogeneous: any or all of the model parameters vary across individuals (e.g, fixed effects, random effects.,)

### Stationarity

- Loner time frames: need to care about stationarity
- Weak stationarity requires:
    - same finite unconditional mean and variance at all time periods
    - Autovariances are independent of time
- Nonstationary panel data series: panel series that does not meet conditions of a weakly stationary time series → statistical properties change over time

[Stationarity in Time Series Analysis Explained using Python](https://blog.quantinsti.com/stationarity/)

### Uni/Multivariate Time Series Models

- Univariate: time series that consists of single observations recorded sequentially over equal time increments

[6.4.4. Univariate Time Series Models](https://www.itl.nist.gov/div898/handbook/pmc/section4/pmc44.htm)
