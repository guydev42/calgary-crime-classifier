# Calgary community crime classifier

## Problem statement

Calgary has over 200 communities, each with distinct crime patterns shaped by demographics and location. This project classifies communities by crime risk level (low, medium, high) using 77,000+ crime records and census data, helping city planners and residents make informed decisions about safety and resource allocation.

## Approach

- Fetched crime statistics and civic census data from Calgary Open Data via Socrata API
- Aggregated crime counts at the community level with per-capita rates and category breakdowns
- Created risk labels using percentile-based thresholds
- Trained and compared four classifiers: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting
- Evaluated with accuracy and F1 scores (weighted and macro)

## Key results

| Metric | Value |
|--------|-------|
| Best model | Gradient Boosting |
| Accuracy | ~0.85 |
| Weighted F1 | ~0.84 |

## How to run

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Project structure

```
project_02_community_crime_classifier/
├── app.py
├── requirements.txt
├── README.md
├── data/
├── notebooks/
│   └── 01_eda.ipynb
└── src/
    ├── __init__.py
    ├── data_loader.py
    └── model.py
```
