🎬 Netflix Content Analysis

An exploratory data analysis (EDA) of the Netflix Movies and TV Shows dataset from Kaggle, covering data cleaning, feature engineering, and a broad set of visualizations to understand trends in Netflix's content catalog.

📌 Overview

This project analyzes ~8,800 titles listed on Netflix to explore patterns across content type, release year, duration, ratings, and country of origin. It's built as a single Jupyter notebook (Netflix_DA.ipynb) that can be run end-to-end in Google Colab or locally.

📊 Dataset
Source: Netflix Movies and TV Shows (Shivam Bansal, Kaggle)
Contents: Title, type (Movie/TV Show), director, cast, country, date added, release year, rating, duration, genres (listed_in), and description
🧹 Data Cleaning & Feature Engineering
Removed duplicate rows
Filled missing director, cast, and country values with "Unknown"
Filled missing rating with the most frequent rating
Parsed date_added into a proper datetime column
Engineered new columns:
year_added, month_added — when a title was added to Netflix
content_age — years between release and the current year
duration_num — numeric duration extracted from the duration string
duration_category — Short / Medium / Long, based on duration_num
decade — release decade bucket (1990s–2020s)



The notebook walks through a wide range of plots to explore the data from different angles, including:

Release year distribution (histogram, KDE)
Duration distribution (box, violin, boxen plots)
Movies vs. TV Shows breakdown
Content rating distribution
Top 10 countries producing content
Release year vs. duration (scatter, strip, swarm plots)
Correlation heatmap between numeric features
Pairplot and jointplots (scatter, KDE, hex) of release year vs. duration
Clustermap of feature correlations
Combined multi-panel summary figure

🛠️ Tech Stack
Python
pandas, numpy
matplotlib, seaborn
opendatasets (for downloading the Kaggle dataset directly)
