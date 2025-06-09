# Afame-Technologies
For Data Science Internship-2025
# Movie Rating Prediction

## Overview
This project predicts movie ratings based on features like genre, director, and actors using a dataset of Indian movies from IMDb provided by Afame Technologies. It involves data cleaning, exploratory data analysis (EDA), feature engineering, and machine learning to estimate user or critic ratings.

## Dataset
- **Source**: The dataset, "Movie dataset.csv," contains Indian movies from IMDb with columns: `Name`, `Year`, `Duration`, `Genre`, `Rating`, `Votes`, `Director`, `Actor 1`, `Actor 2`, `Actor 3`.

## Project Structure
1. **Data Cleaning**:
   - Removed rows with missing `Rating`.
   - Cleaned `Year` and `Duration` to numeric values.
   - Imputed missing `Duration` with mean, `Votes` with median, and categorical fields with "Unknown".
   - Output: `cleaned_movie_dataset.csv`

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed rating distribution, average ratings by genre, and correlations.
   - Identified patterns (e.g., Drama often has higher ratings).

3. **Feature Engineering**:
   - One-hot encoded `Genre` (e.g., `Genre_Drama`, `Genre_Comedy`).
   - Target-encoded `Director` and actors with their average ratings.
   - Added features: number of genres, decade bins.
   - Scaled numeric features.
   - Output: `processed_movie_dataset.csv`

4. **Modeling**:
   - Built a Random Forest Regressor to predict `Rating`.
   - Evaluated with Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score.
   - Output: `movie_rating_predictions.csv` (actual vs. predicted ratings)

## Files
- `movie_rating_prediction.ipynb`: Kaggle notebook with all code (cleaning, EDA, feature engineering, modeling).
- `cleaned_movie_dataset.csv`: Cleaned dataset after preprocessing.
- `processed_movie_dataset.csv`: Feature-engineered dataset for modeling.
- `movie_rating_predictions.csv`: Model predictions on test set.
- `requirements.txt`: Python dependencies for running the notebook.

## Requirements
To run the notebook, install the dependencies:
```bash
pip install -r requirements.txt
