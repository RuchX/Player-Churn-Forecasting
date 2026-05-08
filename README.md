# 🎮 Player Churn Forecasting — Candy Crush

> Predicting which players are likely to stop playing — before they actually do.

---

## 👩‍💻 About This Project

Player churn is one of the biggest challenges in the gaming industry. When players disengage, it directly impacts revenue and community health. This project tackles that problem head-on using machine learning.

We analyzed real-world inspired Candy Crush gameplay data — covering player purchases, daily playtime, social interactions, and engagement patterns — to build a predictive model that identifies players at risk of churning **before** they leave.

The result? A Random Forest model with **98.5% accuracy** and a dual Power BI dashboard that gives game developers clear, actionable insights to improve player retention.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?logo=scikit-learn)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow?logo=powerbi)
![Pandas](https://img.shields.io/badge/Pandas-Data-green?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red?logo=jupyter)

| Category | Tools Used |
|---|---|
| Language | Python 3.8+ |
| ML Libraries | Scikit-learn, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Power BI |
| Techniques | Random Forest, Logistic Regression, PCA |
| Notebook | Jupyter Notebook |

---

## 📊 Dataset

- **Source:** Candy Crush gaming platform (synthesized real-world data)
- **Total Players:** 2,000 (676 churned + 1,324 non-churned)
- **Key Features:**
  - Purchase frequency & total spend
  - Average daily playtime
  - Level progression rate
  - Social engagement ratio
  - Overall engagement score
  - Time since last purchase
  - Booster usage patterns

---

## 🔄 Project Workflow

```
Data Collection → Preprocessing → EDA → Feature Engineering → Model Training → Evaluation → Power BI Dashboard
```

### 1. Data Preprocessing
- Handled missing values and removed duplicates
- Normalized numerical features to consistent scale
- Applied feature engineering — e.g. `session_duration_log` to capture non-linear patterns

### 2. Exploratory Data Analysis
- Descriptive statistics — mean, median, standard deviation
- Distribution plots — histograms, box plots, density charts
- Correlation matrix to identify churn predictors
- Segmentation analysis by player behavior clusters
- Temporal trend analysis of monthly in-app purchases

### 3. Model Development

**Random Forest** ← Primary Model
- Ensemble of decision trees
- Handles complex non-linear relationships
- Resistant to overfitting

**Logistic Regression** ← Baseline Model
- Simple, interpretable binary classifier
- Used for comparison and benchmarking

**PCA (Principal Component Analysis)**
- Reduced high-dimensional feature space
- Improved model efficiency and interpretability
- Retained essential variance while cutting noise

---

## 📈 Results

### Random Forest — Best Model

| Metric | Score |
|---|---|
| **Accuracy** | **98.5%** |
| Precision (Churned) | 0.98 |
| Recall (Churned) | 0.98 |
| F1-Score (Churned) | 0.98 |
| AUC Score | 1.00 |

### Logistic Regression — Baseline

| Metric | Score |
|---|---|
| Accuracy | 83.75% |
| Precision (Churned) | 0.75 |
| Recall (Churned) | 0.81 |
| F1-Score (Churned) | 0.78 |
| AUC Score | 0.93 |

> **Random Forest outperformed Logistic Regression by ~15%** — chosen as the final model for its ability to capture complex player behavior patterns.

---

## 📊 Power BI Dashboard

Two interactive dashboards were built to visualize churn insights:

### Dashboard 1 — Churned Players (676 players)
- Total spend: **₹7.00K**
- Daily playtime: 2–6 hours
- 594/676 players showed **low average daily playtime**
- 427/676 had **low social engagement**
- 397/676 showed **low purchase frequency**

### Dashboard 2 — Non-Churned Players (1,324 players)
- Total spend: **₹22.23K** (3x higher than churned!)
- Daily playtime: 4–23 hours
- Much higher purchase frequency (up to 23 purchases)
- Significantly stronger engagement across all metrics

### 💡 Key Insight
> Non-churning players spend **3x more** and play **4x longer** daily. Boosting engagement in early game stages is the most effective retention strategy.

---

## 📁 Repository Structure

```
player-churn-forecasting/
│
├── datasets/
│   ├── dataset.csv              # Raw player data
│   └── final_dataset.csv        # Cleaned & engineered dataset
│
├── project_code/
│   └── PlayerChurnForecasting.ipynb  # Full ML pipeline
│
├── powerbi_dashboard/
│   ├── not_to_churn.jpg         # Dashboard — Non-churned players
│   └── to_churn.jpg             # Dashboard — Churned players
│
├── player_churn_powerbi_dashboard.pbix  # Power BI file
└── README.md
```

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/RuchX/player-churn-forecasting.git
```

2. Install required libraries
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

3. Open the notebook
```bash
jupyter notebook project_code/PlayerChurnForecasting.ipynb
```

4. For Power BI dashboard — open `player_churn_powerbi_dashboard.pbix` in Power BI Desktop

---

## 🔑 Key Takeaways

- **Random Forest** is significantly more powerful than Logistic Regression for complex player behavior data
- **PCA** helped simplify the feature space without losing predictive power
- Players who churn show consistently **lower engagement** across ALL metrics — not just one
- **Early intervention** (targeting players showing declining playtime) is the most effective retention strategy
- Game developers can use these insights to trigger personalized retention campaigns **before** a player churns
