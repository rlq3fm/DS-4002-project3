# DS-4002-Project3


## Repository Contents
This repository contains the files and information related to the third project done by Lauren Smith, Ann Sofo and Reese Quillian in the DS 4002 Project Course. In this project we explored the question: Has crime in Charlottesville grown since we started at UVA? Our hypothesis was that there is an increasing trend of the crime rate in Charlottesville.


## SRC


### Overview
There are multiple R markdown files in the src folder that contain all code used to clean our data (P3 Data Preparation.Rmd), perform exploratory data analysis (Project3EDA.Rmd), and build/evaluate our model (Project3Model.Rmd). These files can be opened with RStudio and also be knitted into an html document upon opening of the files in the application to produce a more readable format. 


### Code Usage
In order to successfully run the code chunks in the R Markdown files, a few packages need to be installed. When opening the file in RStudio, a message at the top of the source code will ask you if you would like to install the required packages. Click install. Then run the first code chunk at the top of each file which reads in the required packages. For the EDA and Model R markdown files, download the CSV files in the data folder of the repository that were produced by the Data preparation file and set your working directory to their location.

## Data
Our crime data is provided by the government of Charlottesville’s open data website, which is updated nightly and includes data from 2018 to 2023 [1]. All attributes of the crime data originate from the initial information provided by individuals calling for police assistance, along with all other information collected by the caller at that time. Before any pre-processing, there are eight variables in the original dataset: Offense, IncidentID, BlockNumber, StreetName, Agency, DateReported, HourReported, and ReportingOfficer. For the purpose of our analysis, we will only be working with the DateReported and Offense variables and other variables that branch from them. We use observations from 2018-2022 as our training data and observations from 2023 as our test data.

### Data Dictionary
| Variable Name  | Description  |
|---|---|
| Offense  | The type of offense reported (Larceny, Assault, etc.)  |
| GroupA  | An indicator of whether the reported offense is a ‘Group A’ crime: a serious offense that we believe to be increasing (0 = No, 1 = Yes)  |
| GroupB  | An indicator of whether the reported offense is a ‘Group B’ crime: an offense that we don’t believe to be increasing (0 = No, 1 = Yes)  |
| Assault  | Whether or not the offense is identified as the first crime included in GroupA, Assault (0 = No, 1 = Yes) |
| ShotsFired_IllegalHunting  | Whether or not the offense is identified as the second crime included in GroupA, Shots Fired/ Illegal Hunting  (0 = No, 1 = Yes)  |
| Suspicious_Persons_Activity  | Whether or not the offense is identified as the third crime included in GroupA, Suspicious Persons or Activity  (0 = No, 1 = Yes) |
|  Date | The date the incident was reported in ‘yyyy-mm-dd’ format  |
| Year  | The year the incident was reported  |
|  Month | The month the incident was reported  |
| Hour  | The hour the incident was reported  |
| Weekday  | The day of the week the incident was reported (Mon, Tues, etc.) |
| NumCrimes | Number of incidents reported per day |



## Figures


## References
[1] Private Member, “Crime Data.” Charlottesville Open Data, City of Charlottesville, 29 June 2017, https://opendata.charlottesville.org/datasets/charlottesville::crime-data/about. 
[2] E. Howell, “Autocorrelation For Time Series Analysis,” Medium, Dec. 28, 2022. https://towardsdatascience.com/autocorrelation-for-time-series-analysis-86e68e631f77 
[3] “Shootings are up in and around Charlottesville. Officials can’t explain why.,” The Daily Progress, Mar. 11, 2023. https://dailyprogress.com/news/shootings-are-up-in-and-around-charlottesville-officials-cant-explain-why/article_d1a82dca-bf89-11ed-a787-83a86877ca98.html 
[4] sherlockj, “UVa Takes Steps to Protect Students from Increasing Crime in Charlottesville,” Bacon’s Rebellion, Mar. 25, 2023. https://www.baconsrebellion.com/wp/uva-takes-steps-to-protect-students-from-increasing-crime-in-charlottesville/ 
[5] C. Shetty, “Time Series Models,” Medium, Sep. 22, 2020. https://towardsdatascience.com/time-series-models-d9266f8ac7b0 
‌[6] “The Box-Jenkins Method,” NCSS Statistical Software, 2022. [Online]. Available: https://www.ncss.com/wp-content/themes/ncss/pdf/Procedures/NCSS/The_Box-Jenkins_Method.pdf 


