# Medical Data Cleaning Pipeline

A reproducible R Markdown workflow for cleaning clinical data, handling biologically impossible values, and producing publication-ready tables and figures.

**📄 [View the rendered report](https://eugenemofeoluwa.github.io/medical-data-cleaning-pipeline/report.html)**

---

## Overview

Most real-world clinical datasets contain coded missing values (zeros, 999, -1) that silently corrupt analyses if not detected. This pipeline demonstrates a documented, defensible approach to data cleaning using the Pima Indians Diabetes dataset.

## Dataset

- **Source:** UCI Machine Learning Repository
- **Observations:** 768
- **Variables:** 8 clinical predictors + 1 binary outcome
- **Known issues:** Biologically impossible zeros in Glucose, BloodPressure, SkinThickness, Insulin, and BMI

## What this project demonstrates

- Automated validation for impossible values
- Missing-data visualization
- Comparison of complete-case vs. median imputation strategies
- Publication-ready descriptive table (Table 1)
- 300 dpi figure export (PNG + PDF)

## Key findings

- 5 variables contain impossible zeros (up to 49% missing in Insulin)
- Complete-case analysis retains 392 of 768 rows
- Median glucose is significantly higher in the diabetes group

## Project structure

```
medical-data-cleaning-pipeline/
├── report.Rmd              # main R Markdown file
├── report.html             # rendered report
├── data/
│   ├── raw/                # original dataset
│   └── cleaned/            # outputs after cleaning
├── figures/                # PNG + PDF figures
├── output/                 # tables
└── README.md
```

## How to reproduce

1. Clone this repository
2. Open `Medical_Cleaning.Rproj` in RStudio
3. Install packages: `tidyverse`, `janitor`, `skimr`, `naniar`, `gtsummary`, `here`, `gt`
4. Open `report.Rmd` and click **Knit**

## Tools

R · RStudio · tidyverse · janitor · skimr · naniar · gtsummary · ggplot2 · R Markdown

## Author

**Eugene Mofeoluwa**
Medical & Biological Data Analyst

*Available for freelance statistical analysis projects.*