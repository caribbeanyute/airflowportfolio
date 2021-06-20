# Problem Statement (WIP)
There are flat files that need to be imported into a Relational Database,
each file contains time series data for a respective variable .ie, 
WINDSPEED(WDA),TEMP...

# Imposed Constraints
Files are classified into season (SUMMER,FALL..) each file contains time series data for the entire season, and one season must be processed per day.

Missing data, must be noted, ie for each time period indicate which if any columns has data missing.



# Approaches
Tools
a.) Process each file and insert values to its respective column into a single table based on the primary key.


WINDSPD.csv

2020/9/1 00:00:00,A,110.9,98.7,
2020/9/1 00:01:00,A,98.7,98.7,


| TIMESTAMP(DATETIME)(PK) | WINDSP1 | WINDSP2 | TEMP1 | ..... |
|-------------------------|---------|---------|-------|-------|
| 2020-XX-XX              | 89      | 89      | 90    | ....  |
|                         |         |         |       |       |
|                         |         |         |       |       |