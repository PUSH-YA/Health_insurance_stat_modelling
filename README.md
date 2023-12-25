# Health_insurance_statistical_modelling

## **Data**

The selected dataset, which we refer to as the "Healthcare Insurance Dataset," consists of essential attributes, including age, gender, BMI, number of dependents (children), smoking habits (yes or no), geographic region, and medical insurance charges. These attributes enable us to study the relationships between personal characteristics and healthcare expenses. The dataset can be accessed through the following site: https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance.

We have chosen to focus on analyzing Health insurance data, sourced from the Willian Oliveira Gibin and Arun Jingar from the site above. This dataset encompasses the following **7** variables: 

- Age: The insured person's age.
- Sex: Gender (male or female) of the insured.
- BMI (Body Mass Index): A measure of body fat based on height and weight.
- Children: The number of dependents covered.
- Smoker: Whether the insured is a smoker (yes or no).
- Region: The geographic area of coverage.
- Charges: The medical insurance costs incurred by the insured person. 

Based on the table above, There are 3 categorical features: `sex`, `smoker` and `region` and the rest are numeric values `age`, `children`, `bmi` and `charges` with first 2 examples being discrete numerical values and the rest two being continuous numeric values. More specific breakdown variables is as following in a tabular format. We have created a function that creates the table which lists the number of observations, the unique values and missing or NA values for each data type (*this will allow for more reusability*)

There seems to be 1338 observations with no missing values in any of the variables. There seems 2 unique categories for sex: `male` and `female`, binary values for smoker and 4 unique values for regions corresponding to the combination of latitude and longitude direction (*see above output*). 

## **Question**

We will use this dataset to answer the following question: 

$$\text{Identify the factors related to assessing the yearly health insurance charges and then predicting the charges given such factors.}$$

This question is quite 

This data can help us answer our question by helping us infer from the Regression models how personal factors such as age, gender, BMI, number of dependents (children), smoking habits (yes or no) and geographic region correlate with medical insurance charges. Our question will focus on mainly inference as we will create a regression model that estimates the impact of these explanatory variables but hypothesis testing will be performed on them to understand their statistical significance to see whether these variables help us predict the medical insurance charges better or not. We will be using the `charges` as a variable of interest or the response variable and the other features will be the explanatory variables helping us create the statistical model to estimate the response variable. The variables that are of datatype `character` will need to be transformed  to `factor` and then several dummy variables need to be created for it. In our analysis we may be able to narrow the down the number of factors for a more reasonable analysis. In brief, regression will have the following general idea:

$$\text{charges} \sim \text{age} + \text{sex} +  \text{bmi} + \text{children} + \text{smoker} + \text{region} + \text{region}$$

The above model shows an additive model with these factors however, we are going to be performing statistical analysis as some additive terms may be removed and some interactive terms might be added.

We think that this question is useful as the use of regression models and statistical analysis in health insurance can help ensure fair and competitive pricing, potentially leading to lower premiums and more transparent cost structures. Furthermore, it also empowers consumers to make informed decisions, choose suitable insurance plans, and ultimately access essential healthcare services without facing financial burdens.
