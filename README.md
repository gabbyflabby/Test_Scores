# mod2project

## About

#### Source:
We took our data from a MIT course assignment linked here.
https://ocw.mit.edu/courses/sloan-school-of-management/15-071-the-analytics-edge-spring-2017/linear-regression/assignment-2/reading-test-scores/

#### Our Data at a glance:
Our subset contains information about the demographics and schools for American students taking the exam, derived from 2009 PISA Public-Use Data Files http://nces.ed.gov/pubsearch/pubsinfo.asp?pubid=2011038                                                  
(PISA) The Programme for International Student Assessment is a test given every three years to 15-year-old students from around the world to evaluate their performance in mathematics, reading, and science. 

#### Features of our data:

* grade: The grade in school of the student (most 15-year-olds in America are in 10th grade)
* male: Whether the student is male (1/0)
* raceeth: The race/ethnicity composite of the student
* preschool: Whether the student attended preschool (1/0)
* expectBachelors: Whether the student expects to obtain a bachelor's degree (1/0)
* motherHS: Whether the student's mother completed high school (1/0)
* motherBachelors: Whether the student's mother obtained a bachelor's degree (1/0)
* motherWork: Whether the student's mother has part-time or full-time work (1/0)
* fatherHS: Whether the student's father completed high school (1/0)
* fatherBachelors: Whether the student's father obtained a bachelor's degree (1/0)
* fatherWork: Whether the student's father has part-time or full-time work (1/0)
* selfBornUS: Whether the student was born in the United States of America (1/0)
* motherBornUS: Whether the student's mother was born in the United States of America (1/0)
* fatherBornUS: Whether the student's father was born in the United States of America (1/0)
* englishAtHome: Whether the student speaks English at home (1/0)
* computerForSchoolwork: Whether the student has access to a computer for schoolwork (1/0)
* read30MinsADay: Whether the student reads for pleasure for 30 minutes/day (1/0)
* minutesPerWeekEnglish: The number of minutes per week the student spend in English class
* studentsInEnglish: The number of students in this student's English class at school
* schoolHasLibrary: Whether this student's school has a library (1/0)
* publicSchool: Whether this student attends a public school (1/0)
* urban: Whether this student's school is in an urban area (1/0)
* schoolSize: The number of students in this student's school
* readingScore: The student's reading score, on a 1000-point scale

#### Goal:
We will try to predict the reading scores of students from the United States of America on the 2009 PISA exam. Using Linear Regression models such as OLS (ordinary least squares), Polynomials, Ridge, and Lasso.
Read on to see what we got! 

## Preprocessing

#### Null values
In the image below you can see the columns with the count of null values and what percentage of that column is null.
<img src="Images/Columns_and_nulls.png" style="width:150px;height:70px" align="center">

As you can see the columns about if the parents have a bachelor degree has more than 10% null values. There is a risk that these parents were simply embarassed and therefore did not provide their information, therefore, if we simply drop these nulls we may be introducing some bias to our datasets. We concluded it was best to drop these two columns.
For the rest of the dataset, we simply dropped the rows with null values.


#### Outliers

Since our dataset included some extreme outliers we went with a conventional route of removing them.
We found our Upper fence and Lower fence and removed everything outside of them.
The formula is:
Upper fence = Q3 + (1.5 * IQR)
Lower fence = Q1 – (1.5 * IQR)
Where IQR is the interquartile range


## Exploratory Data Analysis

???
insert images


## Hypothesis Testing

#### Students with working parents vs non working parents
Does having both parents who don't work influence the childs reading score?
We've found a statistical significant difference between the mean reading scores for those with working parents vs without.
Average score for students with at least one working parent:
Avergae score for students with parents who don't work: 

#### Students who speak english at home vs those who do not
This one seems quite logical, if the language spoken at home is not English will that affect the childs reading score?
We've found a statistical significant difference between the mean reading scores for those who speak English at home vs those who don't.
Average score for students who speak english at home:
Avergae score for students who don't speak english at home:

#### Students with a parent that graduated high school vs those without one
If a student has a parent with a high school diploma will that student perform differently on the reading test?
As it turns out that student will indeed perform differently on average.
Average score for students with a parent who graduated High school:
Avergae score for students with parents who didn't graduate High school:

#### Students who attend public school vs those who don't
Public vs Private school will there students perform the same on the reading test?
Well we can assure you that according to our data they will not perform the same on average.
Average score for students from Public schools:
Avergae score for students from Private schools:

#### Students with a parent from the US vs those without one
If a students parents are not from the US will that have an influence on that students reading score?

Average score for students with
Avergae score for students with

#### Average reading score for students of different races
We were unable to perform Anova testing since some of the races in our dataset are not presented with enough datapoints
<img src="Images/Races_and_mean_scores.png">

## Regression Model

#### OLS

R squared:
RMSE: 

#### Polynomial

R squared:
RMSE: 

#### Ridge

R squared:
RMSE:

#### Lasso

R squared:
RMSE: 



## Conclusion & next steps

Being that most of the collected data is binary or categorical it seems that a linear model won't be sufficient to predict student test scores. 





