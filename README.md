Fairness with IBM AIF 360 
The goal of this assignment is to study algorithmic fairness concepts using the AIF 360 tool. In
this assignment, we will be using the COMPAS dataset.
Exercise 1 
In group-based definitions of algorithmic fairness, we define protected groups based on
values on a protected attribute, like race, sex, and then measure the discrepancy of some
metric among the protected groups in some observed outcomes. For example, we might
compute the difference of the positive rate between males and females.
In intersectional fairness, we are interested at what happens among groups that are defined
based on intersections of attributes. For example, we might study what is the positive rate
difference between males and females for those aged less than 25. Or, what is the positive
rate difference between the four groups defined by race (African-American and Caucasian)
and sex (males and females).
In the first exercise:
- Consider race to be the protected attribute, fix the bias using the reweighing
preprocessing technique, and measure the bias assuming sex is the protected
attribute.
- Consider sex to be the protected attribute, fix the bias using the reweighing
preprocessing technique, and measure the bias assuming race is the protected
attribute.
- Repeat these measurements considering age groups, to investigate questions like: is
there unfairness with respect to either sex or race between those aged less than 25?
In all cases, you should train a simple logistic regression classifier, and measure bias on a test
set. Document and present your findings in a report.
Exercise 2 
Consider the Multi-Dimensional Subset Scan (MDSS) method from [1] that is implemented in
AIF 360 and showcased in the “demo_mdss_classifier_metric.ipynb” example notebook. The
MDSS method is able to detect unfairness instances in subpopulations.
In the second exercise:
- Examine the privileged and unprivileged groups that MDSS identifies. For each of
them, measure its bias and compare it to a group that has the opposite race or sex.
For example, it a group is defined as “age less than 25” and “race is Caucasian”, you
should compare it to the group “age less than 25” and “race is African American”.
Document and present your findings in a report, where you also summarize how the MDSS
method works.
