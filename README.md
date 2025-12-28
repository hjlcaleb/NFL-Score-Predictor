# NFL Score Predictor: Linear Regression Model

This notebook builds a machine learning model to predict NFL game scores, with a specific focus on forecasting **Seattle Seahawks** matchups for the 2025 season.

### Project Overview
* **Goal:** Predict the points (PPG) a team will score based on their season-to-date performance stats.
* **Data Source:** 2015–2025 NFL Season data via `nflreadpy`.
* **Model:** Linear Regression (using `scikit-learn`).

### Methodology
1.  **Feature Engineering:** Aggregating granular stats like `explosivePlaysPerGame` and `stuffRate` from raw Play-by-Play data.
2.  **Target Calculation:** Deriving true `pointsPerGame` from historical schedule results.
3.  **Normalization:**
    * **Numerical:** Scaled using `MinMaxScaler` (0–1 range).
    * **Categorical:** Team names encoded using `OneHotEncoder`.

### Key Features
The model analyzes 9 core metrics to generate predictions:
* `turnOverDifferential`
* `sacksPerGame`
* `stuffRate` (rate at which defenses stop the run at or before L.O.S)
* `avgGain`
* `yardsPerGame`
* `explosivePlaysPerGame` (20+ yard offensive plays)
* `possessionTimeSeconds`
* `redZoneTDPercentage`
* `penaltyYardsPerGame`
