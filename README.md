# COVID-19 Data Analysis Project

## Description
This project performs an analysis of COVID-19 data, including country-wise statistics on cases, deaths, recoveries, and active cases. The analysis uses various data wrangling and visualization techniques to gain insights into the impact of COVID-19 across different regions.

### Key Features:
- **Data Wrangling**: Handling missing or inconsistent data.
- **Visualization**: Visualizing total deaths, recoveries, and cases across different countries.
- **Correlation Analysis**: Understanding relationships between variables such as total cases, deaths, and recoveries.
- **Prediction**: Using linear regression to predict COVID-19 deaths based on total cases.
- **Clustering**: Clustering countries based on COVID-19 statistics using K-Means.

## Tech Stack
- **Languages/Tools**: Python, Pandas, Matplotlib, Seaborn, Scikit-learn
- **Visualization Tools**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (for prediction and clustering)

## Files
- `country_wise_latest.csv`: The dataset used for the analysis.
- `COVID19_analysis.ipynb`: Jupyter Notebook containing the entire analysis and visualization code.
- `README.md`: This file, providing details of the project.

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/COVID-19-Data-Analysis.git

   pip install -r requirements.txt
   jupyter notebook COVID19_analysis.ipynb

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
file_path = 'country_wise_latest.csv'
df = pd.read_csv(file_path)

# Top 10 countries by total deaths
top_deaths_countries = df.nlargest(10, 'Deaths')

# Bar plot of top 10 countries by total deaths
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
file_path = 'country_wise_latest.csv'
df = pd.read_csv(file_path)

# Top 10 countries by total deaths
top_deaths_countries = df.nlargest(10, 'Deaths')

# Bar plot of top 10 countries by total deaths
plt.figure(figsize=(10,6))
sns.barplot(x='Country', y='Deaths', data=top_deaths_countries)
plt.title('Top 10 Countries by Total COVID-19 Deaths')
plt.xlabel('Country')
plt.ylabel('Total Deaths')
plt.xticks(rotation=45)
plt.show()



