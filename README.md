<div align="center">

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Cuisine%20Combination%20Analysis&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Cognifyz%20Technologies%20%E2%80%94%20Data%20Analytics%20Internship&descAlignY=60&descSize=16" width="100%"/>

<br>

[![GitHub](https://img.shields.io/badge/GitHub-karthiikofcl07-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/karthiikofcl07)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Karthikeyan_Thirunavukkarasu-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karthikeyan-thirunavukkarasu-2a2949305)
[![Cognifyz](https://img.shields.io/badge/Internship-Cognifyz_Technologies-E94560?style=for-the-badge&logoColor=white)](https://cognifyz.com)

<br>

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=flat-square&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557c?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4C72B0?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-2b9348?style=flat-square)

</div>

---

## About This Project

This repository contains the **Cuisine Combination** analysis task completed as part of the **Cognifyz Technologies Data Analytics Internship**. The analysis is applied to a global restaurant dataset of 9,551 records and addresses two research questions from the internship brief:

> **1.** Identify the most common cuisine combinations present in the dataset.
>
> **2.** Determine whether certain cuisine combinations tend to have higher aggregate ratings.

The work is delivered as a fully self-contained Jupyter Notebook with eight professional visualizations, a statistical summary, and structured written conclusions.

---

## Repository Structure

```
cognifyz_cuisine_analysis/
│
├── analysis.ipynb                       ← Main analysis notebook (open this)
├── cognifyz_dataset.csv                 ← Source dataset (included)
├── requirements.txt                     ← Python dependencies
├── README.md                            ← This file
│
├── fig01_top_individual_cuisines.png
├── fig02_pairwise_combinations.png
├── fig03_full_combo_profiles.png
├── fig04_cooccurrence_heatmap.png
├── fig05_combo_ratings_top_bottom.png
├── fig06_single_vs_multi_rating.png
├── fig07_pairwise_rating_heatmap.png
└── fig08_pair_rating_performance.png
```

---

## Dataset

| Property | Value |
|---|---|
| Source | Global Restaurant Dataset provided by Cognifyz Technologies |
| Total records | 9,551 |
| Features | 21 columns |
| Rating range | 0.0 — 4.9 |
| Unique cities | 141 |
| Unique country codes | 15 |
| Records with cuisine data | 9,542 |
| Records with valid ratings | 7,394 |

Key columns used: `Cuisines`, `Aggregate rating`, `City`, `Country Code`, `Votes`.

---

## Methodology

**Data Preparation** — Rows missing the `Cuisines` field are dropped. Restaurants with an aggregate rating of zero are treated as unrated and excluded from all rating analyses, but retained in frequency counts.

**Feature Engineering** — Each comma-separated cuisine string is parsed into a sorted tuple of individual cuisine names. Three counter structures are built: individual cuisine frequencies, pairwise co-occurrence counts, and full combination profile counts.

**Frequency Analysis** — Top-N rankings are computed for all three structures. A co-occurrence matrix is built for the top 15 cuisines. All rating analyses apply minimum count thresholds (10 for full combinations, 15 for pairwise) to suppress low-confidence estimates.

**Rating Analysis** — Mean aggregate ratings are computed per combination with standard deviation error bars. A distributional comparison is performed between single-cuisine and multi-cuisine restaurants via KDE, violin, and grouped bar charts. Pairwise rating heatmaps are produced for the top 12 cuisines.

---

## Visualizations

| Figure | Description |
|---|---|
| fig01 | Top 20 individual cuisines by restaurant count |
| fig02 | Top 20 most frequent pairwise cuisine combinations |
| fig03 | Full cuisine profile frequency — all profiles and multi-cuisine only |
| fig04 | Co-occurrence heatmap matrix for the top 15 cuisines |
| fig05 | Highest and lowest rated full combinations (min 10 restaurants) |
| fig06 | KDE density, violin, and grouped bar — single vs multi-cuisine ratings |
| fig07 | Pairwise average rating and co-occurrence count heatmaps |
| fig08 | Top 15 and bottom 15 cuisine pairs by average aggregate rating |

---

## Key Findings

**North Indian cuisine dominates** individual frequency, followed by Mughlai, Chinese, and Fast Food — reflecting the dataset's geographic concentration.

**North Indian + Mughlai is the most common pairing**, driven by genuine cultural and culinary overlap. North Indian + Chinese ranks second.

**Multi-cuisine restaurants score marginally higher on average** (3.57 vs 3.50 for single-cuisine), consistent across groups with sufficient sample sizes.

**Japanese, Korean, Continental, and European combinations rank highest** on average rating, associated with upscale urban dining and higher service investment.

**Fast Food, Bakery, and Beverage combinations rank lowest**, driven by high volume, standardized service, and mismatched customer expectations.

---

## Setup and Usage

**Prerequisites:** Python 3.8 or later.

```bash
# 1. Navigate into the project folder
cd cognifyz_cuisine_analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open in VS Code
code analysis.ipynb
```

Select the **Python 3** kernel when prompted, then click **Run All**.

Alternatively:
```bash
jupyter notebook analysis.ipynb
```

---

## Notes

All rating analyses exclude restaurants where `Aggregate rating == 0`, as this indicates a missing rating rather than a genuine low score. Minimum count thresholds (10 for full combinations, 15 for pairwise) ensure all reported averages are statistically credible and not driven by single-restaurant anomalies.

---

<div align="center">

<br>

**Karthikeyan Thirunavukkarasu**
<br>
Data Analytics Intern — Cognifyz Technologies

<br>

[![GitHub](https://img.shields.io/badge/-karthiikofcl07-181717?style=flat-square&logo=github)](https://github.com/karthiikofcl07)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/-Karthikeyan_Thirunavukkarasu-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/karthikeyan-thirunavukkarasu-2a2949305)

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" width="100%"/>

</div>
