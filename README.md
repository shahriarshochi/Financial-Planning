# Financial-Planning

This project focuses on using APIs as part of the technical solution for a credit union to develop a prototype application to demo in the next credit union assembly. The credit union board wants to allow the union's members to assess their monthly personal finances, and also be able to forecast a reasonably good retirement plan based on cryptocurrencies, stocks, and bonds.

The aim is to create two financial analysis tools.

The first will be a personal finance planner that will allow users to visualize their savings composed by investments in shares and cryptocurrencies to assess if they have enough money as an emergency fund.

The second tool will be a retirement planning tool that will use the Alpaca API to fetch historical closing prices for a retirement portfolio composed of stocks and bonds, then run Monte Carlo simulations to project the portfolio performance at 30 years. I will then use the Monte Carlo data to calculate the expected portfolio returns given a specific initial investment amount.

## Methods and Techniques Used: 

### Part 1 - Personal Finance Planner

In this section of the challenge, I will create a personal finance planner application. To develop the personal finance planner prototype, I am taking into account the following assumptions:


The average household income for each member of the credit union is $12,000.

Every union member has a savings portfolio composed of cryptocurrencies, stocks and bonds:

Assume the following amount of crypto assets: 1.2 BTC and 5.3 ETH.

Assume the following amount of shares in stocks and bonds: 50 SPY (stocks) and 200 AGG (bonds).

Next I am going to Collect Crypto(bitcoin and ethereym) Prices Using the requests Library. Then I am going to parse the API JSON response to select only the crypto prices and store each price in a variable. Finally I am going to compute the portfolio value of cryptocurrencies and print the results.

Then I am going to collect investments data using Alpaca: SPY (stocks) and AGG (bonds)

I will create two variables named my_agg and my_spy and set them equal to 200 and 50, respectively.
I will be setting the Alpaca API key and secret key variables, then create the Alpaca API object using the tradeapi.REST function from the Alpaca SDK.
Next I need to format the current date as ISO format.
I will fetch the current closing prices for SPY and AGG using Alpaca's get_bars() function. Afterwards I will transform the function's response to a Pandas DataFrame and preview the data.
I will pick the SPY and AGG close prices from the Alpaca's get_bars() DataFrame response and store them as Python variables. Print the closing values for validation.
Compute the value in dollars of the current amount of shares and print the results.


#### Savings Health Analysis:

In this section, I will assess the financial health of the credit union's members.

I will create a variable called monthly_income and set its value to 12000.

To analyze savings health, I am going to create a DataFrame called df_savings with two rows,  store the total value in dollars of the crypto assets in the first row and the total value of the shares in the second row.

I will use the df_savings DataFrame to plot a pie chart to visualize the composition of personal savings.

I will use if conditional statements to validate if the current savings are enough for an emergency fund. An ideal emergency fund should be equal to three times the monthly income.

If total savings are greater than the emergency fund, a message congratulating the person for having enough money in this fund is to be displayed.

If total savings are equal to the emergency fund, a message congratulating the person on reaching this financial goal is to be displayed.

If total savings are less than the emergency fund, a message showing how many dollars away the person is from reaching the goal is to be displayed.

### Part 2 - Retirement Planning

In this section, I will use the Alpaca API to fetch historical closing prices for a retirement portfolio and then Use the MCForecastTools toolkit to create Monte Carlo simulations to project the portfolio performance at 30 years. I will then use the Monte Carlo data to answer questions about the portfolio.

#### Monte Carlo Simulation


The Alpaca API is to be used to fetch the five years historical closing prices for a traditional 40/60 portfolio using the SPY and AGG tickers to represent the 60% stocks (SPY) and 40% bonds (AGG) composition of the portfolio. API output is to be converted to a DataFrame to preview the output. Then we have to configure and execute a Monte Carlo Simulation of 500 runs and 30 years for the 40/60 portfolio.
Then I plot the simulation results and the probability distribution/confidence intervals.

#### Retirement Analysis:

I fetched the summary statistics from the Monte Carlo simulation results.

Given an initial investment of $20,000, I calculated the expected portfolio return in dollars at the 95% lower and upper confidence intervals.

I calculated the expected portfolio return at the 95% lower and upper confidence intervals based on a 50% increase in the initial investment.

## Goals Of The Project:

The main goal of this project is to use the APIs as the main equipment and perform a detailed analysis on client`s portfolio. Make predictions of their investments and to predict if the client has a strong retirement and health plan based on their investments and portfolio data.


