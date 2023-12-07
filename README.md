**Course Name: Data Science Lab (R4EC3012P)**

**Date: January-May 2023**


# Google Play Store EDA

Exploratory data analysis (EDA) is used by data scientists to analyse and investigate data sets for patterns, and anomalies (outliers), and form hypotheses based on our understanding of the dataset and summarize their main characteristics, often employing data visualization methods.

## Table of Contents

- [About the Project](#about-the-project)
    - [Aim](#aim)
    - [Description](#description)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
- [Theory and Approach](#theory-and-approach)
- [Results and Outcomes](#results-and-outcomes)
- [Contributors](#contributors)
- [Acknowledgements and Resources](#acknowledgements-and-resources)

## About The Project

### Aim

We perform Exploratory Data Analysis (EDA) on the Google Play Store data and produce some results and outcomes.

### Description
The objective of this experiment is to deliver insights to understand customer demands better and thus help application developers to popularize their products. In this project we examine the different attributes present in the data set that affect the popularity of the application. We focused on to answer the questions like,
1. Which category has the greatest number of installations?
2. How many free apps does the Play Store have?
3. Which is the most common category of apps on Play Store?
4. Which is the most expensive category?
5. Which category has the highest number of reviews on Play Store?



## Getting Started

### Prerequisites

- Should have python environment. You can refer [here](https://www.tutorialspoint.com/python/python_environment.htm) for the setup.
- Python librairies
    - [NumPy](https://numpy.org/install/) `pip install numpy`
    - [Seaborn](https://seaborn.pydata.org/installing.html) `pip install seaborn`
    - [Pandas](https://pandas.pydata.org/getting_started.html) `pip install pandas`
    - [Matplotlib](https://matplotlib.org/stable/users/installing/index.html) `pip install matplotlib`

For installation of pip you can refer [here](https://www.geeksforgeeks.org/how-to-install-pip-on-windows/)

- Must have Test Data, or you can get it from [here](https://drive.google.com/drive/folders/1ykGovg3hw3sHR_LZYcHYQq7NeIT37jzk?usp=sharing) and from [kaggle](https://www.kaggle.com/datasets).


### Installation

Clone the repo
    
    
    git clone https://github.com/Yash-Desh/Google-Playstore-EDA.git
    
    


## Theory and Approach


### Data Cleaning

Our data set contains a large number of null values in the rating column, so we drop them. Some of the columns have a smaller number of null values, so we replace the null values in these columns with the mode value of that particular column. Our data set also contains duplicate rows for a single application. We also drop the duplicate rows because the rows contain the identical data. Also drop the rows, which have rating greater than 5.


### Checking how many outliers are present and removing them

Outlier is a data object that deviates significantly from the rest of the data objects and behaves in a different manner. They can be caused by measurement or execution errors. The analysis of outlier data is referred to as outlier analysis or outlier mining.
We find Point Outlier in our dataset by giving the condition of Ratings greater than 5

    
    df[df.Ratings>5]

Box plot and Histogram when outliers present:

![1](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/c6f1c6c3-5e89-462e-a091-0758cf9630d8) ![2](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/6cd12225-4686-47a1-a5c4-948e4f7fb31e)



### Removing Outliers


    df.drop([10472], inplace=True)
    df[10470:10475]

Box plot and Histogram when outliers removed:

![3](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/0fed41b2-8973-4c47-911d-dd38fdc5a3a9) ![4](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/efacacb6-4a6c-4ffd-9f1a-d5541e426304)




### Data visualization

Charts and graphs helped us uncover valuable insights from this complex data, revealing patterns and connections within user engagement metrics like app installations, ratings, and reviews across different categories. This approach highlighted popular app genres and showed how various factors impact app performance. Visualizing market trends and distribution of key variables guided decisions on app development, marketing, and user experience. Ultimately, these visuals provided a compelling way to communicate our findings, supporting the conclusions drawn from the analysis.



## Results and Outcomes

The following graphs depict the results of the visualization:

1. Category VS Install:

![5](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/4f73b3a9-183d-47e0-835a-070802bfb741)


2. Category VS Pricing:

![6](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/55d56ea5-f133-487c-b574-8a34006118dc)


3. Category VS Reviews:

![7](https://github.com/cp2392/Google-Playstore-EDA/assets/88549231/79c05d4b-b06c-4f7d-88f0-5dde4ea50782)


Most of the apps are free so developers should focus on creating free apps to have a huge customer base. More Apps should be in the category like Events, Beauty, Parenting as they have not been explored much but still quite popular with huge installations. In order to retain the customer base apps should be updated regularly Developers should develop apps such that their content is available for everyone.
1. Most common category of apps on the Play Store is: **Family**
2. Percentage of free apps on the Play Store is: **~92%**
3. Category with the greatest number of app installs on the Play Store is: **Communication**
4. Category with the greatest number of reviews is: **Communication**
5. Category with the most expensive apps on the Play Store is: **Finance**




## Contributors

- [Chirag Patil](https://github.com/cp2392)
- [Yash Deshpande](https://github.com/yashLM705)
- Atharva Bendre
- Shreyas Bhatlawande


## Acknowledgements and Resources

- [Play Store EDA on Kaggle](https://www.kaggle.com/code/tirendazacademy/google-play-store-eda-data-visualization/notebook)
- [YouTube - Fun with Data Science](https://www.youtube.com/@FUNWITHDATASCIENCE)
