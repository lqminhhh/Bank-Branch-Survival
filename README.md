# BranchWise: Predicting Bank Closure and Risk Timing 🏦

## 🔍 Overview

This project investigates the patterns and drivers behind Bank of America's physical branch closures over the past decade. With the rise of digital banking and shifting consumer behavior, understanding what determines the survival or closure of a bank branch is increasingly valuable.

We leverage both supervised machine learning (e.g., XGBoost) and time-to-event modeling (survival analysis) to address:

- **What factors best predict whether a branch will close?**

- **When is a branch most at risk of closure?**

## 📁 Project Structure

```
├── data/                      # Cleaned and processed datasets
├── images/                    # Output plots and visualizations
├── data_cleaning.ipynb        # Jupyter notebook for data preprocessing
├── data_modeling.Rmd          # R Markdown file for model development and analysis
├── data_modeling.html         # Rendered HTML report from RMarkdown
├── networkequity.ipynb        # Notebook calculating and exploring network equity metrics
├── DA352_Final_Project.pdf    # Final project report (detailed findings)
├── README.md                  # This README file
```

## 🧠 Methodology

### 📊 Data
- Primary Source: *FDIC Summary of Deposits* (2014–2024)

- Supplementary Data: *U.S. Census household income* (ZIP-level)

- Target: Binary classification (closed: 0 = open, 1 = closed)

### 🧼 Data Cleaning
- Handled missing values (< 40 rows removed)

- Merged annual reports into panel format

- Engineered features such as: `deposit_change`, `network_equity`, `branch_share`, `market_share`, `entry_time`, and `exit_time` for survival modeling

## 🧪 Reproducibility
To run the analysis:

1. Clone the repo

2. Ensure you have the necessary R packages installed (`tidyverse`, `caret`, `survival`, `xgboost`, etc.)

3. Run `data_cleaning.ipynb` to prepare the dataset

4. Run the analysis using `data_modeling.Rmd` or open the final rendered `data_modeling.html`

## 📌 Key Findings
- Deposit growth and performance are critical indicators of closure risk.

- Branches in rural/low-income areas are disproportionately vulnerable.

- Network equity and local competition influence closure, but to a lesser extent.

- Machine learning methods like XGBoost significantly improve prediction accuracy compared to baseline models.

## 🔮 Future Work
- Incorporate **internal operations data** (customer counts, transactions)

- Apply **deep learning** or **ensemble methods** for greater accuracy

- Integrate **macroeconomic indicators** and time-varying external shocks

## 📚 References
See the `DA352_Final_Project.pdf` for a full list of references and citations used throughout the project.

## 📬 Contact
For inquiries, feedback, or collaboration:

- 📧 Minh Le – le_m2@denison.edu