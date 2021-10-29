# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Table of Contents
* Problem statement
* Data Dictionaries
* Observations and Data Analysis
* Conclusions and Recommendations
​
### Overview
​
“When you educate one person you can change a life, when you educate many you can change the world”- Shai Reshef
​
The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). SAT has different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)


### Problem Statement
​We want to identify the relationship between <b> County Income</b> and <b> SAT Participation Rate</b>.
Should there be positive correlation, we want to propose qualitative solutions to improve SAT participation rates of students from lower-income counties.



​
## Who Are We?
​
We are data scientists working with the board of directors from College Board of California. We are concerned about the educational standards in California. 


### Datasets
​
These are the datasets that we will be utilising from the [`data’](./data/) folder for this project.

* [`sat_2017.csv’](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv’](./data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv’](./data/sat_2019.csv): 2019 SAT Scores by State
* [`sat_2019_ca.csv’](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School
* [`median_household_income_by_county.csv’](./data/median_household_income_by_county.csv): Median Household Income by County


​
## Data Dictionaries
​
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|2017 SAT Scores by State|States in the USA
|**participation_2017**|*float*|2017 SAT Scores by State|Participation rates for SAT in 2017 by state
|**ebrw_2017**|*float*|2017 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2017 by state
|**math_2017**|*float*|2017 SAT Scores by State|Average SAT Mathematics Score in 2017 by state
|**total_2017**|*float*|2017 SAT Scores by State|Average SAT Total Score in 2017 by state, where Total = Math + EBRW
|**participation_2018**|*float*|2018 SAT Scores by State|Participation rates for SAT in 2018 by state
|**ebrw_2018**|*float*|2018 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2018 by state
|**math_2018**|*float*|2018 SAT Scores by State|Average SAT Mathematics Score in 2018 by state
|**total_2018**|*float*|2018 SAT Scores by State|Average SAT Total Score in 2018 by state, where Total = Math + EBRW
**participation_2019**|*float*|2019 SAT Scores by State|Participation rates for SAT in 2019 by state
|**ebrw_2019**|*float*|2019 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2019 by state
|**math_2019**|*float*|2019 SAT Scores by State|Average SAT Mathematics Score in 2019 by state
|**total_2019**|*float*|2019 SAT Scores by State|Average SAT Total Score in 2019 by state, where Total = Math + EBRW
|**County**|*string*|2019 SAT Scores in California by School|Counties in the state of California
|**enroll_12**|*float*|2019 SAT Scores in California by School|Enrollment for Grade 12 by county
|**tst_tkr_12**|*float*|2019 SAT Scores in California by School|Number of SAT takers in Grade 12 by county
|**num_erw_bm_12**|*float*|2019 SAT Scores in California by School|Number of students meeting the Evidence-Based Reading & Writing (ERW) benchmark established by based on the New 2016 SAT test format as of March 2016 for Grade 12
|**pct_erw_bm_12**|*float*|2019 SAT Scores in California by School|Percentage of students who meet or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12
|**num_math_bm_12**|*float*|2019 SAT Scores in California by School|Number of students who met or exceeded the benchmark for the New 2016 SAT Math test format as of March 2016 for Grade 12
|**pct_math_bm_12**|*float*|2019 SAT Scores in California by School|Percentage of students who met or exceeded the benchmark for SAT Math test for Grade 12
|**enroll_11**|*float*|2019 SAT Scores in California by School|Enrollment for Grade 11 by county
|**tst_tkr_11**|*float*|2019 SAT Scores in California by School|Number of SAT takers in Grade 11 by county
|**num_erw_bm_11**|*float*|2019 SAT Scores in California by School|Number of students meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11
|**pct_erw_bm_11**|*float*|2019 SAT Scores in California by School|Percentage of students who meet or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11
|**num_math_bm_11**|*float*|2019 SAT Scores in California by School|Number of students who met or exceeded the benchmark for the New 2016 SAT Math test format as of March 2016 for Grade 11
|**pct_math_bm_11**|*float*|2019 SAT Scores in California by School|Percentage of students who met or exceeded the benchmark for SAT Math test for Grade 11
|**num_both_bm_12**|*float*|2019 SAT Scores in California by School|Number of students who met the benchmark for Evidence-Based Reading & Writing (ERW) and Math Grade 12
|**pct_both_bm_12**|*float*|2019 SAT Scores in California by School|Percentage of students who met the benchmark for Evidence-Based Reading & Writing (ERW) and Math Grade 12
|**num_both_bm_11**|*float*|2019 SAT Scores in California by School|Number of students who met the benchmark for Evidence-Based Reading & Writing (ERW) and Math Grade 11
|**pct_both_bm_11**|*float*|2019 SAT Scores in California by School|Percentage of students who met the benchmark for Evidence-Based Reading & Writing (ERW) and Math Grade 11
|**participation_rate_12**|*float*|2019 SAT Scores in California by School| SAT participation rate for Grade 12 by county
|**participation_rate_11**|*float*|2019 SAT Scores in California by School|SAT participation rate for Grade 11 by county
|**median_hh_income**|*integer*|2019 California Median Household Income|The annual median household income by county in California for 2019 

​
## Observations and Data Analysis


The chart shows that Grade 11 Participation Rate vs Median Household Income has a correlation of 0.56 and Grade 12 Participation Rate vs Median Household Income has a correlation of 0.69. 

Hence, Median household income is correlated to SAT participation as there is a strong positive correlation (>0.5) between income and SAT participation rate. We SAT Participation rate. Research also shows that parental income has a substantial effect on academic achievement and accounts for a meaningful proportion of the score gap between high income families and the low income families.  

![](data/income and SAT participation rates for both Grades 11 and 12.jpg)
![](data/Median Household Income vs SAT Participation Rate.jpg)

In order to increase the participation rate, some of the strategies include offering SAT at no cost, free access to the college Board’s official SAT online course, conducting SAT exam during school hours with transportation provided and engagement with the school couunselor.  



​ ## Conclusions and Recommendations
We believe it’s possible to increase the participation rate because Delaware and Idaho have implemented SAT at no cost to students since 2011 and 2012 respectively. The program is offered to all 11th grade students who enrolled in the public schools. The students are able to complete the exam during a regular school day instead of the non school day. Additionally, in order to prepare students to complete the SAT successfully, the Delaware Department of Education provides all 11th grade students enrolled in public schools with free access to the College Board’s Official SAT Online Course. Individual districts have also implemented their own SAT preparation programs; for instance, Red Clay Consolidated School District offers a seven‐week SAT prep class free of charge.

Conducting SAT exam during regular school hours with transportation provided. This can reduce potential Saturday testing barriers (e.g., part-time jobs, family responsibilities). A research found that earnings supplements do matter for children’s academic achievement in poor families. 

The College Board reports obtaining a fee waiver does not guarantee test participation. The two most common reasons for test day absenteeism among fee‐waiver recipients were 1) feeling unprepared and 2) not having transportation. Fee‐waiver recipients indicated that the school counselor was the most important influence in deciding whether to register, and they would have been more likely to be present on test day with more encouragement, increased accessibility to test centers, and more preparation. Hence, it is important for students to be confident by having more SAT prep class and engagement with the school counsellor. 


​
---
​
### Citations and References
​
1. Camara, W. J. & Schmidt, A. E. (1999). Group differences in standardized testing and social stratification. College Board Report (99)5. New York, NY: College Board.
2. Zwick, R.  (2004). Is the  SAT a “Wealth Test”? The  link between educational achievement and socioeconomic status (pp. 203–216). In R. Zwick, (Ed.). Rethinking the SAT in university admissions. New York, NY: Routledge Falmer.
3. “Free SAT registration now open for public school juniors.” Delaware PTA, February 10, 2014. http://delawarepta.org/free‐sat‐registration‐now‐open‐for‐public‐school‐juniors/
4. Adams, C. “Delaware Gives All Juniors SAT During School Day.” Education Week, January 25, 2011. http://blogs.edweek.org/edweek/college_bound/2011/01/all_high_school_juniors_in_delaware_take_sat_starting_in_april.html
5.  “SAT.” Idaho State Department of Education. http://www.sde.idaho.gov/site/assessment/SATstudentParent.htm 
6. Duncan, G. J., Huston, A. C., & Weisner, T. S. (2007). Higher ground: New hope for the working poor and their children. New York: Russell Sage Foundation.
7. Rothstein, R. (2004). Class and schools: Using social, economic, and educational reform to close the Black-White achievement gap. Washington, DC: Economic Policy Institute.
8. Sirin, S. R. (2005). Socioeconomic status and academic achievement: A meta-analytic review of research. Review of Educational Research, 75(3), 417–453.
9. Mattern KD, Shaw EJ, & Williams FE (2008). Examining the relationship between SAT, high school measures of academic performance and socioeconomic status: Turning our analysis to unit of measure. College Board Publications. 
10. Zwick R, Brown T, & Sklar JC (2004). California and the SAT: A reanalysis of University of California admissions data Center for Studies in Higher Education, UC Berkeley, Research and Occasional Papers Series; Retrieved January 11, 2013 from http://cshe.berkeley.edu/publications/rops.htm. 
11. https://www.census.gov/search-results.html?q=california+median+income&page=1&stateGeo=none&searchtype=web&cssp=SERP&_charset_=UTF-8