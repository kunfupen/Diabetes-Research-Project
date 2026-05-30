# Diabetes Research Project

This project analyzes clinical and lifestyle predictors associated with diabetes outcomes using logistic regression in R. The workflow includes exploratory review, model selection with AIC, multicollinearity checks, visualization, ROC/AUC evaluation, and 5-fold cross-validation.

## Project Highlights

- Built an interpretable logistic regression model for diabetes outcome prediction.
- Compared full, backward-selected, and bidirectional AIC models.
- Evaluated the final model with a train/test split, confusion matrix, ROC curve, AUC, and cross-validation.
- Produced a full written report, research poster, and rendered code appendix.

## Repository Structure

```text
.
├── analysis/
│   └── diabetes_research_code.qmd
├── data/
│   └── diabetes_dataset.csv
├── reports/
│   ├── diabetes_research_report.pdf
│   ├── diabetes_research_code.pdf
│   └── research_poster_with_code.pdf
├── Diabetes Research Project.Rproj
└── README.md
```

## Data

The dataset contains 9,538 records and 17 variables, including age, BMI, blood pressure, HbA1c, lipid measures, family history, diet type, hypertension, medication use, and diabetes outcome.

See [data/README.md](data/README.md) for a compact variable guide.

## Analysis Workflow

The main analysis is in [analysis/diabetes_research_code.qmd](analysis/diabetes_research_code.qmd). It performs:

1. Package loading and dataset import.
2. Initial logistic regression model fitting.
3. AIC-based model selection.
4. Multicollinearity checks using VIF.
5. Correlation review for final predictors.
6. Final logistic regression model fitting.
7. Visualizations for selected diabetes-related patterns.
8. Holdout-set evaluation with a confusion matrix and ROC/AUC.
9. 5-fold cross-validation.

## Final Model

The final logistic regression model uses:

- Age
- BMI
- HbA1c
- Family history

These predictors were selected for an interpretable model focused on clinically meaningful factors.

## Reports

- [Full research report](reports/diabetes_research_report.pdf)
- [Rendered analysis code](reports/diabetes_research_code.pdf)
- [Research poster with code](reports/research_poster_with_code.pdf)

## Reproducibility

This project was developed in R with Quarto. Required R packages:

- `readr`
- `car`
- `ggplot2`
- `dplyr`
- `caret`
- `corrplot`
- `pROC`

To rerun the analysis, open the RStudio project file and render:

```r
quarto::quarto_render("analysis/diabetes_research_code.qmd")
```

If rendering from a terminal, use:

```bash
quarto render analysis/diabetes_research_code.qmd
```

## Notes

The repository keeps the original analysis logic intact while organizing source, data, and final deliverables for easier review on GitHub.
