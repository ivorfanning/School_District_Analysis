# Project Overview and purpose

The school board asked for a summary of key metrics by each school name and by the district level in their area. The main analysis focused on the performance of math and reading scores. However, the school board found that the data from Thomas High School's 9th grader was altered after reviewing all the data, so the school board asked for the 9th grade data of Thomas High School to be removed and do the analysis again.

# Resources

-Data Source: schools_complete.csv,  students_complete.csv

-Software:  Python 3.7.6, 
            Jupyter notebook, 6.4.8

## Re-analysis results:

### How is the district summary affected?

Original district summary 
![original district summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20district%20summary.png)

*Firstly we need to count the number of student of 9th grade in Thomas Hight School by using the following code and the result turns into __461__ student on 9th grade in Thomas High School.*

```
thomas_9th = student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th")]

thomas_9th_student_count = thomas_9th["student_name"].count()
```
Adjusted district summary 
![adjusted district summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20district%20summary.png)

*After substracting the student of 9th grade in Thomas High School, we have a new total student count 38709.*
*From the above two tables we can tell the change by removing 461 students score from a 39170 student set is less than 0.5%, which we can still round the percentage to the same whole number as original analysis.*

### How is the school summary affected?

Original school summary 
![original school summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20per%20school%20summary.png)

Adjusted school summary 
![adjusted school summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20per%20school%20summary.png)

*From the above two tables, we can see the percentage of passing math, reading, or both are slightly changed by 0.5%, removing the 9th grade students in THS does not significantly affect the school summary.*

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Original school top 5
![original top 5](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20school%20top%205.png)


Adjusted school top 5
![adjusted top 5](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20school%20top%205.png)

*As we stated before, the percentage changed slightly does not affect the Thomas High School's ranking in the district.*

### How does replacing the ninth-grade scores affect the following:


#### Math and reading scores by grade

Original math score summary(Left table) & Adjusted math score summary(Right table)

![original math score by grade](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20math%20score%20by%20grade.png)
![adjusted math score by grade](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20math%20score%20by%20grade.png)

Original reading score summary(Left table) & Adjusted reading score summary(Right table)

![original reading score by grade](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20reading%20score%20by%20grade.png)
![adjusted reading score by grade](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20reading%20score%20by%20grade.png)

*Due to removing the 9th grader's math and reading scores, the math and reading scores of 9th grader in Thomas High School are substituted by NaN as we can see in the below tables, however the scores of other school and the 10th-12th grader in Thomas High School are remain intacted.*

#### Scores by school spending

Original spending summary

![original spending summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20spending%20summary.png)

Adjusted spending summary

![adjusted spending summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20spending%20summary.png)

*The Spending of Thomas High School falls into the group of $631-$645, the change is also under 0.5%, this should not affect any decision concluded from the spending summary. Other numbers remain the same.*

#### Scores by school size

Original school size summary

![original school size summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20school%20size%20summary.png)

Adjusted school size summary

![adjusted school size summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20school%20size%20summary.png)


*The size of Thomas High School falls into the medium group, so the change is only showed in the medium group, same as before, the number changed under 0.5%, Other numbers remain the same.*

#### Scores by school type

Original school type summary

![original school type summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/original%20school%20type%20summary.png)

Adjusted school type summary

![adjusted school type summary](https://github.com/ivorfanning/School_District_Analysis/blob/main/Analysis%20Pictures/Adjusted%20school%20type%20summary.png)

*The type of Thomas High School is charter, so the change is only showed in the charter category, same as before, the number changed under 0.5%, Other numbers remain the same.*

# Summary: 

*As we compared all the original tables and adjusted tables, we found a fact which is after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs, the change is tiny since very small portion of data is removed from a very large polulation of data, in another words the effect is under 0.5%.*





