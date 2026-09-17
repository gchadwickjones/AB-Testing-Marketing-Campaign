# A/B Testing: Marketing Campaign
This project looks at the effectiveness of a marketing campaign, measured by the proportion of users who had converted. This data set contains users who were shown either a public service announcement 
`(PSA)` or an advertisement `(ads)`, allowing the conversion rates of the two groups to be compared through hypothesis testing. 
I wanted to find out whether there was a meaningful difference between the two groups and whether the number of advertisements a user saw, and variables related to a user's engagement with the advertisement, 
had an impact on their conversion rates. 
This project therefore consists of both statistical analyses and supportive exploratory data analysis. 

## Initial Exploratory Analysis
The first stage of the project involved exploring the dataset to understand its structure and the characteristics of the users included in the experiment. 

I looked at the number of users in both the control and test group, and examined the distribution of the conversion rates between both groups. This allowed for an initial view of how the two groups compared
before carrying out the statistical analysis. 

The dataset contained `588,101` users, the majority of which belonged to the test group (`ads`). The initial exploration also revealed that the number of conversions was relatively small when compared against the
number of users. 

I also explored the number of advertisements shown to users and some of the other variables relating to their interaction with the advertising campaign. This helped to identify patterns that could be
investigated further during analysis. 

<img width="846" height="854" alt="image" src="https://github.com/user-attachments/assets/11a53d7e-04b4-4793-acea-ed225baf8ec3" />

## Statistical Analysis
The main statistical analysis focussed on whether the conversion rate was different for the control group (`PSA`) and the test group (`ads`). **The test group had a conversion rate of `2.55%` compared with 
`1.79%` for the control group.**

A **two-proportion z-test** was then used to determine whether the observed difference between the control and test groups had statistical significance. The test gave a z-statistic of `7.37` and a p-value of `1.71x10⁻¹³`. The p-value
is significantly below the threshold of statistical significance, and we can therefore reject the null hypothesis with confidence. 

The **95% confidence interval** for the difference in conversion rates was approximately `0.60` to `0.94` percentage points, meaning the estimated difference was positive across the confidence interval.

<img width="2970" height="1019" alt="conversion_rate_confidence_interval" src="https://github.com/user-attachments/assets/1de693c7-911d-466a-bad1-52f6558efa12" />


## Supporting Exploratory Analysis
Following the main statistical analysis, I explored variables related to the users' engagement with the advertisement. This included viewing the conversion rate in relation to the number of ads viewed, the hour of day that most ads were viewed
as well as the day of week that the user viewed the most ads. 
It was found that conversion rates varied across different levels of advertisement exposure. This gave additional context around the A/B test and highlighted how user engagement with the campaign could be 
explored beyond simply comparing the two experimental groups.

However, this part of the analysis is observational and therefore does not establish causality, but only associations. 

<img width="842" height="1008" alt="84755487" src="https://github.com/user-attachments/assets/0cad0997-6820-46a2-a7c3-413efe3a27d5" />


## Methodology
The project consists of the following stages:
- Data cleaning and preparation
- Initial exploratory Analysis
- Comparison of conversion rates between the experimental groups
- Calculation of absolute difference and relative lift
- Two-proportion z-test
- Calculation of a 95% confidence interval
- Exploratory analysis of advertisement exposure and conversion
- Interpretation of the results

## Data
This project uses the `marketing_AB.csv` dataset, found on Kaggle. It contains 588,101 user observations from an online marketing experiment.

The main variables used were:
* Experiment group — whether the user was shown the advertisement or PSA
* Total advertisements — the number of advertisements shown to the user
* Converted — whether the user converted
* Other engagement variables — variables describing the user’s interaction with the advertising campaign

## Tools & Technologies

* Python
* pandas
* NumPy
* Matplotlib
* Seaborn
* Statistical hypothesis testing
* Jupyter Notebook

## Limitations 
The main A/B test compares two experimental groups, but the supportive analysis is only observational. Additionally, other factors that may impact conversion are also not considered in the analysis, and it
is not clear whether the users in each experimental group were randomly assigned. 

## Conclusion
The `test group` was found to have a higher conversion than the `control group`, which was found to be statistically significant following hypothesis testing using a two-proportion z-test.  The supporting analysis also found differences in conversion across levels of advertisement exposure, although these relationships should not be interpreted as evidence of causation.
Overall, this analysis demonstrates how hypothesis testing and data analysis can be used together to investigate the effectiveness of a marketing campaign. 
