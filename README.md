# Climate Challenge Week 0: African Climate Trend Analysis

## Project Overview

This project was completed as part of the **10 Academy Artificial Intelligence Mastery Program – Week 0 Challenge**.

The objective was to analyze historical climate and weather data from five African countries:

* Ethiopia
* Kenya
* Sudan
* Tanzania
* Nigeria

Using data from the NASA POWER database, the project investigates temperature trends, precipitation patterns, climate variability, and vulnerability indicators to support evidence-based climate discussions ahead of COP32.

The final analysis focuses on identifying climate trends, comparing countries, and producing actionable insights that can inform climate adaptation and policy decisions.

---

## Business Objective

EthioClimate Analytics was tasked with supporting Ethiopia's preparations for hosting COP32 by analyzing historical climate data across selected African countries.

The project aims to answer:

* What climate trends are changing across the region?
* Which countries are most vulnerable to climate stress?
* How do temperature and precipitation patterns differ across countries?
* What evidence-based recommendations can support climate policy discussions?

---

## Repository Structure

```text
climate-challenge-week0/
│
├── .github/
│   └── workflows/
│       └── unittests.yml
│
├── notebooks/
│   ├── ethiopia_eda.ipynb
│   ├── kenya_eda.ipynb
│   ├── sudan_eda.ipynb
│   ├── tanzania_eda.ipynb
│   ├── nigeria_eda.ipynb
│   └── compare_countries.ipynb
│
├── src/
│
├── scripts/
│
├── tests/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Technologies Used

* Python 3.13
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Scikit-learn
* Jupyter Notebook
* Git & GitHub
* GitHub Actions

---

## Environment Setup

### 1. Clone the Repository

```bash
git clone https://github.com/lydiab04/climate-challenge-week0.git
cd climate-challenge-week0
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

Windows Command Prompt:

```cmd
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Data Preparation

The original datasets are not included in this repository.

Place the downloaded NASA POWER CSV files in a local `data/` directory:

```text
data/
├── ethiopia.csv
├── kenya.csv
├── sudan.csv
├── tanzania.csv
└── nigeria.csv
```

The `data/` directory is excluded from version control through `.gitignore`.

---

## Data Cleaning Process

The following preprocessing steps were applied to each dataset:

1. Load country-specific climate data.
2. Replace NASA sentinel values (`-999`) with `NaN`.
3. Convert `YEAR` and `DOY` into a proper datetime column.
4. Extract month information for seasonal analysis.
5. Detect and remove duplicate records.
6. Identify missing values and apply appropriate handling.
7. Detect outliers using Z-score analysis.
8. Export cleaned datasets for downstream analysis.

---

## Exploratory Data Analysis

For each country, the following analyses were performed:

### Time Series Analysis

* Monthly average temperature trends
* Monthly precipitation trends
* Seasonal climate patterns

### Correlation Analysis

* Correlation heatmaps
* Temperature vs humidity relationships
* Temperature range vs wind speed relationships

### Distribution Analysis

* Precipitation distributions
* Bubble plots for climate variable interactions
* Outlier assessment

---

## Cross-Country Comparison

A comparative analysis was conducted across all five countries to evaluate:

### Temperature Trends

* Monthly average temperature comparisons
* Temperature summary statistics

### Precipitation Variability

* Rainfall distribution comparisons
* Variability assessment

### Extreme Climate Events

* Extreme heat days (>35°C)
* Consecutive dry days

### Statistical Testing

ANOVA testing was used to determine whether temperature differences between countries were statistically significant.

---

## Key Findings

The analysis revealed a "two-headed" climate challenge across Africa:

### Heat-Dominated Vulnerability

Countries such as Sudan experience:

* High average temperatures
* Frequent extreme heat events
* Long dry periods

### Volatility-Dominated Vulnerability

Countries such as Tanzania and Nigeria experience:

* High rainfall variability
* Increased flood risk
* Greater climate uncertainty

These findings suggest that climate adaptation strategies should be tailored to regional climate risks rather than applying a single continental approach.

---

## Reproducing the Analysis

1. Clone the repository.
2. Create and activate the virtual environment.
3. Install dependencies.
4. Place the raw datasets in the local `data/` directory.
5. Run the country-specific EDA notebooks.
6. Run `compare_countries.ipynb` for cross-country analysis and vulnerability ranking.

---

## Continuous Integration

GitHub Actions is configured to automatically verify the project environment whenever updates are pushed to the repository.

The workflow installs project dependencies and validates the Python environment to improve reproducibility.

---

## Author

**Lydia B.**

Computer Science Student
Addis Ababa University

Week 0 Challenge Submission – 10 Academy Artificial Intelligence Mastery Program
