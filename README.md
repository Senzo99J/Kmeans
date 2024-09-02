# Kmeans

## Data Source
The data used in this task was originally sourced from HELP.NGO. This international non-government organization specialises in emergency response, preparedness, and risk mitigation.

### Dataset Attributes
- country: name of the country
- child_mort: death of children under 5 years of age per 1000 live births
- exports: exports of goods and services per capita. Given as a percentage of the GDP per capita
- health: total health spending per capita. Given as a percentage of GDP per capita
- imports: imports of goods and services per capita. Given as a percentage of the GDP per capita
- income: net income per person
- inflation: the measurement of the annual growth rate of the Total GDP
- life_expec: the average number of years a new born child would live if the current mortality patterns remain the same
- total_fer: the number of children that would be born to each woman if the current age-fertility rates remains the same
- gdpp: the GDP per capita. Calculated as the Total GDP divided by the total population.

#### Install and Import Python Libraries on Jupyter Notebook
- import numpy as np
- import pandas as pd
- import matplotlib.pyplot as plt
- import seaborn as sns
- from sklearn import metrics-
- from sklearn.cluster import kmeans
- from sklearn.metrics import Silhoueties_score
- from sklearn.preprocessing import MinMaxScaler 

##### Load data
- Explore the data and present the first five observations

###### Preprocessing and Feature Selection
- Drop any non-numerical columns from dataset
- Create a correlation map of features to explore relationships between features
- Explore the seaborn heatmap 
- Calculating the correlation matrix
- Plot nine different scatter plots with different combination of variables against child_mort
- Plot nine different scatter plots with different combination of variables against gdpp
- Explore the continous independent features against against child_mort using scatterplots
- Set the label for y-axis  to 'child Mort'
- Set the title of the plot to show the relationship between 'Child Mort' and the current feature('f')
- Display the current scatter plot
- Create a pair plot
- Hint: Explore seaborn pairplot

- Create a pair plot using Seaborn for the DataFrame 'data_df'
- A pair plot shows pairwise relationships between variables in the DataFrame
- Display the pair plot
- Note the peaks in the diagonal graphs that are distinct from each other or only overlap slightly. Looking at the scatter plot distributions may also give you some indication of features that would be good candidates for clustering the data.

###### Scaling the Data
- Normalise the data using MinMaxScaler
- Fit and transform the data
- Name the normalised dataframe "df_scaled"

###### K-Means Clustering
- Selecting K
- Plots Elbow curve
- Plots elbow curve using scaled dataset
- Function to calculate the inertia for a range of cluster numbers
- Silhouette score method

###### Fitting a K-Means Model with the selected K value
- Remember to set the random_state to rseed
- Set the numbers of clusters (k) for KMeans clustering
- Set the random seed (rseed) for reproducibility of results
- Count the number of records in each cluster
- Create and initialize a KMeans object with the specified number of clusters
- Fit the K-means model to scaled dataset 'df_scaled'
- Get the cluster labels assigned to each data point in the dataset
- Count the number of records in each cluster

###### Predictions
- Add the predicted cluster labelcolumn to the original dataframe

###### Visualisation the clusters
- child_mortality vs gdpp
- inflation vs gdpp

###### Conclusion
- Countries that are developed have a lower inflation and child mortality rate. Developed countries also have a higher gdpp Countries that are not developed have a higher child mortality and inflation rate.
-  Least developed countries have a lower gdpp.
