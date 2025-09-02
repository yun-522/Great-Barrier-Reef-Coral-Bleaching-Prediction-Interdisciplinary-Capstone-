# Great-Barrier-Reef-Coral-Bleaching-Prediction-Interdisciplinary-Capstone-
## Overview  
This project was developed as part of the **DATA3888 Interdisciplinary Data Science Capstone** at the University of Sydney.  
It was a **group project (6 members, Data Science + Marine Science students)**.  

We investigated whether **environmental variables** could be used to predict coral bleaching severity across the Great Barrier Reef (GBR).  
My contributions included:  
- Developing the **first version of models** (Random Forest, SVM, XGBoost, Ordinal Tree) on the full dataset.  
- Writing the **Results – Part A (model evaluation)** and **Results – Part B (data section)** of the report.  
- Creating the **project schematic** to visualize workflow.  
- Contributing to the **presentation of results**.  

---

## Objectives  
1. **Predict bleaching severity** (ordinal categories 0–4).  
2. **Compare models** using repeated 5-fold cross-validation.  
3. **Assess region-specific differences** across Northern, Central, and Southern GBR.  
4. **Communicate findings** via report, schematic, and Shiny app for stakeholders.  

---

## Tech Stack  
- **Language:** R  
- **Libraries:** `tidyverse`, `caret`, `randomForest`, `e1071`, `xgboost`  
- **Data:**  
  - `bleachingSurveys-1.csv` — bleaching survey records (categories 0–4).  
  - `ereefs_data_filtered.csv` — environmental predictors (temperature, salinity, pH, algae, nitrogen, etc.).  

Due to licensing restrictions, the **full datasets are not included**. Instead, sample rows are provided for illustration.  

- [sample_bleachingSurveys.csv](./sample_bleachingSurveys.csv)  
- [sample_ereefs_data.csv](./sample_ereefs_data.csv)  

---

## Repository Structure  
reef-bleaching-prediction/  
│── [Interdisciplinary Project- Reef 4.html](https://yun-522.github.io/Great-Barrier-Reef-Coral-Bleaching-Prediction-Interdisciplinary-Capstone-/)   # My original code (model development, workflow)  
│── [Report.pdf](https://github.com/yun-522/Great-Barrier-Reef-Coral-Bleaching-Prediction-Interdisciplinary-Capstone-/blob/3341376aa1fd693d91b03250a1ff7456855b0d12/Report.pdf)   # Final group report (my contributions: Results Part A & B, schematic)  
│── [sample_bleachingSurveys.csv](./sample_bleachingSurveys.csv)   # Sample of bleaching survey dataset (5 rows)  
│── [sample_ereefs_data.csv](./sample_ereefs_data.csv)             # Sample of environmental dataset (5 rows)  
│── README.md   # Project description  

---

## Key Results  
- **Central GBR:** Ordinal Tree chosen (Kappa = 0.30, Accuracy = 0.48).  
- **Northern GBR:** SVM chosen for stronger balance across metrics (Kappa = 0.32, MAE = 0.72).  
- **Southern GBR:** Models lacked discriminatory power due to imbalanced data.  

---

## Insights  
- Environmental drivers differed by region:  
  - **Central GBR:** Temperature, pH, nitrogen concentration.  
  - **Northern GBR:** Salinity, nitrogen concentration.  
  - **Southern GBR:** Limited predictive signal due to few bleaching events.  
- Results communicated via a **Shiny dashboard**, enabling stakeholders to explore bleaching maps and environmental drivers interactively.  
