# Prediction Model for Estimating Aqueous SOLubility (EASOL) of Molecular Compound

Sanchita Mondal

## Table of Contents
  -  Background
  -  Data Understanding
  -  Model Training and Evaluation
  -  Discussion and Conclusions

### Background
This study presents a regression technique for determining a compound's aqueous solubility (EASOL-Estimated Aqueous SOLubility) from its structure and feature set. Using linear regression against six molecular characteristics, a set of 1128 observed solubilities was used to create the model.  The most important parameter was the measured log solubility in mols per litre, which was followed by the number of rotatable bonds, number of rings, molecular weight, and the polar surface area. The model well performed for medicinal/agrochemical sized compounds, performing consistently well across the datasets and predicting solubilities within a factor of 6 of their measured values.

### Data Understanding
ESOL is a small dataset consisting of water solubility data for 1128 compounds. The dataset has been used to train models that estimate solubility directly from the extracted features from the chemical structures (as encoded in SMILES strings). This CSV file was obtained from GLambard's GitHub at [https://github.com/GLambard/Molecules_Dataset_Collection/blob/master/originals/ESOL_delaney-processed.csv]. 

### Model Training and Evaluation
Simple linear regressions were performed for each of the features followed by a multiple linear regression using all four features. Visualization of results with matplotlib along with code for creating the models can be found in `Source code/ETSC_Molecular_Solubility.ipynb` . Linear regressions were implemented using the sklearn.linear_model.LinearRegression estimator, and the sklearn library will be used for generating other potential model candidates.

![image](https://github.com/SanchitaMondal/Molecular_Solubility/assets/102673516/128acf96-1b39-41fd-b774-a0e5c5d01c3c)

### Discussion and Conclusions
The multiple linear regression with all four features yielded an R-squared score of 0.686 which is similar to the results obtained by Delaney, even with a subset of the molecules used.

![image](https://github.com/SanchitaMondal/Molecular_Solubility/assets/102673516/22457550-870f-4c48-aad8-aa365e95e1ce)


