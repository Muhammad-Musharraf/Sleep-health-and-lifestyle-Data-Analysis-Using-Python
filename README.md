# 😴 Sleep Health & Lifestyle — Data Analysis Project

A comprehensive Python-based Exploratory Data Analysis (EDA) project investigating the relationships between sleep health, lifestyle habits, stress levels, physical activity, BMI, occupation, and medical risk indicators across 374 individuals.

---

## 📌 Project Overview

This project explores how lifestyle choices and demographic factors influence sleep quality, sleep duration, and the prevalence of sleep disorders. Using a structured dataset of 374 records, the analysis covers data cleaning, multi-condition filtering, grouping, and rich visual storytelling — all aimed at surfacing actionable health insights.

The project is organized around four core analytical themes: **Health & Sleep**, **Lifestyle & Fitness**, **Medical Risk**, and **Demographics**.

---

## 📁 Repository Structure

```
Sleep-health-and-lifestyle-Data-Analysis-Using-Python/
│
├── Dataset/
│   └── Sleep_health_and_lifestyle_dataset.csv   # Source dataset (374 rows, 13 columns)
│
├── Project/
│   └── Project_of_Sleep_health_and_lifestyle (1).ipynb   # Main Jupyter Notebook
│
├── LICENSE
└── README.md
```

---

## 📊 Dataset Description

The dataset contains **374 records** and **13 columns** covering sleep, lifestyle, and health attributes:

| Column | Description |
|---|---|
| `Person ID` | Unique identifier for each individual |
| `Gender` | Male / Female |
| `Age` | Age of the individual (years) |
| `Occupation` | Job role / profession |
| `Sleep Duration` | Average hours of sleep per day |
| `Quality of Sleep` | Self-reported sleep quality score (1–10) |
| `Physical Activity Level` | Daily physical activity (minutes or steps) |
| `Stress Level` | Self-reported stress level (1–10) |
| `BMI Category` | Normal / Overweight / Obese |
| `Blood Pressure` | Systolic/Diastolic reading (e.g. `120/80`) |
| `Heart Rate` | Resting heart rate (bpm) |
| `Daily Steps` | Number of steps walked per day |
| `Sleep Disorder` | None / Insomnia / Sleep Apnea |

- **Rows:** 374
- **Missing Values:** `Sleep Disorder` column had nulls — filled using mode imputation
- **Duplicates:** None

---

## 🔍 Key Analyses Performed

### 🧹 Data Cleaning & Preprocessing
- Shape, info, dtypes, and statistical summary (`describe()`)
- Null detection and mode-based imputation for `Sleep Disorder`
- Duplicate check and unique value inspection
- Blood pressure column split into `Systolic BP` and `Diastolic BP` for medical analysis

---

### 💤 1. Health & Sleep Analysis

| # | Business Question | Real-Life Impact |
|---|---|---|
| Q1 | Who sleeps < 6 hours AND has stress level > 7? | Identifies burnout and mental health risk |
| Q2 | How many overweight/obese people have sleep disorders? | Links obesity to sleep problems |
| Q3 | Which occupations have the most sleep disorder cases? | Supports workplace wellness programs |
| Q4 | Among people aged 40+, who sleeps less than 7 hours? | Targets aging population health risks |

---

### 🏃 2. Lifestyle & Fitness Analysis

| # | Business Question | Real-Life Impact |
|---|---|---|
| Q5 | Do people walking > 10,000 steps have better sleep quality? | Promotes physical activity for sleep health |
| Q6 | Who has low physical activity (< 30) and high BMI? | Identifies lifestyle disease risk |
| Q7 | What is average sleep quality for people who exercise > 60 min/day? | Measures activity's effect on sleep |

---

### 🏥 3. Medical Risk Analysis

| # | Business Question | Real-Life Impact |
|---|---|---|
| Q8 | Who has high blood pressure (>120/80) AND sleep apnea? | Early cardiovascular risk detection |
| Q9 | How many have heart rate > 80 AND stress level ≥ 8? | Detects stress-related health concerns |
| Q10 | Which BMI category has the highest average stress level? | Links weight to mental health |

---

### 👥 4. Demographic Analysis

| # | Business Question | Real-Life Impact |
|---|---|---|
| Q11 | Do males or females report better sleep quality? | Gender-based health recommendations |
| Q12 | Which age group has the highest sleep disorder prevalence? | Targeted healthcare interventions |
| Q13 | Which occupation gets the least average sleep? | Identifies sleep-deprived professions |

---

### 📈 Data Visualizations

| Visualization | Type | Insight |
|---|---|---|
| Quality of Sleep vs Sleep Duration | Line plot | Trend between sleep quality and hours |
| BMI vs Age by Gender | Bar chart | Age and weight distribution by gender |
| Sleep Disorder Distribution | Pie chart | Prevalence of None / Insomnia / Sleep Apnea |
| Occupation vs Age | Bar chart | Age profile of different professions |
| Stress Level vs Sleep Duration | Line plot | Inverse stress-sleep relationship |
| Sleep Disorder vs Sleep Duration (by Gender & BMI) | Bar charts | Multi-dimensional disorder impact |
| Occupation vs Heart Rate | Bar chart | Cardiovascular load by profession |
| Stress Level vs Sleep Quality | Line plot | How stress erodes sleep quality |
| BMI Category Distribution | Pie chart | Weight category breakdown |
| Occupation vs Stress Level (by Gender & BMI) | Bar charts | Stress burden across professions |
| Heart Rate vs Stress Level (by Sleep Disorder) | Line plot | Cardiovascular-stress-disorder link |
| Blood Pressure Distribution | Histogram + KDE | BP spread across population |
| Heart Rate Distribution | Histogram + KDE | Resting HR distribution |
| Blood Pressure vs Heart Rate | Line plot | Cardiovascular co-relationship |
| BMI vs Physical Activity (by Gender) | Bar chart | Activity levels by weight category |
| Daily Steps vs Physical Activity Level | Line plot | Correlation between steps and activity |
| Occupation vs Sleep Duration (by Gender) | Bar chart | Sleep hours by job and gender |
| Stress Level vs Physical Activity | Line plot | How stress affects activity |
| Occupation vs Physical Activity (by Gender) | Bar chart | Fitness behavior by profession |
| Pair Plot (all numeric features, hue=Gender) | Pair plot | Full feature correlation overview |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning, filtering, grouping |
| NumPy | Numerical computations |
| Matplotlib | Base plotting and pie charts |
| Seaborn | Statistical bar, line, dist, and pair plots |
| Jupyter Notebook | Interactive analysis environment |
| Google Colab | Original development environment |

---

## 🚀 Getting Started

### Prerequisites

Install all required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run the Notebook Locally

```bash
# Clone the repository
git clone https://github.com/Muhammad-Musharraf/Sleep-health-and-lifestyle-Data-Analysis-Using-Python.git

# Navigate into the project
cd Sleep-health-and-lifestyle-Data-Analysis-Using-Python

# Launch Jupyter Notebook
jupyter notebook "Project/Project_of_Sleep_health_and_lifestyle (1).ipynb"
```

> **Note:** The notebook was originally developed on Google Colab. Update the dataset path from `/content/drive/MyDrive/Sleep_health_and_lifestyle_dataset.csv` to `../Dataset/Sleep_health_and_lifestyle_dataset.csv` before running locally.

---

## 💡 Key Findings

- **Stress and sleep are inversely related** — individuals with higher stress levels consistently report shorter sleep durations and lower sleep quality scores.
- **Longer membership and higher physical activity correlate with better sleep outcomes**, suggesting that consistent exercise is a meaningful predictor of sleep health.
- **Sleep apnea is concentrated among overweight and obese individuals** with elevated blood pressure, indicating a strong BMI-cardiovascular-disorder connection.
- **Occupation significantly shapes sleep behavior** — certain professions show notably lower average sleep hours and higher stress, pointing to the need for targeted workplace wellness programs.
- **Middle-aged individuals (40+)** are disproportionately affected by insufficient sleep, making them a priority group for preventive health interventions.
- **Gender differences exist in sleep quality**, with one gender reporting marginally better outcomes — highlighting the case for gender-specific health guidance.

---

## 📌 Conclusion

This project demonstrates that sleep health does not exist in isolation — it is deeply intertwined with occupation, physical activity, stress, BMI, and age. By combining multi-condition filtering, aggregation, and diverse visualizations, the analysis surfaces patterns that can inform healthcare professionals, employers, and individuals in building data-driven strategies for better sleep and overall well-being.

---

## 📄 License

This project is licensed under the terms of the [LICENSE](LICENSE) file included in this repository.

---

## 🙋 Author

**Muhammad Musharraf**  
[GitHub Profile](https://github.com/Muhammad-Musharraf)
