
# PredictBC: Predictive Ensemble Models for Breast Cancer Classification Using Microbial and Metabolomic Signatures

## Project Overview
PredictBC leverages advanced ensemble machine learning methods to classify breast cancer cases (pre- and postmenopausal) against control subjects using microbial species and metabolite (BGC) abundance data. The ensemble method significantly enhances predictive performance by integrating predictions from multiple classifiers.

## Repository Structure
```
PredictBC/
│
├── data/
│   ├── metadata_premen_control_case.csv
│   ├── metadata_postmen_control_case.csv
│   ├── premen_species_abundance_matrix.csv
│   ├── postmen_species_abundance_matrix.csv
│   ├── premen_bgc_abundance_matrix.csv
│   └── postmen_bgc_abundance_matrix.csv
│
├── scripts/
│   └── Real_Premen_Species_stack.ipynb
│
├── outputs/
│   ├── confusion_matrix_stacking_ensemble.png
│   ├── roc_curve_all_classifiers.png
│   ├── model_performance_metrics.csv
│   ├── top_10_significant_features.csv
│   ├── top_10_significant_features_per_model.csv
│   └── all_features.csv
│
└── README.md
```

## Data Description
The data includes abundance matrices for microbial species and metabolites (BGC), as well as metadata separately for premenopausal and postmenopausal groups. These datasets distinguish between cases and controls:
- **Premenopause_Case vs Premenopause_Control**
- **Postmenopause_Case vs Postmenopause_Control**

## Modeling Approach
The ensemble model incorporates Random Forest, Gradient Boosting, and XGBoost classifiers, employing a stacking ensemble approach to enhance predictive accuracy. The script provided is for the premenopausal species category but can be generalized to postmenopausal and BGC data.

### Steps Included in the Ensemble Modeling Script:
- Data preprocessing and feature engineering
- Implementation and training of individual classifiers (RF, GB, XGB)
- Stacking ensemble to combine classifier predictions
- Evaluation using ROC-AUC and confusion matrix
- Identification of significant predictive features

## Results Interpretation
- **Confusion Matrix:** Illustrates classification performance of the stacking ensemble model.
- **ROC Curves:** Show performance comparison among individual classifiers (Random Forest, Gradient Boosting, XGBoost).
- **Feature Importance:** Highlights the most significant microbial and metabolite predictors contributing to the classification.

## Running the Analysis
1. Clone the repository.
2. Navigate to the `scripts/` directory.
3. Execute the Jupyter notebook (`Real_Premen_Species_stack.ipynb`) after placing your data in the `data/` folder.

## Dependencies
- Python (>=3.8)
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib

Install required libraries using:
```bash
pip install pandas numpy scikit-learn xgboost matplotlib
```

## Contribution
Contributions are welcome. Please open issues for suggestions or submit pull requests for enhancements.

## License
This project is open-source. You're encouraged to freely use, adapt, and modify the scripts provided. Please acknowledge this repository if you use or modify its scripts for research or publication.
