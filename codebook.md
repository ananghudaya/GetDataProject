---
title: "Getting and Cleaning Data - Project Codebook"
author: "Anang Hudaya"
date: "Tuesday, January 20, 2015"
output: html_document
---

This codebook was generated using `knitr` tool in RStudio. It describes the variables and other relevant information inside `run_analysis.R`.



## 1. Data Source

* The data for this project has been collected from the accelerometers from the Samsung Galaxy S smartphone. A description on this dataset can be found using the following URL:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
* The data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* The raw data contains in both train and test set:
  
     Type      | Training Data  | Test Data
-------------- | -------------- | -------------
Subject        | `subject_train.txt`  | `subject_test.txt`
Activity Data  | `y_train.txt`  | `y_test.txt`
Actual Data    | `x_train.txt`  | `x_test.txt`

## 2. Variable List

Here is the list of variables and their descriptions:

|Variable         |description                                                                                            |
|:----------------|:------------------------------------------------------------------------------------------------------|
|Subject          |Identifier of subject who performed the activity for each window sample. The value ranges from 1 to 30 |
|activity         |Activity performed by the subject                                                                      |
|featDomain       |Feature: Time or frequency signal domain                                                               |
|featAcceleration |Feature: Acceleration signal (body or gravity                                                          |
|featInstrument   |Feature: Measuring instrument used (Accelerometer or Gyroscope                                         |
|featJerk         |Feature: Jerk signal                                                                                   |
|featMagnitude    |Feature: Magnitude of the signals calculated using the Euclidean norm                                  |
|featVariable     |Feature: Variable (Mean or Standard Deviation)                                                         |
|featAxis         |Feature: 3-axial signals (X, Y, or Z direction)                                                        |
|count            |Feature: Count of datapoints used to compute the average                                               |
|average          |Feature: Average reading for each activity and each subject                                            |



## 3. Dataset Structure

Output of this program is a tidy dataset that consists of 11 variables mentioned in the previous section.

### 3.1 Summary

Below is the summary of the tidy dataset generated using `run_analysis.R`.


```
##     Subject                   activity    featDomain  featAcceleration
##  Min.   : 1.0   LAYING            :1980   Time:7200   NA     :4680    
##  1st Qu.: 8.0   SITTING           :1980   Freq:4680   Body   :5760    
##  Median :15.5   STANDING          :1980               Gravity:1440    
##  Mean   :15.5   WALKING           :1980                               
##  3rd Qu.:23.0   WALKING_DOWNSTAIRS:1980                               
##  Max.   :30.0   WALKING_UPSTAIRS  :1980                               
##        featInstrument featJerk      featMagnitude  featVariable featAxis 
##  Accelerometer:7200   NA  :7200   NA       :8640   Mean:5940    NA:3240  
##  Gyroscope    :4680   Jerk:4680   Magnitude:3240   SD  :5940    X :2880  
##                                                                 Y :2880  
##                                                                 Z :2880  
##                                                                          
##                                                                          
##      count          average        
##  Min.   :36.00   Min.   :-0.99767  
##  1st Qu.:49.00   1st Qu.:-0.96205  
##  Median :54.50   Median :-0.46989  
##  Mean   :57.22   Mean   :-0.48436  
##  3rd Qu.:63.25   3rd Qu.:-0.07836  
##  Max.   :95.00   Max.   : 0.97451
```

### 3.2 Snapshot

A snapshot of the tidy dataset is shown below:


```
##   Subject activity featDomain featAcceleration featInstrument featJerk
## 1       1   LAYING       Time             <NA>      Gyroscope     <NA>
## 2       1   LAYING       Time             <NA>      Gyroscope     <NA>
## 3       1   LAYING       Time             <NA>      Gyroscope     <NA>
## 4       1   LAYING       Time             <NA>      Gyroscope     <NA>
## 5       1   LAYING       Time             <NA>      Gyroscope     <NA>
## 6       1   LAYING       Time             <NA>      Gyroscope     <NA>
##   featMagnitude featVariable featAxis count     average
## 1          <NA>         Mean        X    50 -0.01655309
## 2          <NA>         Mean        Y    50 -0.06448612
## 3          <NA>         Mean        Z    50  0.14868944
## 4          <NA>           SD        X    50 -0.87354387
## 5          <NA>           SD        Y    50 -0.95109044
## 6          <NA>           SD        Z    50 -0.90828466
```

### 3.3 Key Variables

```
## [1] "Subject"          "activity"         "featDomain"      
## [4] "featAcceleration" "featInstrument"   "featJerk"        
## [7] "featMagnitude"    "featVariable"     "featAxis"
```
