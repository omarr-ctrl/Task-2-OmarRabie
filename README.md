# DecodeLabs Internship — Project 2 Submission

This repository contains the final submission for Project 2: Exploratory Data Analysis (EDA) under the DecodeLabs Industrial Training Track.

The objective of this phase was to conduct a diagnostic analysis of the dataset, moving past simple reporting to uncover underlying distributions, trends, anomalies, and feature correlations before executing any downstream predictive modeling.

---

## Technical Framework and Methodology

The exploratory process was built using the Input-Process-Output (IPO) framework to systematically evaluate structural trends:

* Input: Sanitized dataset containing validated behavioral and transaction profiles.
* Process: Applied descriptive statistics, univariate distribution checks, and bivariate correlation mapping.
* Output: Statistical summary reports and quantified observations to support strategic decisions.

---

## Statistical Summary and Data Profiling

### 1. Central Tendency Analysis
Evaluated the geometric behavior of variables to map their true center of gravity:
* Symmetrical Features: Analyzed using Mean calculations due to their balanced, non-skewed distribution.
* Skewed Features: Evaluated using Median values to ensure robust baseline metrics unaffected by extreme anomalies (e.g., heavily skewed financial data).

### 2. Five-Number Summary (Logic Skeleton)
Established the baseline parameters for core features via descriptive distribution tracking:
* Minimum (The structural floor)
* 25th Percentile (Q1)
* 50th Percentile (Median / The structural center)
* 75th Percentile (Q3)
* Maximum (The structural ceiling)

---

## Outlier and Diagnostic Profiling

Anomalies were categorized and isolated using statistical thresholds to separate data collection errors from valid business anomalies:

* Interquartile Range (IQR) Method: Implemented for robust outlier detection on non-normal, skewed business records. Boundaries were calculated using the standard fence rules (Q1 - 1.5 * IQR and Q3 + 1.5 * IQR).
* Z-Score Method: Applied specifically to normally distributed, symmetrical features. Data points displaying an absolute Z-score greater than 3 (|Z| > 3) were flagged.
* Signal vs Noise Diagnostics: Verified structural noise (typos, ingestion errors) for removal, while isolating rare operational signals (VIP transactions, unique events) for targeted assessment.

---

## Correlation and Relationship Mapping

* Method: Evaluated linear dependencies using the Pearson Correlation Coefficient (r).
* Value Space: Tracked on a standard scale from -1.0 (perfect negative linear relationship) to +1.0 (perfect positive linear relationship), with 0.0 signaling no linear correlation.
* Operational Precaution: Acknowledged the causal constraint that correlation indicates a mathematical relationship but does not inherently confirm operational causation due to potential confounding variables.

---

## Operational Impact and Verification

The structural patterns isolated during this phase were evaluated against concrete metrics to deliver functional clarity:
* Translated abstract distribution shifts into clear operational conclusions.
* Discarded legacy charting clutter (such as 3D charts or high-cardinality charts) in favor of high-contrast, high-readability visual distributions.
* Verified that the underlying dataset matches all formatting constraints and is structurally prepared for predictive data modeling or advanced dashboard architecture.
