# PyCitySchools Pandas Challenge MOD 4 (Week 4)
Analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. The task is to aggregate the data to showcase obvious trends in school performance.

# PyCity Schools Analysis

Analysis Summary

The district has a total of 15 schools, 7 District and 8 Charter schools with District schools performing better in reading than math scores. The District schools lower math percentage scores lowers the overall passing (math and reading) percentage for the district. 
Theres no distinct correlation between school spending per student and student scores either positive or negative. But there is a drop in average math scores for the two higher per student spending range (630-645 and 645-680). Huang High school spends the most per student but has the lowset average math scores (76.8). Reviewing the "Highest and Lowest performing by overall % score" data set and comparing total school budget, theres no correlation in budget and scores performance but there is a corre;lation between school size and performance scores.

Obervable trend/Correlation 1

Charter schools perform better then distric schools across all score metrics, specifically in reading (94% charter vs 67% district). 

Observable trend/Correlation 2

Small to medium schools perform about equally to each other but both perform overall better then large schools, specifically in the percentage of passing math, which drops significantly (30%) in large schools. 

## District Summary

15 schools total with total 39,170 total students
    8 Charter Schools
    7 District Schools
The District performs better overall reading scores over math scores, but overall total students passing is low at 65%

## School Summary
Spending per capita is overall even between District and Charter schools although Charter schools have less students.

## Highest-Performing Schools (by % Overall Passing)
Charter schools appear to perfoem better across all metrics

## Bottom Performing Schools (By % Overall Passing)
District schools appear to perform worst overall while having the most spending per capita

_____________________________________________________________________________________________________________________

## Instructions
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

## District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:
- Total number of unique schools
- Total students
- Total budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

## School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:
- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

## Highest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in descending order and display the top 5 rows and save the results in a DataFrame called "top_schools".

## Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows and save the results in a DataFrame called "bottom_schools".

## Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

## Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

## Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).
Use the code provided below to create four bins with reasonable cutoff values to group school spending.
    - spending_bins = [0, 585, 630, 645, 680]
    - labels = ["<$585", "$585-630", "$630-645", "$645-680"]

Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.
    - spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
    - spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
    - spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
    - spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
    - overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()

Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

## Scores by School Size
Use the following code to create three bins with reasonable cutoff values to group school size.
    - size_bins = [0, 1000, 2000, 5000]
    - labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]

Use pd.cut to categorize school size based on the bins.
Use the following code to then calculate mean scores per size range.
    - size_math_scores = school_size_df.groupby(["School Size"])["Average Math Score"].mean()
    - size_reading_scores = school_size_df.groupby(["School Size"])["Average Reading Score"].mean()
    - size_passing_math = school_size_df.groupby(["School Size"])["% Passing Math"].mean()
    - size_passing_reading = school_size_df.groupby(["School Size"])["% Passing Reading"].mean()
    - size_overall_passing = school_size_df.groupby(["School Size"])["% Overall Passing"].mean()

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

## Scores by School Type
Use the per_school_summary DataFrame to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".

Note:
This homework was loooong, frustrating, and extremely challenging. But overall I do appreciate it because it provided enough exercises to reference and learn pandas and jupyter notebook. 
