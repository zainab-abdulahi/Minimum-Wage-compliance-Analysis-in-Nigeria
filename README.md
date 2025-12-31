# Minimum-Wage-compliance-Analysis-in-Nigeria
  The minimum wage represents the legally mandated lowest level of pay that employers must provide to workers. In Nigeria, compliance with the national minimum wage is a critical policy issue, as it directly affects workers’ welfare, income stability, and overall economic equity across states. Despite federal wage policies, not all states comply uniformly, often due to differences in fiscal capacity, revenue generation, and debt burden.
  This project investigates minimum wage compliance across Nigerian states using a five-year panel dataset (2019–2023). The study combines exploratory data analysis, machine learning, and clustering techniques to understand the financial and structural factors influencing compliance.

## Research objectives
  The objectives of this analysis are to:
* Examine state-level trends in fiscal indicators over time
* Analyze how financial capacity and debt structure relate to minimum wage compliance
* Predict which states are likely to comply or not comply with minimum wage policy
* Group states into financially similar clusters

## Data Description
 **Data Type**: Panel data

 **Coverage Period**: 2019–2023

 **Entities**: Nigerian states

## Variables
### Variable	Description
Y	Minimum wage compliance (binary outcome)
X1	Political party affiliation
X2	Net allocation
X3	Internal debt
X4	External debt
X5	Internally Generated Revenue (IGR)
State	State identifier
Year	Time dimension
**Continuous independent variables were standardized using z-scores to ensure comparability across states.**

## Exploratory Data Analysis
### Fiscal Trends Over Time
  An examination of fiscal indicators reveals a general upward trend in: Net allocation, Internally Generated Revenue (IGR), Internal and external debt. Lagos State consistently records significantly higher values across all fiscal indicators, reflecting its dominant economic position. In contrast, states such as Sokoto and Taraba exhibit relatively low fiscal capacity throughout the study period.
### Correlation Analysis
  The correlation matrix indicates a strong positive relationship between internal debt, external debt and IGR. This suggests that states with stronger revenue bases are also more capable of sustaining higher debt levels.

## Predictive Modelling
### Models Applied
* Random Forest Classifier
* XGBoost Classifier
### Validation Approach
  To preserve the temporal structure of the panel data:
* Training set: 2019–2022
* Test set: 2023

## Model Performance
### Model	Accuracy	Interpretation
Random Forest	72.2%	Identified 7 states as non-compliant
XGBoost	80.6%	Identified 14 states as non-compliant
**Feature importance analysis highlights IGR and debt-related variables as the most influential predictors of minimum wage compliance.**

## Clustering Analysis
States were grouped into three clusters based on fiscal indicators:
**Cluster 1**: Lagos State
  A fiscally dominant outlier with extremely high revenue and debt capacity
**Cluster 2**: Delta, Akwa Ibom, and Rivers
  Oil-producing states with strong fiscal capacity
**Cluster 3**: All other states
  States with moderate to low fiscal capacity
**This clustering highlights the structural fiscal inequality across Nigerian states.**

# Key Insights
* Fiscal capacity is a major determinant of minimum wage compliance
* States with higher IGR and sustainable debt structures are more likely to comply
* Political affiliation alone does not fully explain compliance behavior
* Machine learning models provide useful predictive insights beyond descriptive analysis

## Tools & Technologies
Python, pandas, numpy, scikit-learn, XGBoost, statsmodels, matplotlib, seaborn

# Conclusion
  This analysis demonstrates how data science  can be applied to evaluate public policy compliance. By Using  machine learning, the project provides actionable insights into the financial constraints affecting minimum wage implementation across Nigerian states.
