# Netherlands Student Test Result
The data set nlschools (in the MASS library, use data(nlschools, package = "MASS") to load in the data) contains the following records for 2287 students in the Netherlands. Snijders and Bosker (1999) use as a running example a study of 2287 eighth-grade pupils (aged about 11) in 132 classes in 131 schools in the Netherlands. Only the variables used in our examples are supplied.

* lang: their test score on a language exam
* IQ: their verbal IQ
* class: the ID number for their classroom
* GS: the number of students in each class
* SES: the socio-economic status of their family
* COMB: was the student in a multi-grade class? (0=no, 1=yes)

## Tasks in this practise:
Understand the dataset
The task is to explore and describe this data set. You should use both models and visualization. You should use your judgement as to what are the most important aspects of the data to highlight; however, the following questions are of particular interest:

* Are there descrepancies in IQ or SES in the different classes, or when grouping by multi-grade vs non-multi-grade classes?
For this question, we will firstly generate class group to better server the analysis. And then use Quantile plot and QQ plot to evaluate each class group versus pooled data and see if descrepencies exist on IQ, SES, respectively. Next, we will use the same strategy to evalute whether multi-grade will affect IQ and SES.

* When did students perform better or worse on the language exam? Describe which variables had the most important effects.
In this section, we will evaluate effect of individual variables on language test scores. Cross validation is used to look for the best degree of freedom to build linear model. For one thing, the analysis will be able to tell which variables have impact on language score. On the other hand, I will be able to tell how these variables and what trend is the effect. We will use forward/backward stepwise linear regression to validate our findings in the next question as well.

* Do you think there are interactions in the effects of the variables on the language exam score? Speculate as to the cause of any such effects that you think should be included.
Firsly, we will use forward/backward stepwise linear regression to validate our find in question 2 on what are the important variables. Then we can use ^2 on variables to run linear regression to get interactions. Then use the Coplots to check if our finds are visiable in the plot on these interactions. Meanwhile, interactions that are not presented in the linear model will be plot as well to confirm no interactions exist between other variables.

