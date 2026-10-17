# 🔍 Titanic Mini EDA — Task 3

### Data Science / Data Analysis with Python Internship — Main Crafts Technology

This repository contains my submission for **Task 3** of the 6-week virtual Data Science internship at **Main Crafts Technology**. Building on Task 2, this task is a **Mini Exploratory Data Analysis (EDA)** of the Titanic dataset, with better missing-value handling, deeper `groupby` insights, and more advanced visualizations.

---

## 📁 Dataset

- **Name:** Titanic Dataset
- **Source:** [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **File used:** `train.csv`
- **Size:** 891 passengers, 12 attributes

---

## 🎯 Objective

1. **Clean the dataset:** fill missing `Age` with the mean, drop irrelevant columns (e.g. `Cabin`).
2. **Answer analysis questions:**
   - Survival rate by **Age Group**
   - Survival rate by **Embarkation Port**
   - Survival rate by **Family Size** (`SibSp + Parch`)
3. **Visualize:** age distribution (histogram), correlation heatmap, survival by family size (bar plot).

---

## 🛠️ Tools & Libraries

`pandas` · `numpy` · `matplotlib` · `seaborn` — run in **Google Colab**.

---

## 📅 Day-wise Progress

| Day | Stage | Notebook |
|---|---|---|
| Day 1 | Load dataset | [`Day1_Data_Loading_Task3.ipynb`](notebooks/Day1_Data_Loading_Task3.ipynb) |
| Day 2 | Clean dataset | [`Day2_Data_Cleaning_Task3.ipynb`](notebooks/Day2_Data_Cleaning_Task3.ipynb) |
| Day 3 | Analysis questions | [`Day3_Analysis_Task3.ipynb`](notebooks/Day3_Analysis_Task3.ipynb) |
| Day 4 | Visualizations | [`Day4_Visualizations_Task3.ipynb`](notebooks/Day4_Visualizations_Task3.ipynb) |
| Day 5 | Conclusion | [`Day5_Conclusion_Task3.ipynb`](notebooks/Day5_Conclusion_Task3.ipynb) |

The complete notebook is [`Titanic_EDA_Task3.ipynb`](Titanic_EDA_Task3.ipynb).

---

## 🔍 Key Findings

- 🧹 **Cleaning:** `Age` (177 missing) filled with the mean (~29.7); `Cabin` (687 missing, ~77%) and `Ticket` dropped; 2 missing `Embarked` values filled with the mode.
- 👶 **Age group:** children survived most (**~58%**); young adults least (**~33%**).
- ⚓ **Embarkation port:** Cherbourg **~55%**, Queenstown **~39%**, Southampton **~34%**. Cherbourg's lead is largely a class effect (about half its passengers were 1st class).
- 👨‍👩‍👧 **Family size:** solo travellers survived at **~30%**; families of 1–3 relatives reached **55–72%**; families of 4+ did poorly (0–33%).
- 🔥 **Correlations:** `Pclass` (−0.34) and `Fare` (+0.26) relate most strongly to survival. `FamilySize` shows almost no linear correlation (0.02) despite a clear non-linear pattern.

---

## 📈 Visualizations

| Chart | Insight |
|---|---|
| Age histogram | Mostly 20–40 year olds; spike at the mean is an imputation artefact |
| Survival by age group | Children had the best odds, young adults the worst |
| Correlation heatmap | Class and fare matter most; family size looks unrelated linearly |
| Survival by family size | Rises to a peak at size 3, then collapses for large families |

Chart images are in the [`visuals/`](visuals/) folder.

---

## 🚀 How to Run

1. Clone this repository.
2. Download `train.csv` from the [Kaggle Titanic page](https://www.kaggle.com/c/titanic/data).
3. Open `Titanic_EDA_Task3.ipynb` in [Google Colab](https://colab.research.google.com/).
4. Run all cells. If `train.csv` is not in the working folder, you will be prompted to upload it.

---

## 📌 Conclusion

Patterns in data are not always causes: the port of embarkation looked important, but it was mostly a proxy for passenger class. And correlation alone can miss real effects, as family size showed.

---

*Completed as part of the 6-week virtual internship at **Main Crafts Technology**.*

#DataScience #Python #Pandas #Seaborn #EDA #TechInternship #Maincrafts
