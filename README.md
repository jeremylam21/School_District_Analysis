# School_District_Analysis

## Overview of the Analysis

The purpose of this analysis was to determine certain statistics regarding the performance of students and their respective schools. Further, a large portion of this analysis was cleaning the data in order to better represent performance and accurately calculate statistics. This was done by pulling data from the provided CSVs in order to create multiple DataFrames that help us compare the school performance based on metrics such as Budget per capita.


## Results

###  District Summary

When comparing the PyCitySchools_Challenge file with the PyCitySchools_Challenge-testing file, we see a few discrepancies that result from the new total student count performed earlier in the file. Other than the newly reflected Total Student number (from 39,170 to 38,709), we see lower "% Passing Math," "% Passing Reading," and "% Overall Passing" percentages although this is not reflected in the outputed tables since they are formatted. This carries over to all other measures that include Thomas High School, albeit quite marginally.

### School Summary

Other than the Thomas High School portion of the School summary (which we'll discuss in the follow section), the DataFrame remains mostly unchanged. By using the .groupby method in Pandas, we were able to group our initial expression by schools and then pass it into the dataframe to get the passing students for each subject matter (math & reading). 


### Thomas High School

Removing the 9th grade scores for Thomas High School lowered all of their passing percentages (math, reading, and overall). However, this did not affect their 2nd place standing - as shown by the top_schools DataFrame. 
For scores by school spending, we do see a significant difference since Thomas High Shool is no longer in any of the bins that were provided by the starter code. By removing 9th graders at Thomas High School, we have increased their spending per capita from $638 to $888.53. 
Scores by school size doesn't change much, since Thomas High School remains in the same sizing bin of "Medium" after removing 9th graders. As stated in the District Summary section passing math, reading and overall percentages are decreased marginally.
Scores by school type wasn't affected (despite marginal percentage decrease for charter school) since removing 9th graders from Thomas High School doesn't affect its type in the DataFrame. 


## Summary
There are four main differences that we can see from updating the school district analysis after reading and math scores for the ninth grade at Thomas High School have been changed. 
1.  Decrease in math, reading, and overall percentages across all measures (marginal enough to not be reflected after formatting)
2.  Decrease in average math and reading scores across all measures (marginal enough to not be reflected after formatting)
3.  Change in average scores due to a new student total which excludes Thomas High School 9th graders
4.  Change in spending per capita for Thomas High School
