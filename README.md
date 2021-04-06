# Are water sports the most dangerous activity to avoid being attacked by a shark in the water?

The objective of the project is to perform a first filtering while I take the opportunity to start a first exploratory analysis to determine some hypotheses. Once the first filtering is done, the objective is to clean the dataset to make it ready for the verification of each of the hypotheses. The hypotheses will be verified by visualizing some graphs corresponding to the data obtained from the previous filtering.

![Image text](https://c1.wallpaperflare.com/preview/488/379/718/shark-surfer-wave-fantasy.jpg)

## Table of Contents
1. [General Info](#general-info)
2. [Data treatment](#Data)
3. [Libraries](#Libraries)
4. [Technology](#Technology)
5. [Methodology](#Methodology)

### General Info and Hypotheses

In this analysis we try to prove some hypotheses through a dataset obtained from Kaggle https://www.kaggle.com/teajay/global-shark-attacks. Las hipótesis son las siguientes: 
```
- Can being in motion in the water increase the risk of being attacked by a shark in the water?
- Can it be said that acuatic sports are the activities with the highest risk of lethality in terms of shark attacks?
- In which places is it more likely to be attacked by a shark?
```

### Data treatment

The realization of the project is divided into up to 4 parts: 
1. Preliminary cleaning of the dataset and exploratory analysis of the dataset. 
2. Cleaning of the dataset according to the hypotheses and extraction of up to 3 new data tables. 
3. Visualization of the data obtained in section 2 by using the seaborn library. 
4. Conclusions according to the hypotheses

## Libraries
***
A little intro about libraries. 
```
import pandas as pd
import numpy as np
import re
import matplotlib.pyplot as plot
import src.funciones as fun
import seaborn as srs

```

## Technology: 

A list of technologies used within the project:
* [Jupyter Notebook](https://jupyter.org/) : Version 6.1.4
* [Python](https://www.python.org/): Version 3.8
* [Visual Studio Code](https://code.visualstudio.com/)

## Methodology: 

The realization of the project is divided into up to 4 parts: 
1. Preliminary cleaning of the dataset and exploratory analysis of the dataset: 
* use of some functions to detect anomalies in the dataset (.valuecounts, .shape, .isnull.sum).
* use of other functions to remove null values (dropna. (tresh),df.drop....)
* substitution of some values by using the replace function
* reset.index 

2. Cleaning of the dataset according to the hypotheses and extraction of up to 3 new data tables.

* Cleaning of the Activity column
- use of regex to preserve only the gerunds of the activity
- creation of new column to transfer these gerunds
- assignment of values by creating a dictionary to split the activities according to the movement
- elimination of rows with null values in the column of interest.

* Cleaning of the Fatal column
- standardization of values in Yes, No, Unknown using the replace function. 
- elimination of lines with no value in this section. 
- parallel cleaning of the Activity column in order to be able to relate both in subsequent graphs.
- renaming of columns for further manipulation
- discarding columns using the drop function

* Cleanup of the Country column
- use of the above to list the Country column next to the Fatal column. 

3. Visualization of the data obtained in section 2 by using mainly the seaborn library.
- sns.catplot
- sns.kdeplot
- sns.histplot
- sns.stripplot
- use of the where function for some data changes. 

4. Conclusions according to the hypotheses


## Authors

* **Luis Sánchez de León** - *Initial work* - (https://github.com/lsdl3)




