# Cyclistic Bike-Share Analysis Case Study


## Introduction
For this case study I am a junior data analyst working in the marketing analyst team at the fictional company Cyclistic. Cyclistic is a bike-share company based in Chicago, Illinois. Cyclistic has 5,824 bycicles that are locked into a network of 692 stations across Chicago. Pricing plans for the bikes are single-ride passes, full-ride passes, and annual memberships. Customers who purchase the single or full ride passes are considered casual riders and customers who purchase annual memberships are considered annual members. Lily Moreno, my manager and director of marketing at Cyclistic, wants to find out how to convert casual riders into annual members. Moreno has assigned me to figure out how annual members and casual riders use Cyclistic bikes differently?  For this case study I will follow the six steps of the data analysis process that I have learned from Coursera's Google Data Analytics Certificate. The six steps are ask, prepare, process, analyze, share, and act. Lets get started!



## Ask
For the ask part of the data analysis step I identify the business task and consider key stakeholders. Then considering both, state the clear business task.

**Identifying the Business Task**: Cyclistcs financial analysts have concluded that annual members are much more profitable than casual riders. So Moreno wants me to analyze the differences between casual members and annual members so that the team can design marketing strategies aimed at converting casual riders into annual members.

**Key Stakeholders**: Stakeholders would be Moreno, the rest of the marketing analytics team, and the Cyclistic executive team.+

**Business Task**: Analyze the key differences between casual and annual members and report to my manager so that the team can design a marketing strategy to convert casual members to annual members that we will have to present to the Cyclistic executive team who will decide whether to approve said marketing strategy.



## Prepare
For the prepare part of the data analysis I will download the data and store it, identify how its organized, determine the credibility of the data so that I know I can use it in the later steps, decide what tools I will be using for the project, and load the data into the tools I will be using..

**Download Data**: For downloading the data I have download 12 different data sets on bike rides for the 12 months of 2021 and stored them in a folder that I created just for this project.

**How the data is organized**: Each dataset has 13 variables. Ride_id, rideable_type (what kind of bike), start time, end time, start station name, end station name, start station id, end station id, start latitude, start longitude, end latitude, end longitude. 

**Credibility**: These datasets are Cyclistics historical trip data. Using ROCCC as a guideline for credebility. For reliability I would say that the dataset is reliable and fit for use since all of the data are from transactions and are factual so we can make conclusions based on them. For originalm this is good because the data comes from Cyclistic and is thus first-party data. For comprehensive, this is okay because some of the values of the datasets are null but we wont be using the variables that have null values since they dont contribute much to the question at hand. For current, since the usefullness of data decreases as time passes we can give the go ahead for these datasets since they were only in 2021. For cited, this data comes from the company itself so it can be cited.

**Tools**: The tools I will be using for this project will be R and RStudio. I will also be using packages that RStudio offer. The packages are loaded below.

```markdown
library(tidyverse)
```

**Loading Data**:
For loading our data I will use the tidyverse package. Since we have 12 datasets to look at I want to combine all twelve into one dataset.
```
data_all = list.files(path="C:/Users/rgens/OneDrive/Desktop/RideShare", # Looks for all csv files in my folder and puts them in a list.
                      pattern="*.csv",full.names=TRUE) %>%
  lapply(read_csv) %>% # Applies the read_csv function to all objects in my list.
  bind_rows # Combines data into one dataset
head(data_all)
```


## Process
For the process part of the data analysis I will check my data for errors, transform the data so I can work with it effectively, and document the code through MarkDown.





