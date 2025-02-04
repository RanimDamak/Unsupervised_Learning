# Unsupervised Learning: Clustering & PCA

## Overview
This project focuses on **unsupervised learning techniques**, particularly **Principal Component Analysis (PCA)** and **K-Means Clustering**, to analyze country-level socio-economic and health indicators. The goal is to identify patterns and determine which countries are in dire need of aid.

## Dataset
The dataset used in this project is **Country-data.csv**, which includes various economic, health, and social indicators for different countries.

### Features in the dataset:
- `country`: Name of the country
- `child_mort`: Child mortality rate per 1000 births
- `exports`: Exports as a percentage of GDP
- `health`: Health expenditures as a percentage of GDP
- `imports`: Imports as a percentage of GDP
- `income`: Per capita income in USD
- `inflation`: Inflation rate
- `life_expec`: Average life expectancy
- `total_fer`: Total fertility rate
- `gdpp`: GDP per capita in USD

## Project Structure
- **Unsupervised_Learning.ipynb**: Jupyter Notebook containing data preprocessing, PCA, and clustering implementation.
- **Country-data.csv**: The dataset used for analysis.
- **README.md**: Documentation for the project.

## Implementation Steps
### 1. Data Preprocessing
- Load the dataset and check for missing values.
- Perform exploratory data analysis (EDA) and visualize distributions using boxplots.
- Identify and remove outliers using the Z-score method.
- Standardize the dataset before applying PCA.

### 2. Principal Component Analysis (PCA)
- Standardize the dataset using `StandardScaler`.
- Apply **PCA** to reduce dimensionality while retaining maximum variance.
- Select the optimal number of components by analyzing cumulative variance explained.
- Transform the dataset using **Incremental PCA** with the selected components.

### 3. Clustering using K-Means
- Apply **K-Means clustering** on the PCA-transformed data.
- Use the **elbow method** to determine the optimal number of clusters.
- Assign cluster labels to each country.
- Identify countries that are in **dire need of aid** based on cluster assignments.

## Results & Insights
- PCA helped reduce the dimensionality while preserving important variance.
- K-Means clustering grouped countries into **four distinct clusters**.
- Countries in **Cluster 1** were identified as those most in need of aid, based on factors like low GDP per capita, high child mortality rates, and low life expectancy.

## Dependencies & Setup
### **Requirements**
- Python 3.x
- Jupyter Notebook
- Required libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `sklearn`, `scipy`

### **Installation**
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```sh
   jupyter notebook Unsupervised_Learning.ipynb
   ```

## Acknowledgments
- The dataset was used for educational purposes in exploring **PCA and K-Means Clustering**.
- Libraries such as **Scikit-Learn, Pandas, and Seaborn** were used for analysis and visualization.

## License
This project is open-source and available under the MIT License.
