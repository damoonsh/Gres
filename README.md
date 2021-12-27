# G-Research Crypto Forecasting Competition

This repository contains my attempt at the [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting) competition on Kaggle.

# Data Structure

- The training dataset has timestamp, Asset_ID, Count, Open, Close, High, Low, Volume, VWAP, Target colummns. Where Target is to be predicted. 
- They are missing values within the Target column.



## Time-Series Traits

There some extreme cycles in cryptocurrency market that causes drastic change in market caps and prices. But in order to be able to see if major coins follow these trend/seasonality cycles or not, I got the z-score for each Target (seperated by coin) then graphed the z-scores.

Observing this graph tells us that there is some correlation between ups and downs of all graph. They all go up and down together (for major changes) but still they are some changes in each individual coin that does not follow others' changes.

- The unique changes for each coin might correspond to endorsments (Elon Musk's tweets about Dodge) and major development peaks (or something else).
- These unique changes can be seen as short-term trend for each coin.
- But the changes that are seen in all of the coins at the same can be seen as a general seasonality.

<img style="float: right;" src="./assets/coin-dep.png">


Idea:
- Get the target_z for all the coins, merge then try to find seasonality within that.