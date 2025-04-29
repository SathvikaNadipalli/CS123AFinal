# Analysis of Spaceflight Effects on Mouse Brain Inflammatory Cytokines

This repository contains data and code used to analyze the effects of spaceflight on inflammatory cytokine levels in the brains of mice. The study investigated inflammasome activation in mice housed on the International Space Station (ISS) for 37 days.

## Data Files

* **Metadata File:** `OSD-753Metadata.csv` - Contains metadata associated with each sample.
* **Numerical Data:** `LSDS-113_Immunoassay_Roy_ECLIA_Hippocampus_TRANSFORMED.csv` - Contains the numerical data for each sample, specifically the Electrochemiluminescence Immunoassay (ECLIA) results, representing inflammatory cytokine levels in brain tissue.
* **Analysis Results:** The other `.csv` files in this repository contain saved results from intermediate steps of the KMeans analysis (e.g., cluster centers, feature importance).

## Code

* **Analysis Notebook:** `final.ipynb` - A Jupyter Notebook containing the Python code used for data analysis.

## Analysis Overview

The analysis performed in this repository aimed to understand how spaceflight affects inflammatory cytokine levels in mouse brains. The primary steps involved:

1.  **Data Preprocessing:** Loading and preparing the data from the provided CSV files.
2.  **Initial Labeling:** Samples were initially grouped based on experimental conditions:
    * **Ground:** Basal Control and Vivarium Control (representing normal mouse environments).
    * **Flight:** Space Flight and Ground Control (where "Ground Control" in this context refers to a control group that experienced all aspects of the flight *except* microgravity).
3.  **Data Visualization:** Box plots were generated to visualize the distribution of each cytokine across the experimental groups.
4.  **KMeans Clustering:** KMeans clustering was performed to try to form ground and space clusters.
5.  **Feature Importance Analysis (KMeans):** Feature importance was calculated from the KMeans clustering results to determine which cytokines contributed most to the separation of clusters.
6.  **Key Finding:** The analysis identified `il12p70_concentration_normalized` as the cytokine with the highest feature importance, which was consistent with the observations from the initial box plot visualization. This suggests that IL-12p70 levels have a strong link between spaceflight and inflammasome activation in the brain.

## Conclusion

This analysis indicates that `il12p70_concentration_normalized` is a key cytokine in the brain's response to spaceflight.
