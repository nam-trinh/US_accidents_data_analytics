# US_accidents_data_analytics
This is a Notebook that I created to analyze the US accident data analytics.
The original US accident data is at: https://www.kaggle.com/sobhanmoosavi/us-accidents
The dataset used in this assignment contains information about US traffic accidents
collected from February 2016 to March 2019 in 49 states of the US. This dataset was and
released in academic papers [1] and [2] and retrieved from
https://www.kaggle.com/sobhanmoosavi/us-accidents. This dataset is collected using realtime
traffic APIs from information from states’ department of transportation, law enforcement
agencies, traffic cameras and traffic sensors.


### Aspects of big data ###
The dataset has 49 columns with 2,243,939 entries. The attributes are information about
accidents including time, location, weather conditions, visibility and description. Total data
size is 819 Mb in one CSV file.
Aspects of big data present in this data:
- Volume: In terms of size, the dataset has about 2.25 million records with 49 attributes
and its size is big (819 Mb). In terms of complexity, this dataset is also collected from
many resources such as text records from states’ department of transportation and
numerical values from traffic cameras and traffic sensors.
- Velocity: This dataset is collected in real-time from traffic sensors and traffic
cameras.

### Data PreProcessing ###

All steps involved with Data Exploration, Processing, and Cleaning are implemented with
Jupyter Notebook using Python libraries such as Pandas and Numpy. Data Visualisation is
implemented using Matplotlib and Pyplot.

Data Import: To import the data, Pandas library with function read_csv(path_to_file) is used
to load in the CSV file.

Data exploration: To have a summary of the CSV file, Pandas.info() function is used to
display the number of entries, number of columns and types of attributes. Pandas.head()
method is then used to display the first 5 entries to explore the attributes.

Data Cleaning: the method isnull().sum() is used to check the number of null values. To
answer the two questions mentioned in the Abstract, information in column ‘State’ and
‘Severity’ is needed to count the number of accidents and to calculate the mean of severity
of accidents occurred in each state. Since there is no null value in these columns, data
cleaning is not necessary in this case.

Data Processing: To get the number of accidents in each state, Pandas function
count_values() is used to count the number of appearances of each state in the State
column. To get the mean of severity in each state, the method mean() is used followed by a
round(2) method to round the mean to 2 digits to calculate the mean of values in column
Severity.


### References ###

[1] Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv
Ramnath. “A Countrywide Traffic Accident Dataset.”, 2019.

[2] Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu
Teodorescu, and Rajiv Ramnath. "Accident Risk Prediction based on Heterogeneous Sparse
Data: New Dataset and Insights." In proceedings of the 27th ACM SIGSPATIAL International
Conference on Advances in Geographic Information Systems, ACM, 2019.






