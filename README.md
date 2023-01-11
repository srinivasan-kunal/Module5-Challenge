# Asset Value and Financial Planning

This project contains an mock-assessment of individual fund portfolios based on given values of crypto currency, stocks and bonds holdings. The assessment of the values uses the asset prices as of 01-06-2023 pulled using API extraction from ALPACA.

Further the module deploys MCForecastTools to use Monte Carlo simulation in order to assess the estimated portfolio returns over 30- years and 10- years to make recommendations for member retirement plan.

---

## Technologies

Key python libraries required for the program have been imported in the first code block and includes- `pandas`, `numpy`, `pathlib` and 
`%matplot inline`.

In order to work with APIs following modules must be available in the virtual environment- `os`, `Requests`,`json` to facilitate API requests. `os` module comes under Python's standard utility models and the `requests` and `json` libraries are installed with Anaconda. Availability of `requests` & `json` libraries can be verified using 

```python
conda list requests

conda list json
```


---

## Installation Guide

In case pandas or numpy modules are unavailable the following commands in the terminal will help install them.

```python
pip install pandas

pip install numpy
```
In case the `requests` and `json` libraries are unavailable the following code will help installing the same. Ensure that the development environment is activated before running the codes below.

For Requests library
```python
conda install -c anaconda requests
```

For json library
```python
conda install -c jmcmurray json
```

In order to interact with APIs a `python-dotenv` library and ALPACA SDK need to be set up.

```python
pip install python-dotenv
```

```python
pip install alpaca-trade-api
```

The availability of the above libray and SDK may be verified using

```python
conda list python-dotenv

conda list alpaca-trade-api
```

---

## Usage

Prior to execution of the .ipynb program create an environment file `(.env)` in the main directory with the ALPACA-KEY & ALPACA-SECRET-KEY. 

In the first part of the program the current value of the current value of the member's asset position is calculated
1) json dumps using Free Crypto APIs are used to extract the price of the crypto currencies held by them
2) Alpaca APIs are used to extract the updated price of the stocks and bonds held by them 

In the second part MCForecastTools.py is deployed to run Monte Carlo simulations on the historical returns on the stocks and bonds held by the member. In this report the simulations are run under two scenario assumptions a 40:60 split between bonds & stocks over 30 years and a 20:80 split between bonds and stocks over 10 years. As per the simulation results the expected value of the portfolio even when weighted heavily on stocks is lower in 10 years that over 30 years.

---

## Contributors


Kunal Srinivasan

---

## License

2022 edX Bootcamps 