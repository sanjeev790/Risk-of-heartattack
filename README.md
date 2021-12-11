# Risk-of-heart attack
# Heart Disease Prediction using Machine Learning Techniques
Heart disease, alternatively known as cardiovascular disease, encases various conditions that impact the heart and is the primary basis of death worldwide over the span of the past few decades. It associates many risk factors in heart disease and a need of the time to get accurate, reliable, and sensible approaches to make an early diagnosis to achieve prompt management of the disease. Data mining is a commonly used technique for processing enormous data in the healthcare domain. Researchers apply several data mining and machine learning techniques to analyse huge complex medical data, helping healthcare professionals to predict heart disease. This research paper presents various attributes related to heart disease, and the model on basis of supervised learning algorithms as Naïve Bayes, decision tree, K-nearest neighbor, and random forest algorithm. It uses the existing dataset from the Cleveland database of UCI repository of heart disease patients. The dataset comprises 303 instances and 76 attributes. Of these 76 attributes, only 14 attributes are considered for testing, important to substantiate the performance of different algorithms. This research paper aims to envision the probability of developing heart disease in the patients. The results portray that the highest accuracy score is achieved with K-nearest neighbor.
#Supervised Learning
Approach Methodology
This research aims to foresee the odds of having heart disease as probable cause of computerized prediction of heart disease that is helpful in the medical field for clinicians and patients. To accomplish the aim, we have discussed the use of various machine learning algorithms on the data set and dataset analysis is mentioned in this research paper. This paper additionally depicts which attributes contribute more than the others to anticipation of higher precision. This may spare the expense of different trials of a patient, as all the attributes may not contribute such a substantial amount to expect the outcome
1. DATA SET DESCRIPTION
The data set is publicly available on the Kaggle website, and it is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has 10-year risk of future coronary heart disease (CHD). The data set provides the patients’ information. It includes over 4,000 records and 15 attributes. Each attribute is a potential risk factor. There are both demographic, behavioral and medical risk factors.
Attributes:
Demographic:
Sex: male or female(Nominal)
Age: Age of the patient;(Continuous — Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)
2. chest pain:
3.blood pressure:BP Meds: whether or not the patient was on blood pressure medication (Nominal)

4. cholestrol:Tot Chol total cholesterol level.

5. Information on (fasting blood sugar &gt; 120 mg/dl) (1 = true; 0 = false)

6.ECG report:resting electrocardiographic results

7.thalach: maximum heart rate achieved

8.exang: exercise induced angina (1 = yes; 0 = no)

9.oldpeak:ST depression induced by exercise relative to rest

10.thalach: maximum heart rate achieved

11.Target variable to predict:


# TOOL DEVELOPMENT
The full code for this article can be found here. It is implemented in Python and different classification algorithms are used. Below is a brief description of the general approach that I employed:
Data cleaning and pre-processing: Here I checked and dealt with missing and duplicate variables from the data set as these can grossly affect the performance of different machine learning algorithms (many algorithms do not tolerate missing data).
Exploratory Data Analysis: Here I wanted to gain important statistical insights from the data and the things that I checked for were the distributions of the different attributes, correlations of the attributes with each other and the target variable and I calculated important odds and proportions for the categorical attributes.
Feature Selection: Since having irrelevant features in a data set can decrease the accuracy of the models applied, I used the Boruta Feature Selection technique to select the most important features which were later used to build different models.
Model development and comparison: I used four classification models, i.e., Logistic Regression, K-Nearest Neighbors, Decision Trees and Support Vector Machine, After which I compared the performance of the models using their accuracy and F1 scores. I then settled with the best performing model.
3.1 Data cleaning and pre-processing

First 20 records of the data set
There were no duplicate entries in the data set but some had missing values and the table below gives a summary of these:

percentage of missing values per feature

At 9.15%, the blood glucose entry had the highest percentage of missing data. The other features have very few missing entries.
The missing entries accounted for only 12% of the total data and could, therefore, be dropped without losing a lot of data.
3.2 Exploratory Data Analysis
The first step was to check the distribution different attributes and this was best visualized by histograms

Data distribution
It is easy to pick out the categorical and continuous variables from the distribution plots. Also, it can be seen that none of the respondents had prevalent stroke and very few were diabetic, on blood pressure medication or hypertensive. These distributions also raised the suspicion that the data set might not be properly balanced and to confirm this I compared the number of positive and negative cases and true to my suspicions there were 3179 respondents without CHD and 572 patients with CHD.
