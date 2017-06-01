# Valeria V. Rozenbaum
## Data Science and Visualization Portfolio

### Projects
#### US Exonerations 1989-2017
For my capstone project at General Assembly’s Data Science Immersion Program, I chose to work with the National Registry of Exonerations Database. For some background, the database was started in 2012 by the University of Michigan Law School, Michigan State University College of Law and the University of California Irvine Newkirk Center for Science and Society. It contains detailed information about all known individual exonerations in the United States.

For the modeling portion of the project, I did a panel regression to predict the total number of exonerations per state for 2017. For this to work, I had to double index the data by year and state, which allowed me to get my target variable of total exonerations per year for any given state. A correlation heatmap I had previously made showed me that the age and years served variables, both had positively correlated relationships with total exonerations. In order to use these as features for my model, I took the average age and average years served per state for every year. For the train/test portion, I split the data by years and used 1989–2010 as my training set and 2011–2017 for my testing set. In the end, my model gave me an adjusted R²score of 0.7105, meaning that I was able to explain 71% of the variance in my data.

- See the viz:
https://public.tableau.com/views/USExonerations1989-2017/StoryUSExonerations?:embed=y&:display_count=yes 

#### Web Scraping Indeed.com & Predicting Data Science Salaries
For this analysis, I built a webscraper to collect data science job listings from Indeed.com across 16 U.S. cities. After collecting over 10,500 listings, the database was then reduced to only include positions that listed annual salaries. The final dataframe of 493 observations was then assessed to determine a median salary. Several classification models were employed to determine what key factors (including location, key words, and job title) affected a job being above or below the median salary.

When determinging whether a job would be above or below the median, a significant factor included whether or not the job title included the terms "Machine Learning" or "Engineer". Further analysis showed that the city where the job is located, as well as the seniority of the role, weighed heavily on whether or not a position paid above median salary. The model developed can be used to test potential job postings to predict with 85 percent accuracy, whether the salary associated with the position should be above or below the median.

- See the viz:
https://public.tableau.com/profile/valeria.rozenbaum#!/vizhome/USDataScienceSalaryAnalysis/IndeedSalaryAnalysis 


#### Global Terrorism Database: Bayesian Inference and Imputation
The Global Terrorism Database (GTD) is a product of several years of work collating, classifying, and recording terrorist attacks around the world from 1970 to 2015. It has undergone several ownership changes and is currently housed at the University of Maryland. Since its procurement, the team at UMD have developed standardized modes of collectiona and recording information. However, because the database has traded hands so many times, a large amount of the pre-2011 data suffers from issues. Due to this, the database is excludes information for incidents that occurred in 1993. 
This project involved two portions:

- Applying Bayesian Inference to two populations of interest.
- Imputing the number of bombing incidents for 1993.

I used Bayesian inference to look at hostage barricade attacks in India and Pakistan post 2001. Narrowing my focus to these two populations translated to me working with a much smaller dataset, which meant that Bayesian analysis would be most fitting for the task. Unlike the frequentist approach, Bayesian inference does not assume a larger sample sizes in order to provide statistically viable results.
To impute the number of bombing attacks for 1993, I used a rolling mean to determine what values were likely. With this method, I took the rolling means for 1991 and 1992, as well as the means for 1994 and 1995. I then averaged them to arrive at my estimate of 1,417 bombing incidents.

- See the viz:
https://public.tableau.com/views/GlobalTerrorismDatabase-DataExploration/Story1?:embed=y&:display_count=yes


