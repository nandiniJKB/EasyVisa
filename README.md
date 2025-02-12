# EasyVisa
Ensemble Techniques:  Analyze the data of Visa applicants, build a predictive model to facilitate the process of visa approvals, and based on important factors that significantly influence the Visa status recommend a suitable profile for the applicants for whom the visa should be certified or denied.

 ## Problem Statement

As a Data Scientist at EasyVisa, I am tasked with addressing a key challenge faced by the Office of Foreign Labor Certification (OFLC) in the United States.  With a high volume of visa certification applications (over 775,979 applications for 1,699,957 positions in FY 2016), the manual review process is inefficient.

My objective is to develop a Machine Learning-based classification model to:

1. **Facilitate visa approval:** Automatically shortlist applicants with a higher likelihood of approval.
2. **Recommend visa status:** Recommend whether a visa should be certified or denied by analyzing employee and employer attributes.

The goal is to create a data-driven solution that streamlines visa decision-making, ensuring efficient processing while complying with US labor regulations and protecting the interests of both US workers and foreign applicants.

## Data Description

The data includes employee and employer attributes.  Key features include:

* `case_id`: Visa application ID.
* `continent`: Employee's continent of origin.
* `education_of_employee`: Employee's education level.
* `has_job_experience`: Employee's job experience (Y/N).
* `requires_job_training`: Employee's job training requirement (Y/N).
* `no_of_employees`: Employer's company size.
* `yr_of_estab`: Employer's company establishment year.
* `region_of_employment`: Foreign worker's intended US employment region.
* `prevailing_wage`: Average wage for similar occupations in the employment area.
* `unit_of_wage`: Prevailing wage unit (Hourly, Weekly, Monthly, Yearly).
* `full_time_position`: Position's full-time status (Y/N).
* `case_status`: Visa status (Certified/Denied).

## Insights and Recommendations

This section presents key insights and recommendations for the Office of Foreign Labor Certification (OFLC) based on the visa application analysis.

### Insights

Three critical factors significantly influence visa application outcomes:

* **Education Level:** Applications for jobs requiring higher education (Master's, Doctorate) are much more likely to be approved than those requiring lower education levels (e.g., High School Diploma).
* **Prior Job Experience:** Applicants with prior job experience have a considerably higher approval rate compared to those without experience.
* **Prevailing Wage:** Higher prevailing wages, especially for hourly positions, correlate strongly with higher approval probabilities.

### Recommendations

To optimize resource allocation for screening, the OFLC can prioritize applications based on these factors:

1. **Education-based Sorting:** Sort applications by education level and prioritize review of those with higher qualifications.
2. **Experience-based Sorting:** Sort applications by prior job experience and prioritize those with experience.
3. **Wage-based Sorting:** Divide applications into hourly and annual wage categories. Within each group, sort by prevailing wage (highest to lowest) and prioritize review of higher-paying salaried positions first.

**Model Selection:** While the Gradient Boosting classifier performs best overall, the tuned Decision Tree
