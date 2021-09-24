# EDA on Loan Payments Data [View](https://iamswati.github.io/eda-loan/)

This notebook will perform initial analysis and EDA (Exploratory Data Analysis) on Loan Payments Data.

## About The Data
* **Description -** This data set includes customers who have paid off their loans, who have been past due and put into collection without paying back their loan and interests, and who have paid off only after they were put in the collection. The financial product is a bullet loan that customers should pay off all of their loan debt in just one time by the end of the term, instead of an installment schedule. Of course, they could pay off earlier than their pay schedule.
* Data Source: [Link](https://www.kaggle.com/zhijinzhai/loandata)
* Data Format: .csv

## Content

* **Loan_id -** A unique loan number assigned to each loan customers
* **Loan_status -** Whether a loan is paid off, in collection, new customer yet to payoff, or paid off after the collection efforts
* **Principal -** Basic principal loan amount at the origination
* **terms -** Can be weekly (7 days), biweekly, and monthly payoff schedule
* **Effective_date -** When the loan got originated and took effects
* **Due_date -** Since it’s one-time payoff schedule, each loan has one single due date
* **Paidoff_time -** The actual time a customer pays off the loan
* **Pastdue_days -** How many days a loan has been past due
* **Age, education, gender -** A customer’s basic demographic information

## EDA (Exploratory Data Analysis)

* Used for data visualization to draw meaningful patterns and insights. It also involves the preparation of data sets for analysis by removing irregularities in the data.

![image](https://user-images.githubusercontent.com/67102886/134719845-1689b265-ec26-41b2-8e86-a9047ef3ee8c.png)

```
# Import required libraries
import pandas as pd                       # It is fast, used for data analysis
import numpy as np                        # It is a large collection of high-level mathematical functions to operate on these arrays.
import matplotlib.pyplot as plt           # It is a state-based interface to matplotlib. It provides a MATLAB-like way of plotting.
import seaborn as sns                     # It is the data visualization library based on matplotlib. Provides a high-level interface.
```

## 1. Data Collection & Pre-processing

* Total number of null values and duplicate values

```
# Find total number of null values
print("Total number of null Values... \n\n", loan_data.isnull().sum())

# Check the dataset for duplicate
print("\n Total number of duplicate Values =", loan_data.duplicated().sum())
```

## 2. Visualizations

![image](https://user-images.githubusercontent.com/67102886/134720365-ed383c30-3297-41ca-bfeb-f8953a5a5682.png)

![image](https://user-images.githubusercontent.com/67102886/134720376-d05d84bc-698d-4e7d-8702-fe74245a0a5e.png)

![image](https://user-images.githubusercontent.com/67102886/134720389-67b9cd23-0022-4fb7-9075-ed7849df956a.png)

![image](https://user-images.githubusercontent.com/67102886/134720393-95351d32-2083-4c90-9f8e-4bd924e484e1.png)

![image](https://user-images.githubusercontent.com/67102886/134720412-b39f3242-5208-4c8e-a5e1-8c32f2e3ec2d.png)

![image](https://user-images.githubusercontent.com/67102886/134720431-10f667d3-6d8f-476a-b14d-fcf4f82a579d.png)

![image](https://user-images.githubusercontent.com/67102886/134720453-bf34c794-322d-4433-92be-b128f7232add.png)

![image](https://user-images.githubusercontent.com/67102886/134720463-b9fa2553-335c-4e3d-aeb7-dffb14ce4ab0.png)

![image](https://user-images.githubusercontent.com/67102886/134720479-e2ad187e-42a6-4b09-9f61-64af511eb048.png)

![image](https://user-images.githubusercontent.com/67102886/134720491-c2acaf63-4a3b-4620-b6b9-676b8fe801b5.png)

![image](https://user-images.githubusercontent.com/67102886/134720502-bb58e22e-de04-46bc-82ba-86080cf201d8.png)

## 3. Correlation

![image](https://user-images.githubusercontent.com/67102886/134720565-e78ba3b6-a651-4d13-83a7-c320b2e2ae90.png)

**Obervations:**

* People going for higher studies or college apply for loan with Principal Amount of 800, 1000
* Male candidates apply wide variety of loans
* People who apply for loan of any age or gender maximum take 30 days (Monthly), some 15 days (fortnightly) and very less 7 days (Weekly) to pay off their loan
* 40% of people applying for loans to this (xyz) bank are defaulters which means bank need to work on their policies and recovering rules










