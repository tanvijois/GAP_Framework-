# GAP_Framework-
This repository contains the implementation of the GAP (Greenhouse Gas Analysis Platform) framework for detecting, analysing, and predicting discrepancies (“blind-spots”) between top-down (TD) atmospheric observations and bottom-up (BU) emission inventories across Australasia.

The framework follows three major stages:

Blind-spot Detection
Blind-spot Analysis
Blind-spot Prediction

The study focuses on CO$_2$, CH$_4$, N$_2$O and NO$_2$/NO$_X$ datasets from 2015–2022.

# 1. GAP Data Collection File

This file contains the complete data acquisition and preprocessing workflow.

Responsibilities
= Downloading datasets from CAMS, OMI, and EDGAR
= Spatial harmonisation of datasets
= Temporal aggregation to monthly resolution
= Regional subsetting to Australasia
= Standardisation and integration of multi-gas datasets
= Preparation of aligned TD and BU datasets for modelling Data Sources

# Top-Down (TD) Atmospheric Datasets
### CAMS (Copernicus Atmosphere Monitoring Service

Used for:
CO$_2$
CH$_4$
N$_2$O

Source:
CAMS Atmosphere Data Store (ADS)

### OMI (Ozone Monitoring Instrument)

Used for:
NO$_2$ top-down observations

Source:
NASA Aura OMI OMNO2d v003 product

# Bottom-Up (BU) Emission Inventories
EDGAR (Emissions Database for Global Atmospheric Research)

Used for:
CO$_2$
CH$_4$
N$_2$O
NO$_X$

Note:
EDGAR reports nitrogen oxides as NO$_X$ (NO + NO$_2$), which is used only as a qualitative validation proxy for TD NO$_2$ observations.

# 2. GAP File
This file contains the implementation of the complete GAP framework.

## Included Components
### Blind-spot Detection
TD–BU gap calculation
Blind-spot index computation
Statistical divergence detection
Under-reporting and over-reporting classification

### Blind-spot Analysis
Feature engineering
Lag features
Rolling statistics
Interaction features
XGBoost modelling
SHAP explainability analysis
Block bootstrap validation

### Blind-spot Prediction
ARIMA/SARIMA forecasting for TD datasets
XGBoost forecasting for BU datasets
Future blind-spot reconstruction
Back-testing and forecasting evaluation

# Additional Files
Worldly Impact Excel File: The repository also includes an Excel file summarising the broader environmental and climate accountability impact of the proposed framework, including the significance of TD–BU mismatch detection for emissions monitoring and future climate intelligence systems.
