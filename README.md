# FIFA Player Clustering & Outlier Analysis (2017)

## Overview

This project performs unsupervised analysis of FIFA player performance data using both Python and Orange Analytics.

The objective was to:
- Identify player archetypes using K-Means clustering
- Detect anomalous player profiles using Local Outlier Factor (LOF)
- Validate analytical consistency across Python and Orange

The analysis focuses on FIFA 2017 to ensure a consistent rating scale and avoid cross-season leakage.

---

## Analytical Workflow

### 1. Data Preparation (Python)
- Loaded combined FIFA 2017–2022 dataset
- Filtered to FIFA 2017 season
- Engineered composite features:
  - Pace
  - Shooting
  - Passing
  - Defending
  - Physicality
- Removed rows with missing modeling features

### 2. Outlier Detection (Python)
- Applied Local Outlier Factor (LOF)
- Manhattan distance metric
- Ranked players by LOF score
- Categorized outliers into:
  - Normal
  - Slight
  - Moderate
  - Strong
  - Extreme
- Identified Top 10 structural outliers

### 3. Clustering (Python)
- Applied K-Means (k = 6)
- Computed silhouette scores
- Identified distinct player archetypes

### 4. Visual Validation (Orange Analytics)
- Reproduced clustering structure
- Reproduced LOF anomaly patterns
- Confirmed consistency of results across tools

Both Python and Orange produced structurally similar cluster separations and outlier patterns.

---

## Key Insights

- Elite players form tightly clustered high-performance groups rather than appearing as global anomalies.
- LOF identifies local structural mismatches rather than simply high-performing players.
- Development inconsistency is more common among mid- and lower-tier players.
- Cross-tool validation increases confidence in unsupervised findings.

---

## Tools Used

- Python (Pandas, Scikit-learn)
- Orange Analytics
- Tableau (visual exploration)

---
