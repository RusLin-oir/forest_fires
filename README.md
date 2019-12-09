# Introduction
## Project Goal
The Goal of this Project is to use **meteorological data** to predict a **forest fire size**.

## Background
To turn this regression problem into a classification, the target (area burned from the forest fire) is binned into three categories: small, medium, and large. According to Institute for the Conservation of Nature and Forests, a Large Forest Fire is defined as a forest fire burning more than 100 hectares (ha). (https://journals.openedition.org/mediterranee/6863) Therefore, the large threshold is set to be at 100 ha for our model, which determines our focus for our target goal.

## Data Set
- **Imbalanced Data** 
	-**47.78%** of the target (area) is 0.0 (0.0 ha observations were recorded because they were fires with an area of less than 1/100 ha)
**97.87%** of forest fires **were not considered** as large at the time of data collection (out of the three different categories).

* **Delete if nothing else**  
The data somethingsomething.

# Highlight
## Data Preprocessing
* Dates: Turned string months and day of weeks into **ordinal variables**
* Imbalanced data set: performed over-sampling(SMOTE) on the training sets


## Feature Engineering
From the top 3 best performing models:
* checked for feature importance via rfpimp package
* performed random search Cross Validation (CV) for hyperparameter tuning

# Summary
* **Five Model Approach**
Using the Pipeline package, five different sklearn classification models were utilized:
	- **LogisticRegression:** 
	- **KNeighborsClassifier:** 
	- **GaussianNB:** 
	- **SVC:** 
	- **RandomForestClassifier:** 

* **The Best Model after CV using F1 score as Northstar metric**
	- **KNeighborsClassifier** [input metric here]
	- **RandomForestClassifier** [input metric here]
	- **SVC** [input metric here]

* **What we learn from this Project**  
	- [describe baseline model behavior]
	- [pros of our model/ advantages]
	- [comment about our model and others]

# References
## Dataset
	-Source: https://archive.ics.uci.edu/ml/datasets/forest+fires

	-Citation Request: This dataset is public available for research. The details are described in [Cortez and Morais, 2007]. Please include this citation if you plan to use this database:

	-P. Cortez and A. Morais. A Data Mining Approach to Predict Forest Fires using Meteorological Data. In J. Neves, M. F. Santos and J. Machado Eds., New Trends in Artificial Intelligence, Proceedings of the 13th EPIA 2007 - Portuguese Conference on Artificial Intelligence, December, Guimaraes, Portugal, pp. 512-523, 2007. APPIA, ISBN-13 978-989-95618-0-9. Available at: http://www.dsi.uminho.pt/~pcortez/fires.pdf

## Background
	- Flora FERREIRA-LEITE, Luciano Lourenço and António Bento-Gonçalves, « Large forest fires in mainland Portugal, brief characterization », Méditerranée [Online], 121 | 2013, Online since 19 December 2015, connection on 09 December 2019. URL : http://journals.openedition.org/mediterranee/6863 ; DOI : 10.4000/mediterranee.6863
