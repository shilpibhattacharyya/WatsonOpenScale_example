# Instructions

This notebook should be run in a Watson Studio project, using with Python 3.5 with Spark runtime environment. If you are viewing this in Watson Studio and do not see Python 3.5 with Spark in the upper right corner of your screen, please update the runtime now. It requires service credentials for the following Cloud services:

### 1. IBM Watson OpenScale
### 2. Watson Machine Learning

The notebook will train, create and deploy a Food Inspection Risk model, configure OpenScale to monitor that deployment, and inject seven days'(not perfect data - still working on it) worth of historical records and measurements for viewing in the OpenScale Insights dashboard.

## Watson Openscale monitoring evaluation through Spark ML Regression model for Food Inspection Dataset
There are over 15,000 food establishments across the City of Chicago that are subject to sanitation inspections by the Department of Public Health. Three dozen inspectors are responsible for checking these establishments, which means one inspector is responsible for nearly 470 food establishments. The Department of Public Health has systematically collected the results of nearly 100,000 sanitation inspections; meanwhile, other city departments have collected data on 311 complaints, business characteristics, and other information. With this information, the city's advanced analytics team and Department of Public Health teamed up to forecast food establishments that are most likely to have critical violations so that they may be inspected first. The result is that food establishments with critical violations are more likely to be discovered earlier by the Department of Public Health's inspectors.

In this notebook I try to monitor bias in this prediction model on two attributes - 'Facility Type' and 'Inspection Type' for monitoring.

## Create a model
The model predicts the inspection results based on Facility Type, Risk, City, State, Violations and Inspection Type. The inspection result is binary (Pass/Fail).


