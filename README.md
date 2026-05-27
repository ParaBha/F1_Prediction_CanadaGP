# Formula 1 Race Predictor 🏎️📊

An end-to-end Machine Learning pipeline built in Python to forecast Formula 1 race outcomes. This project leverages historical race classifications, driver grid positions, and qualifying lap pacing to model and predict the top finishers of a Grand Prix weekend.

## 🌟 Project Milestone: Canadian GP Prediction Success
To test the long-term predictive power of this pipeline, a test run was locked in **two months prior** to the 2026 Canadian Grand Prix weekend at Montreal. Despite F1's extreme operational volatility, the model achieved remarkable precision against the final race classification:

* **P4 Bullseye:** Correctly predicted Charles Leclerc bringing his Ferrari home exactly in **P4**.
* **P8 Precision:** Correctly predicted Pierre Gasly finishing exactly in **P8**.
* **Team Trajectory:** Successfully anticipated the massive upward performance inflection of the Mercedes package weeks in advance, locking out the top tier with Kimi Antonelli and George Russell.

*Note on Track Chaos:* The model predicted a George Russell victory; however, a mechanical power unit failure on Lap 30 forced a DNF while he was leading. This highlighted a classic data science challenge: modeling unpredictable mechanical and environmental anomalies.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Pipelines, Imputation, RandomForest)

---

## 🧬 Data Framework & Feature Engineering
The pipeline processes and merges multi-source historical datasets to construct a robust feature space:
* `F1_2025_QualifyingResults.csv`
* `F1_2025_RaceResults.csv`
* `F1_2025_SprintQualifyingResults.csv`
* `F1_2025_SprintResults.csv`

### Key Features Modeled:
* **Qualifying Pace Progression:** Continuous tracking of individual driver time deltas across `Q1`, `Q2`, and `Q3` sessions.
* **Grid Position Weights:** Assessing historical track-specific probabilities of maintaining positions from the starting grid.
* **Team & Driver Performance Indicators:** Historical feature grouping to capture baseline team development trajectories.
* **Target Encodings:** Evaluation metrics for race wins, podium positions, Fastest Laps, and historic DNF risk thresholds.

---

## 🚀 Pipeline Architecture
The project is built around a structured machine learning pipeline (`pipe1`) ensuring clean reproducibility:
1. **Data Ingestion & Merging:** Cleaning and combining fragmented sprint, qualifying, and race result sets.
2. **Preprocessing & Imputation:** Handling missing data thresholds gracefully using Scikit-Learn's imputation pipelines.
3. **Model Training:** Utilizing an ensemble-based model (`RandomForestClassifier` / `RandomForestRegressor` workflows) to estimate final driver classifications.

---

## 📂
