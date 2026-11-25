# Bank Customer Segmentation

A team coursework analysis of a 1.04M+ transaction banking dataset (879,357 unique customers). It translates RFM (Recency, Frequency, Monetary) feature engineering and PCA dimensionality reduction (retaining 92% variance across 4 components) into actionable customer profiles.

## Contribution

Team: Mohamed Ayman and Hamed Ahmed, as credited in the project report. Mohamed cleaned and preprocessed the data, worked with the codebase, and authored the report and poster. Modeling choices and results belong to the team project, not to an independent implementation claim by Mohamed.

## Results

K-Means clustering was evaluated with Elbow and Silhouette metrics (0.62 Silhouette score at k=5 clusters), defining targeted banking strategies across 5 distinct segments, including High-Value Transactors and Risk-Prone Outliers driving 22% of total revenue.

## Data and local setup

The notebook expects `bank_transactions.csv` in its working directory. Obtain the dataset from its source and review its terms before use:

https://www.kaggle.com/datasets/shivamb/bank-customer-segmentation

The source dataset contains over a million transactions from an Indian bank. The dataset is not included, nor are trained artifacts or raw customer records.

```bash
python -m venv .venv
# Activate .venv.
pip install -r requirements.txt
jupyter lab bank_customer_segmentation.ipynb
```

Place the authorized dataset beside the notebook and run from that directory. Dependencies are listed for reproducibility work, not a verified lockfile.

## Workflow

1. Load and inspect transaction and customer fields.
2. Clean missing values and date/age fields.
3. Build transaction/customer features and scale numeric columns.
4. Sample up to 100,000 rows for the clustering experiment.
5. Explore elbow/silhouette measures, K-Means segments and PCA projections.

## Limits and verification

This is a cleaned archival notebook, not an independently rerun study. Notebook outputs and execution metadata have been removed, so stale plots and raw customer previews do not ship. The figures above come from the team's analysis and were not re-run during cleanup. Segments are exploratory, not evidence of revenue improvement, creditworthiness or fraud. Review preprocessing assumptions and sampling before interpreting results.

The original report/slides and all data files are omitted from this source-only portfolio copy. No license grant is added on behalf of other contributors or dataset owners.
