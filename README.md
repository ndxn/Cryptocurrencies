# Cryptocurrencies

## Project Overview
This analysis provides a summary of the investement vaibility of various cryptocurrencies based on previous performance for a hypotheical client, Accountability Accounting. The analysis is conducting using unsupervised machine learning. The goal of the analysis was to select out from the dataset the cryptocurrencies considered viable according to set criteria and then to classify the currencies by their performance.

## Tools Used
- **Language:** Python with Pandas
- **Dependencies:** SKLearn, Plotly, hvPlot dependencies
- **Environment:** Jupyter Notebook

## Summary

The challenge first involved cleaning data from the crypto_data.csv file in order to ensure that both the currencies were worth consideration and that the data could be processed by the machine learning tools. Viable currencies were considered to those that:
- are actively trading.
- have been mined.
- have an algorithm defined.

In order to process the data, it was necessary to:
- remove columns that were redundand (in the case of having filtered the data by trading status).
- create dummy variables for categorical data.
- remove labels.

Because of the number of variables, which was made especially large because of the dummy values associated with the algorithms, it became necessary to reduce the dimensionality of the data. This was accomplished using PCA, wherein the dimensions were reduced to three.

After the dimensions had been reduced, the machine learning algorithm could be put into effect. The primary goal of this project was to classify the different cryptocurrencies. As such, it became necessary to decide what the most appropriate number of clusters would be. Plotting the inertia against the numnber of clusters (K) revealed the "elbow" on the Elbow Curve to be at four clusters.

The cryptocurrencies were then fit into the model and clustered into the four classes. Various visualizations, as presented in the ./Plots folder and within the Juypter Notebook file itself, were generated to demonstrate how the cryptocurrencies clusters have commonality.

## Data Sources
crypto_data.csv, retrieved from CryptoCompare
