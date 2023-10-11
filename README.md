# Capstone Project - Google Advanced Data Analytics
## User Churn Prediction

The Google Advanced Data Analytics Capstone Project revolves around Employee Churn Prediction, a pivotal aspect of workforce management. This project applies advanced analytics techniques to scrutinize employee behavior trends and forecast potential departures. Through the application of concepts learned in data cleaning, visualization, statistical analysis, and machine learning, the objective is to construct a resilient model that equips organizations with the foresight to retain their valuable talent pool.

#### Business Scenario and Problem:
At Salifort Motors, the HR department is eager to enhance employee satisfaction levels. They've gathered data from their workforce, but are seeking guidance on how to effectively leverage it. As a data analytics professional, I've been consulted to offer data-driven insights and recommendations based on my analysis of the provided data.

#### Procedure followed:
- Plan: Initial EDA, checking for missing values, evaluating response and explanatory variables
- Analyze: Continue EDA, checking for outliers, analyzing relationships between variables
- Construct: Determine which models are appropriate, setting and confirming model assumptions, constructing ML model
- Execute: Recall evaluation metrics, interpret model performance and results, share key findings
  
#### Key Findings Extracted

![ss1](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss1.png)

#Note: '1' represents the employees who left and

It's natural that individuals handling more projects tend to invest more hours, as evident in the increasing mean hours for both groups (stayed and left) with project count. However, a few notable patterns emerge from this analysis.
- Among those who left the company, there are two distinct groups: (A) employees who worked significantly fewer hours compared to their counterparts on similar projects, and (B) those who put in considerably more hours. Group A may include individuals who were potentially let go, while it's plausible that this group also encompasses employees who had already given notice and had reduced workloads in preparation for departure. Group B likely consists of individuals who resigned, and their extensive contributions to projects are noteworthy.
- All employees with seven projects ultimately left, and both this group and those who left with six projects had interquartile ranges around 255–295 hours per week much higher than any other cohort.
- The ideal project load for employees appears to be in the range of 3–4. These groups show a very low ratio of departures to retentions.

![ss2](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss2.png)

- The scatterplot above shows that there was a sizeable group of employees who worked ~240–315 hours per month. 315 hours per month is over 75 hours per week for a whole year. It's likely this is related to their satisfaction levels being close to zero.
- The plot also shows another group of people who left, those who had more normal working hours. Even so, their satisfaction was only around 0.4. It's difficult to speculate about why they might have left. It's possible they felt pressured to work more, considering so many of their peers worked more. And that pressure could have lowered their satisfaction levels.
- Finally, there is a group who worked from 210–280 hours per month, and they had satisfaction levels ranging from 0.7–0.9.

![ss3](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss3.png)

Employees who left fall into two general categories: dissatisfied employees with shorter tenures and very satisfied employees with medium-length tenures.
Four-year employees who left seem to have an unusually low satisfaction level. It's worth investigating changes to company policy that might have affected people specifically at the four-year mark, if possible.
The longest-tenured employees didn't leave. Their satisfaction levels aligned with those of newer employees who stayed.
The histogram shows that there are relatively few longer-tenured employees. It's possible that they're the higher-ranking, higher-paid employees.

![ss4](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss4.png)


![ss5](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss5.png)

From the graph above, there does not seem to be any department that differs significantly in its proportion of employees who left and those who stayed

![ss6](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss6.png)

The correlation heatmap confirms that the number of projects, monthly hours, and evaluation scores all have some positive correlation with each other, and whether an employee leaves is negatively correlated with their satisfaction level.

![ss7](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss7.png)

For the champion model (Random Forest model) confusion matrix above:

The upper-left quadrant displays the number of true negatives. The upper-right quadrant displays the number of false positives. The bottom-left quadrant displays the number of false negatives. The bottom-right quadrant displays the number of true positives.

- True negatives: The number of people who did not leave that the model accurately predicted did not leave.

- False positives: The number of people who did not leave, the model inaccurately predicted as leaving.

- False negatives: The number of people who left that the model inaccurately predicted did not leave

- True positives: The number of people who left, the model accurately predicted as leaving

![ss8](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss8.png)

feature importance chart for decision tree above:

The barplot above shows that in this decision tree model, last_evaluation, number_project, tenure, and overworked have the highest importance, in that order. These variables are most helpful in predicting the outcome variable, left.

![ss9](https://github.com/pushpakGD/user_churn_pred/blob/main/projectImgs/ss9.png)

The plot above shows that in this random forest model, last_evaluation, number_project, tenure, and overworked have the highest importance, in that order. These variables are most helpful in predicting the outcome variable, left, and they are the same as the ones used by the decision tree model.


#### Conclusions

Logistic Regression

- The logistic regression model achieved precision of 80%, recall of 83%, f1-score of 80% (all weighted averages), and accuracy of 83%, on the test set.
  
Tree-based Machine Learning

- After conducting feature engineering, the decision tree model achieved AUC of 93.8%, precision of 87.0%, recall of 90.4%, f1-score of 88.7%, and accuracy of 96.2%, on the test set. The random forest modestly outperformed the decision tree model.

##### Recommendation

The models and the feature importances extracted from the models confirm that employees at the company are overworked.
- Implement a limit on the number of projects assigned to each employee to prevent overwork and burnout.
- Consider promotions for employees who have dedicated at least four years to the company, or investigate reasons behind their dissatisfaction.
- Provide incentives for employees working extended hours, or consider flexible work arrangements to maintain a healthy work-life balance.
- Ensure all employees are well-informed about the company's overtime pay policies, and establish clear guidelines for workload expectations and time off.
- Facilitate open discussions at both company-wide and team levels to better understand and enhance the overall work culture.
- Evaluate employees based on proportional effort rather than solely on hours worked, to recognize and reward contributions effectively.
