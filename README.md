# Time-Series Analysis of Global Temperature & MNIST Clustering

### Project Overview
* **Institution:** IDEAS Foundation (Summer Internship Program 2026)
* **Author: SAMIT MONDAL

---

## Part 1: Time-Series Analysis of Global Temperature Data

### Objective & Data Processing
The objective of this segment was to clean, manipulate, and analyze historical global temperature records using `pandas` and `numpy`.
* **Data Ingestion:** Loaded the global temperature dataset (`monthly_csv.csv`) comprising 3,288 records across two primary tracking sources: **GCAG** and **GISTEMP**.
* **Feature Engineering:** Extracted temporal components (`Year` and `Month`) from the converted datetime index to analyze underlying seasonal and yearly trends.
* **Smoothing:** Computed a 12-month moving average calculated independently per tracking source to highlight global warming indicators.

### Key Insights
* **Source Discrepancies:** Aggregated historical records show that the `GCAG` tracking pipeline yields a slightly higher cumulative baseline mean temperature (~0.0488) compared to `GISTEMP` (~0.0244).
* **Seasonality:** Across all historical records, **October** stands out as the month with the highest average baseline global mean temperature variation.
* **Pivot Aggregation:** Built a structured monthly-versus-yearly pivot table evaluating temperature deviations across the final 20 years (1997–2016) of records.

---

## Part 2: Unsupervised Learning via MNIST Clustering

### Objective & Clustering Pipeline
To evaluate non-temporal multi-dimensional feature groupings, unsupervised learning was applied to image data.
* **Dataset:** MNIST handwritten digit collection (`load_digits`), containing 1,797 samples across 64 feature dimensions.
* **Model:** Unsupervised K-Means Clustering initialized with $K = 10$ unique target clusters to partition digits (0–9).

### Performance Metrics
* Because cluster labels are assigned arbitrarily by K-Means, clusters were programmatically re-mapped to the mode of their factual true target classes.
* **Clustering Evaluation:** The pipeline achieved a **Macro-averaged F1 Score of 0.7895**, proving strong alignment between unsupervised geometric boundaries and original pixel labels.
