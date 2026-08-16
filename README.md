# Drug Review Dataset Analysis

This repository contains an exploratory data analysis (EDA) and data preprocessing pipeline for a Drug Review dataset. The project focuses on cleaning the data, handling missing values, and visualizing trends in patient reviews, drug ratings, and medical conditions.

## Project Overview

The primary notebook, `Self ML.ipynb`, processes raw drug review data (training and testing sets) to prepare it for potential machine learning applications. It includes data ingestion, feature engineering, and statistical visualization.

## Dataset

The analysis uses two primary CSV files:
*   `drugsComTrain_raw.csv`
*   `drugsComTest_raw.csv`

**Features include:**
*   `uniqueID`: Unique identifier for each review
*   `drugName`: Name of the drug
*   `condition`: Medical condition being treated
*   `review`: Text of the patient's review
*   `rating`: Patient rating of the drug (1-10)
*   `date`: Date of the review
*   `usefulCount`: Number of users who found the review helpful

## Technologies Used

*   **Python 3.x**
*   **Pandas:** Data manipulation, cleaning, and aggregation
*   **Matplotlib & Seaborn:** Data visualization
*   **Jupyter Notebook:** Interactive development environment

## Key Steps Performed

1.  **Data Ingestion & Merging:** Loaded and concatenated the training and testing datasets into a single Pandas DataFrame consisting of 215,063 records.
2.  **Data Cleaning:** 
    *   Identified and dropped 1,194 records with missing values in the `condition` column.
    *   Converted the `date` column from a string representation to a standard Pandas datetime format.
3.  **Feature Engineering:**
    *   Extracted the `year` from the date column.
    *   Calculated `review_length` by counting the number of words in each text review.
4.  **Exploratory Data Analysis (EDA):**
    *   Visualized the distribution of patient `ratings` using Seaborn countplots.
    *   Analyzed the distribution of `review_length` using histograms.
    *   Explored the most frequent medical conditions (e.g., Birth Control, Depression, Pain, Anxiety).
    *   Identified the most frequently reviewed drugs (e.g., Levonorgestrel, Etonogestrel).

## How to Run

1.  Clone this repository:
    ```bash
    git clone [https://github.com/Shashwat-Singh536/Drug-Review-Dataset.git](https://github.com/Shashwat-Singh536/Drug-Review-Dataset.git)
    ```
2.  Navigate to the project directory:
    ```bash
    cd Drug-Review-Dataset
    ```
3.  Ensure you have the required libraries installed:
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```
4.  Make sure the raw data files (`drugsComTrain_raw.csv` and `drugsComTest_raw.csv`) are located in the same directory.
5.  Launch the Jupyter Notebook:
    ```bash
    jupyter notebook "Self ML.ipynb"
    ```

## Future Scope
*   Implement Natural Language Processing (NLP) to analyze the sentiment of the text reviews.
*   Train classification models to predict drug ratings or medical conditions based on the review text.
*   Build a recommendation system to suggest drugs based on user conditions and historical review sentiments.
