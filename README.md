# XYZ-Chocolate-Company-Data-Cleaning-and-Transformation
#  Executive Summary
XYZ Chocolate Manufacturer company started its operations in 2020 with branches in India and New Zealand. Workforce data have been collected and stored in a spreadsheet to have a wider perspective of their functions, remuneration, and contribution to the company’s culture. Cleansing and transformations on data were performed through Power Query data management tool and complex formulas and functions were used for measures calculation. Interactive visualization tools were conformed to structure and explore the data to  establish comparisons from different perspectives and obtain descriptive outcomes.
#  Business Problem:
Cleansing and transforming data are crucial steps in the data analysis process to ensure the data is accurate, complete, and ready for analysis. The spreadsheet exposes employee-related data to get meaningful insights that impact the organization's performance. How do we ensure that data is reliable and consistent for supporting the analysis process?
#  Methodology
  1.	Make a profile description to understand data structure, quality, and relationships within the data 
  2.	Conduct data pre-processing that addresses missing values, data types, and format standardization, remove duplicates, and fix errors and inconsistencies to ensure accurate analysis.
  3.	Verify that cleansing and transformation processes were executed correctly and validate them against predefined constraints to ensure their accuracy and integrity.
  4.	Perform an Exploratory Data Analysis (EDA), focusing on summary statistics to understand data context and gain insights within the datasets, including the presence of outliers, patterns and trends.
#  Results and Business Recommendations
Obtaining accurate and reliable results from the data analysis process depends largely on the integrity of the data. A profile description was conducted on the two datasets related to the personnel who work at India and New Zealand locations to examine their structure and content.
A table component was adjusted to store the data and provide a clear and logical format allowing to set rules and transformations to support the data preparation process for further analysis. 
With the use of spreadsheet functionalities, the process derived that:
1.	Gathered information is the same for both datasets and is related to employee gender, department, age, date joined the company, salary, and rating. 
2.	Both datasets were not properly maintained and didn’t follow a standardized format.
3.	Duplicated employees and missing information are present on datasets, holding a total of 213 data points. 
4.	Data has no organization and cannot be easily filtered.
To potentially improve reliability during cleansing and transformation steps, adding more context that reveals a comprehensive and complete picture of the problem’s nature, datasets were consolidated into one, where New Zealand employee data was appended to the India dataset. A custom column “Country” was created to differentiate datapoints.
##  Data Pre-Processing Activities
##  1.	Handling duplicates
Duplicated data points can skew and distort analysis results, leading to confusing insights and causing analysts to draw incorrect conclusions or make flawed decisions. 
Using Power Query <Remove duplicates> feature, employees with duplicated names, are erased, leaving only the first occurrence within the dataset. In case the datapoint appears multiple times, might be convenient to pick a distinct identifier as a duplicate determinator.
##  2.	Dealing with missing values 
According to the dataset characteristics and analysis requirements, common strategies can be applied when missing values in the dataset. First, is just to remove missing values from rows and columns, keeping in mind, that available data can be significantly reduced. On the other hand, missing values can be replaced with estimated or calculated values also called imputation.
That is the case for the gender column, where the strategy to deal with the missing values consists of assigning the <Other> value when the value is not present.
##  3.	Data types and format standardization
Ensuring that each field in the dataset is consistently represented as the correct data type is crucial to preserve consistency in the analysis process. In the case of financial data represented by the employee salary, the type was adjusted as US currency with the corresponding symbol. 
Converting dates and times to a specific format is essential to maintain uniformity. In this case, format variations are present in the date each employee joined to the company, using the DD-MM-YYYY format and the numeric format representing the number of elapsed days since the start of Excel Calendar (01/01/1900) to the date value.  
The date format was adjusted to the standard US format MM-DD-YYYY.

![Picture1](https://github.com/user-attachments/assets/c172b964-d2ed-4f2f-bd18-29ce46d830ba)

The Exploratory Data Analysis (EDA) process was conducted to investigate and summarize the main characteristics of the dataset and serve as a support process for the validation of cleansing and transformation operations. Some of the techniques applied were:
  1.	Calculate basic summary statistics, including measures of central tendency (mean, mode, and median) and count the frequency of different categories for categorical variables.
  2.	Use interactive visualization tools to explore the data and establish comparisons from different perspectives. 
  3.	Visualize relationships between variables to identify patterns or correlations.
  4.	Create a visual representation of the growth of the company in terms of number of employees.

# Summary Statistics

![2](https://github.com/user-attachments/assets/4ecf9783-f8e5-4008-843a-c185f778e24d)

The difference between the mean and median values for salary can be interpreted as the probability that some employees have very high salaries, which means that the average salary is being pulled in the wrong direction.
A custom column <Tenure> was created and added to the table to store the years that every employee has been with the company. The average tenure is then calculated.

#  Comparison of Female vs Male personnel within the company
Understanding the representation and treatment of males and females within a company is crucial for addressing potential disparities in areas such as hiring, promotion, pay, and overall treatment in the workplace. Comparing gender experiences can help identify factors that contribute to job satisfaction and retention, allowing companies to address any specific concerns, improve workplace culture, and retain top talent from both genders.
Pivot tables spreadsheet’s feature was used to summarize how the company’s employees are represented according to gender and with the use of aggregating and grouping functions, such as summing, averaging, and counting, analyze and visualize age, salary, and years working with the company.

![3](https://github.com/user-attachments/assets/c8d47aee-350f-4caf-ac42-69b20a35e51b)

Gender-based analysis reveals no relevant differences regarding department representation, age ranges, and number of years with the company. In the case of salary distribution, females receive higher payments than males, with the exception of the ones who work in the Website department. 

#  Relationship between Salary and Rating
This type of relationship provides valuable insights into how performance evaluations impact compensation within a company. The chocolate manufacturer uses employee ratings as a basis for determining salary adjustments. At first sight, the analysis might reveal that on average, personnel with greater ratings have lower salaries. Referring to how spread the employees are and related to the rating, the wider group has average as performance classifier. That would be a reason to justify why the average salary in this category looks less to inferior rating salaries.

![4](https://github.com/user-attachments/assets/ef853e44-dbec-4d4d-831f-a7c9a955bd71)

#  Growth of the company 
Analyzing company growth in terms of number of employees provides a comprehensive view of the organization's development, structural changes, and implications on overall performance. Understanding how the employee count has evolved can provide context for current trends and future projections.
A pivot table and a line chart were conformed to analyze the growing tendency of the company, based on the date employees joined the company and grouped by month and year.

![5](https://github.com/user-attachments/assets/99ecd73c-8c38-4153-a624-9dc90b500511)

The chart above describes the cumulative total for every year. A new table and chart were built to show the cumulative total over the entire time the company started its operations.

![6](https://github.com/user-attachments/assets/1d96beb1-e099-4297-890e-d474137512ca)

As a result, the graph shows that starting in September 2022, the company has maintained a constant and uniform hiring process for employees.

Being comparative in terms of competitiveness at companies is essential for assessing performance, setting goals, enhancing strategic planning, and  monitoring progress for continuous improvement. Count with a clear and informative structure that summarizes employee key indicators that allow to compare their performance metrics, the chocolate manufacturer  can establish a baseline for evaluating their competitiveness, leverage their strengths to create a sustainable competitive advantage, and foster a culture of continuous improvement.










