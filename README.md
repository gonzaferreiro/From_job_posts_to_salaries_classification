# From job posts to salaries classification

## Business Case Overview

For any expanding business working with Data Scientists, it's hard to keep up to date being competitive in the hiring market. That's why this project gathered tons of job posts publications in order to answer the following questions:

   1. Industry factors that are most important in predicting the salary amounts for these data.
   2. Factors that distinguish job categories and titles from each other. 

To limit the scope we *focus on data-related job postings*, e.g. data scientist, data analyst, research scientist, business intelligence, in between others. Only within the UK.

**Final goal:** Scrape our own data from Indeed.com in order to collect the data to best answer our questions.

---

### QUESTION 1: Factors that impact salary

To predict salary out from job posts we developed a classification problem, dividing each publication in four categories according to percentiles (P25, P50, P75 and up) using features like the location, title, and summary of the job. At the end, we analyzed the feature importance for each category, using the scraped predictors and the features engineered.

### QUESTION 2: Factors that distinguish job category

Using the job postings scraped for part 1 we tried to identify features in the data related to job postings that can distinguish job titles from each other. 

We could also perform Linear Regression (or any regression) to predict the salary value here. Instead, we are going to convert this into a _binary_ classification problem, by predicting two classes, HIGH vs LOW salary.

While performing regression may be better, performing classification may help remove some of the noise of the extreme salaries. We don't have to choose the `median` as the splitting point - we could also split on the 75th percentile or any other reasonable breaking point.

#### We started up with a binary problem, using only the location as a feature to experiment:

- Logistic regression using both statsmodels and sklearn.
- Further classifiers.
- Features scaling.
- Coefficients/feature importances with a short summary of what they mean.

#### Later, we model taking into account more categories and models:

- Creating a few new variables in the dataframe to represent interesting features of a job title.
- Incorporating other text features from the title or summary that you believe will predict the salary.
- Then buildinf new classification models including also those features.
- Tuning our models by testing parameter ranges, regularization strengths, etc. 
- Discussing model coefficients or feature importances as applicable.

Finally, let's suppose we're working for a company, for which our boss would rather tell a client incorrectly that they would get a lower salary job than tell a client incorrectly that they would get a high salary job. We tried to adjust one of our models to ease his mind, and explain what it is doing and any tradeoffs.

The conclusions of this project can be found in the following document:

#### **[CONCLUSIONS](./Conclusions.pdf)**
