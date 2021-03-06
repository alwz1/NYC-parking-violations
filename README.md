# NYC Parking Violations
The use case for the project is to predict the top four violation categories. The dataset "Open Parking and Camera Violations" is downloaded from NYC Open Data. The dataset is provided by the Department of Finance (DOF). It contains more than 47 million records and 19 columns. 
### Table of Contents
1. [Installations](#installations)
2. [Project Motivation](#project_motivation)
3. [File Descriptions](#file_descriptions)
4. [Results](#results)
5. [Licensing, Authors, Acknowledgements](#licensing)

### Installations<a name="installations"></a>
IBM Watson Studio

Python 3.6 with Spark

### Project Motivation<a name="project_motivation"></a>

- What are the top four violation categories?
- Which license types have the most violations?
- Which departments issue the most violations? 
- What are the yearly payment amounts? 
- Predict top four violation categories

### File Descriptions<a name="file_descriptions"></a>
- NYC_Parking_Violations_IBM_Capstone_1.ipynb: Initial Data Exploration
- NYC_Parking_Violations_IBM_Capstone_2.ipynb: Feature Engineering
- NYC_Parking_Violations_IBM_Capstone_3.ipynb: Modeling and Evaluation
- LICENSE.txt: MIT License

### Results<a name="results"></a>
The top four violation categories are 'NO PARKING-STREET CLEANING', 'PHTO SCHOOL ZN SPEED VIOLATION', 
'FAIL TO DSPLY MUNI METER RECPT', and 'NO STANDING-DAY/TIME LIMITS'.

The license types for the most violations are 'PAS', 'COM', 'OMT', 'OMS', and 'SRF', which stand for passenger, commercial, taxi, and special ominibus rentals.

The departments that issue the most violations are Traffic, Department of Transportation, Police Department, and Department of Sanitation. 

Thre is a large increase in yearly payment amount from about 36 million dollars in 2015 to 516 million dollars in 2016. The peak payment amount of 733 million dollars occured in 2018. 

In data preparation stage, the identification features such as 'Summons Number' are dropped. Features with more than 70% missing values such as Judgment Entry Date and Violation Status are also dropped. 'Interest_Amount' is also dropped because it is highly correlated with 'Amount_Due'. The dataset is filtered to include top twelve states, top four violation categories, top ten counties, top ten license types, and top five issuing agencies; 5% of this filtered data is sampled for further processing.

A four-layer neural networks model with 16 units each in the hidden layers was used for predicting the top four violation categories. 
The data was normalized using MinMaxScaler. We found that the accuracy of the model was 0.97. F1 scores for the first and third categories are 0.96 and 0.94 respectively, and the model predicted accurately for second and fourth categories. Decision tree and random forest models were also developed and evaluated, and we found that these models gave similar results as the neural networks model. 


### Licensing, Authors, Acknowledgements<a name="licensing"></a>
MIT License

https://www.ibm.com/watson

https://data.cityofnewyork.us/City-Government/Open-Parking-and-Camera-Violations/nc67-uf89








