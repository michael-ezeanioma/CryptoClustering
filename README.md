# Overview 

Built with Python, Pandas, Scikit-Learn, K-Means, and hvPlot, this project applies clustering analysis to cryptocurrency market data using K-Means and Principal Component Analysis (PCA). The project involves data preprocessing, scaling, clustering, and visualization to identify market trends and categorize cryptocurrencies based on their performance.

# Project Components

__1. Data Preprocessing:__
Loads crypto_market_data.csv into a Pandas DataFrame.
Retrieves summary statistics and visualizes initial trends.
Normalizes data using StandardScaler() from Scikit-Learn.
Creates a new DataFrame with the scaled data, setting "coin_id" as the index.

__2. Finding the Optimal k for Clustering:__
Uses the Elbow Method to determine the best number of clusters (k).
Iterates through k-values from 1 to 11 while computing inertia.
Plots an elbow curve to visually identify the optimal k.

__3. K-Means Clustering on Scaled Data:__
Initializes and fits a K-Means model with the optimal k.
Predicts clusters and adds the labels to a new column in the DataFrame.
Uses hvPlot to create a scatter plot:
X-axis: "price_change_percentage_24h"
Y-axis: "price_change_percentage_7d"
Color: Cluster labels
Hover Info: "coin_id"

__4. Dimensionality Reduction with PCA:__
Reduces the dataset to three principal components using PCA.
Retrieves the explained variance to determine information retention.
Creates a new DataFrame with the PCA-transformed data while keeping "coin_id" as the index.

__5. Finding the Optimal k Using PCA Data:__
Repeats the Elbow Method on the PCA-reduced data.
Compares the optimal k from the PCA data with the original dataset.

__6. K-Means Clustering on PCA Data:__
Applies K-Means clustering to the PCA-transformed dataset.
Visualizes the results using an hvPlot scatter plot, setting:
X-axis: "PC1"
Y-axis: "PC2"
Color: Cluster labels
Hover Info: "coin_id"

__7. Comparing Results & Analysis:__
Compares clustering performance between original and PCA-reduced data.
Evaluates the impact of using fewer features for clustering.
Uses hvPlot to create a composite plot comparing elbow curves and clustering results.

# Files

__Crypto_Clustering.ipynb:__ Jupyter Notebook with all analysis and visualizations.
crypto_market_data.csv – Dataset containing cryptocurrency market data.

# Key Features

__Data Processing & Scaling:__
Loads and normalizes cryptocurrency market data.
Uses StandardScaler() for data normalization.

__Clustering & Visualization:__
Implements K-Means clustering on both original and PCA-reduced data.
Identifies the best number of clusters using the Elbow Method.
Uses hvPlot to visualize cluster distributions.

__Dimensionality Reduction:__
Reduces dataset dimensionality using PCA while retaining essential variance.
Compares clustering performance before and after PCA transformation.

__Analysis & Interpretation:__
Evaluates the impact of reducing feature dimensions.
Compares clustering effectiveness between the scaled data and PCA-transformed data.

# Dependencies

__Pandas:__ Loads and processes the cryptocurrency dataset.

__Scikit-Learn:__ Performs scaling, clustering, and PCA analysis.

__K-Means:__ Groups cryptocurrencies into distinct clusters.

__hvPlot:__ Generates interactive scatter plots and composite visualizations.

# Technologies Used

__Python:__ Core programming language for data processing and analysis.

__Pandas:__ Handles data manipulation and DataFrame operations.

__Scikit-Learn:__ Provides tools for scaling, clustering, and PCA.

__hvPlot:__ Generates interactive visualizations.

# How to Use

1. Clone this repository to your local environment.
2. Open Crypto_Clustering.ipynb in Jupyter Notebook.
3. Run each cell step-by-step to:
4. Preprocess and normalize the dataset.
5. Apply K-Means clustering and visualize the results.
6. Perform PCA to reduce dimensionality.
7. Compare clustering effectiveness before and after PCA.
8. Analyze the results and answer discussion questions.

<!--Mod 19-->
