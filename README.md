# Chatbot - Concord Travel Agency

Team: Hongyi Zhan, Ge Gao, Yanhuan Huang

## Overview

Centered on addressing three fundamental aspects of travel, this project aimed to create a Chatbot for Concord, a Montreal-based travel agency. The objective was to enhance the existing website services by offering personalized customization through the Chatbot. We employed a variety of machine learning techniques to integrate four scenarios, all designed to elevate the overall customer experience.

## Data Description

The solution drew from 4 datasets:customer preferences, travel cost specifics, airfare trends, and destination insights. 
Customer data was built using a python package called Faker and has the following information to be matched with destination characteristics:
- Temperature
- Budget
- Purpose
- Language
- Travel with or without Families

Additionally, the dataset incorporated supplementary information to facilitate matching with like-minded travelers:
- Gender
- Age
- Preferred Destination Category
- Travel Months
- Transportation
- Hobby
- Number of People Tavelling Together

## Scenario Description
#### Scenario 1: Recommendation on destination
In this scenario, we compare similarity between customer preference and city characteristics through **Euclidean distance metric**. We then recommend destination city with the highest similarity to  customers. By doing so, we allow customers to search for any places that they may be interested in, and so to fulfill **the purpose of exploration and discovery**.
#### Scenario 2:  Travel tips
In this scenario, we provide travel tips to customers based on their selections. We offer users to search for general, transportation, culture, language, weather, photography spots, shopping, tipping, and internet tips. This allows chatbot to develop following **the purpose of culture enrichment**.
#### Scenario 3: Find friends for group travel
This scenario helps customers to connect with other travelers who have similar travel habits. It utilizes advanced algorithms, specifically **K-means clustering**, to intelligently group participants based on their personal preferences across various aspects of travel. This enables the creation of well-matched travel companionships and minimize conflicts during trip, and so fulfill **the purpose of building relationships and connections**.
#### Scenario 4: Estimated travel costs
After we implement scenarios to fulfill the three main purposes of travel, we also give estimated travel cost for our customers to help them plan their budgets. It combines sophisticated time series analysis using **ARIMA models** for airfare prediction and the visualization power of pie charts to create a robust platform.

## Design Structure
<img src="images/design_structure.png">

## Libraries Used

- **Pandas**

<img src="images/pandas.png" width="200">

Restructured raw datasets

- **Matplotlib & Wordcloud**

<img src="images/matplotlib.svg" width="200">
<img src="images/wordcloud.png" width="200">

Visualized analysis results and plotted findings using line chart, pie chart and word cloud

- **Scikit-learn**

<img src=images/sklearn.svg.png width="200">

Performed K-means clustering in the process of traveller companion pairing

- **Statsmodel**

<img src=images/statsmodels.svg width="200">

Performed ARIMA model fitting in the process of costs estimation

- **IPython.display**

Created rich and interactive contents and displayed External HTML Files

