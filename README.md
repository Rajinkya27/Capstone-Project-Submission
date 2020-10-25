# Capstone-Project-Submission
## Background:
  * As road accidents, injuries & deaths is the global problem that every country is facing. Throughout the world, roads are shared by cars, buses, trucks, motorbikes,   mopeds, pedestrians, animals & other travelers.
  * Travel made possible by motor vehicles supports economic & social development yet each year, vehicles are involved in crashes are responsible for millions of deaths and injuries.
   * Road traffic injuries place a huge burden on low and middle income countries. India, as a developing country, I'd like to work on this data to provide some practical solutions.
  
## Interest:
   * People travelling, goods carriers will be interested to know the traffic condition so as to save the time.  
   *  Different government project contractors will be interested. 
   *  Cities in the country will be smart to implement these ideas.

## Problem:
   * The project aims to predict severity of road accidents according to severity code 3-Fatality, 2b-Serious injury, 2-injury, 1-property damage, 0-unknown.

## Cleaning:
   * I downloaded the given data,Imported basic libraries like numpy, pandas.
   * Used basic concepts of EDA to get acquainted with data.
   * There were a lot of missing values. Replaced them with mode (most frequent value).
   * Deleted features due to redundancy (like SEVERITYCODE.1)
   * In order to deal with the issue of columns having a variation in frequency, arrays were made for each column which were encoded according to the original column and had equal proportion of elements as the original column. Then the arrays were imposed on the original columns in the positions which had Other and Unknown in them. This entire process of cleaning data led to a loss of almost 5000 rows which had redundant data, whereas other rows with unknown values were filled earlier.

## EDA:
   * Feature Selection- Target variable- y= SEVERITYCODE
Independent variables- X= INATTENTIONIND, UNDERINFL, WEATHER, ROAD CONDITION, LIGHT CONDITION, SPEEDING
 * It is seen that the dataset is supervised but an _unbalanced_ dataset where the distribution of the target variable is in almost 1:2 ratio in favor of property damage. 
 * It is very important to have a balanced dataset when using machine learning algorithms. Hence, SMOTE was used from imblearn library in order to balance the target variable in equal proportions in order to have an unbiased classification model which is trained on equal instances of both the elements under severity of accidents.
## Modelling:
 * Logistic Regression: Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable.
In Logistic Regression, independent variables, if categorical they should be converted into dummy or indicator coded.
 * Decision Tree Analysis: The Decision Tree Analysis breaks down a data set into smaller subsets while at the same time an associated decision tree is incrementally developed. The final result is a tree with decision nodes and leaf nodes.
 
## Results:
 * Decision Tree
Accuracy of Decision tree is- 0.5760076740692476
 * Logistic Regression
Accuracy of Logistic Regression- 0.5888219217751715



