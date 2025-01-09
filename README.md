# Patient Experience Survey 
The objective of this project is to analyse the latest 12 months of patient survey data regarding the quality of service and medical treatment provided by the doctors. <br>

## Code files
Python 
* Establishing connection to MySQL <br>
https://github.com/bayyangjie/Data-Wrangling/blob/main/Python%20file <br>

SQL
* Merging the datasets and manipulating the merged database <br>
https://github.com/bayyangjie/Data-Wrangling/blob/main/SQL%20codes.sql <br>

R 
* Visualisation and Linear regression <br>
https://github.com/bayyangjie/Data-Wrangling/blob/main/RMarkdown%20file <br>

# About the data
* The timeline for the data used is over a period of 12 months and it is stored in twelve separate microsoft excel documents, one per calendar month. 
* Each column in the excel files represent different quality metrics that are measured, for example overall satisfaction, level of empathy, doctor competency etc. 
* Each metric also has different rating levels. For example, the metric "respectful" has ratings from 1 to 5 and 99 (1:Very Poor to 5:Excellent, and 99:NA which refers to no response recorded)

# Software tools used
* Rstudio
* Tableplus
* VSCode

# About the project
## Data pipeline creation
In this project, I assembled a data flow by creating a single Python program that reads in all the twelve datasets into the MySQL database. Tableplus was the database management tool used in this case. Once the datasets were imported into MySQL, I renamed each table which represents the different months with a different name. Using MySQL, I then constructed a query to create a new table that combined the data from all the twelve datasets. The data types of the column variables are then verified to ensure that they are correct. 

## Visualisation and Regression
After the data had been preprocessed in Tableplus, it was then imported into R for running a **linear regression model** as well as generating a **performance-impact bar plot**. The purpose of running a linear regression model was to evaluate which measurement metrics were the most influential to the response variable, overall patient satisfaction. The model result showed that the level of empathy that the doctor shows to the patient would have the greatest impact on the patient's overall satisfaction. On the other hand, the patient's age has the least impact on the overall patient satisfaction. At the same time, the model results also identified metrics/variables that were statistically insignificant to the response variable's outcome due to having p-values < 0.05.

Regression results: <br>

![image](https://github.com/user-attachments/assets/862cd7d6-76e9-41f1-b412-4f3301f5a96a) <br>

Performance-impact bar plot: <br>

![image](https://github.com/user-attachments/assets/71933a57-73c9-4f48-b34a-98f2abb7e644)




