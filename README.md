# Agronomic Data Scientist

Welcome to my portfolio, where I share my learning journey in business analytics. These projects show my growing skills in data analysis, predictive modeling, and making decisions based on data.

<details>
  <summary><strong>Education</strong></summary>
  
  <ul>
    <li><strong>Master of Science in Business Analytics</strong><br>University of Utah, Salt Lake City, UT, United States</li>
    <li><strong>MBA in Business and Entrepreneurship</strong><br>PUC RS, Porto Alegre, Brazil</li>
    <li><strong>Specialist in Soil Management</strong><br>Esalq USP, Piracicaba, Brazil</li>
    <li><strong>Bachelor's Degree in Agronomy</strong><br>UEL, Londrina, Brazil</li>
  </ul>

</details>

<details>
  <summary><strong>Work Experience</strong></summary>

  <ul>
    <li><strong>Data Entry Specialist and Assistant Buyer</strong><br>The University of Utah Campus Store, April 2023-present</li>
    <li><strong>Founder/CEO/Senior Crop Advisor</strong><br>Apta Agribusiness, July 2010 - July 2023</li>
    <li><strong>Junior Crop Advisor and Precision Agriculture Analyst</strong><br>Insolo Agricultural Management, August 2004 - June 2010</li>
  </ul>

</details>
<br>
<hr>

## 1. Kaggle Competitions
<p align="left" style="margin: 0; line-height: 1;">
   <span style="font-size: 16px; vertical-align: middle; margin-right: 10px;">Home Credit Competition</span>
   <a href="https://www.kaggle.com/competitions/home-credit-default-risk">
      <img src="images/kaggle_logo.png" alt="Kaggle Logo" style="width: 18%; max-width: 1000px; display: inline-block; vertical-align: middle;" />
   </a>
</p>

[Home Credit RMarkdown code](https://github.com/kleytonrps/Home_Credit_Project/blob/main/Home_Credit_Kleyton.qmd)

[Home Credit Project PDF](https://github.com/kleytonrps/Home_Credit_Project/blob/main/pdf%20files/Home_Credit_pdf_code.pdf)


**Business problem and project objective**

Home Credit aims to address the challenge of providing secure credit access to underserved populations and empowering individuals and businesses. This project focuses on developing a default prediction model using advanced analytics, aligning with Home Credit's goal of promoting financial inclusion while ensuring the company's financial stability.
 
 
**Analytics approach**

The extensive dataset contains information on over 307,000 consumers across 121 variables. It is also highly imbalanced, with only 8% of individuals classified as defaulters, posing significant challenges to both business decision-making and the prediction process. A thorough data exploration revealed issues such as ambiguous variable values, outliers, and missing data, all addressed through appropriate transformations and cleaning steps.

<p align="center">
   <img src="https://github.com/kleytonrps/Home_Credit_Project/blob/main/plots/default%20by%20income.png?raw=true" alt="Default by Income" width="600" />
</p>

Our approach involved one-hot encoding categorical variables and re-balancing the dataset via downsampling, selecting 24,000 defaulters and 48,000 non-defaulters. We also applied Recursive Feature Elimination (RFE) to identify the most relevant variables, enhancing computational efficiency and model performance.

We developed four classification models—Logistic Regression, Random Forest, XGBoost, and LightGBM—using 70% of the re-balanced dataset (72,000 observations) for training. Class probabilities were evaluated using the Area Under the Curve (AUC), and binary classifications were assessed using confusion matrices on the remaining 30% of the data. Data standardization was applied throughout the modeling process.

All models underwent 10-fold cross-validation with two repetitions to further enhance predictions, complemented by grid search optimization for hyperparameter tuning (except for Logistic Regression). This robust framework ensured reliable and accurate model performance.

**Our Solution**

To assist Home Credit in achieving its goals, we developed an ensemble model that combines four individual models to balance prediction results. Compared to a random classifier, this ensemble model improves the prediction of defaulters from 8% to 38% while maintaining high accuracy in identifying non-defaulters (89% compared to 92% with the random classifier).
<p align="center">
   <img src="https://github.com/kleytonrps/Home_Credit_Project/blob/main/plots/final_metrics.jpg?raw=true" alt="Final Metrics" width="600" />
</p>
Additionally, the models highlighted Home Credit’s reliance on external risk classification data. The analysis revealed that data from external sources 2 and 3 were the most significant. Furthermore, the study showed that variables such as credit amount, goods price, years of employment, age, ID publication date, car ownership, last phone change date, and education level played a key role in strengthening the models.
<p align="center">
   <img src="https://github.com/kleytonrps/Home_Credit_Project/blob/main/plots/xgboost_predictors.jpg?raw=true" alt="XGBoost Predictors" width="600" />
</p>

This solution achieved a score of nearly 0.74 in the Kaggle competition, which can be considered a strong performance, approximately 8% lower than the winning solution.



**Business Value**

With the improved predictive capabilities, Home Credit can allocate resources at least 30% more efficiently, reducing financial losses associated with defaults. Despite a slight 3% decrease in non-defaulter accuracy, the ensemble model aligns with the company’s mission of financial inclusion by minimizing unnecessary rejections.

Moreover, by identifying the most relevant data sources and variables, Home Credit can streamline its processes, ensuring faster and more convenient loan application experiences for clients. This targeted approach balances precision and inclusivity, enabling Home Credit to make smarter, data-driven decisions while maintaining its commitment to underserved populations.


**My role, difficulties, and learning**

I actively participated in all stages of the project, leading discussions about the models and, most importantly, how to explain the results in a way relevant from a business perspective. I spent over 80 hours working on this project, and my ability to analyze and question the data made a difference, even though I still rely on LLM models for writing code.

We faced numerous challenges, including the high computational demands of modeling, which I overcame for the XGBoost and LightGBM models by creating the process in separate stages, inspired by a Machine Learning class. The RFE process was the most time-consuming, taking more than 7 hours to complete. Additionally, I attempted KNN imputations, which I decided to refine in another project because they generated values outside the acceptable range for some variables.

There were two significant issues that, while not technically critical, caused considerable inconvenience. The first was the difficulty generating a well-structured PDF from the quarto file in RStudio. The second occurred when GitHub Desktop committed a 130 MB file, which caused significant disruptions since it wasn't possible to undo the change in the history. As a result, the repository had to be deleted and recreated. I'm considering focusing on Jupyter Notebooks using Python to address these challenges.

I learned that more time should be spent thinking about the data, perhaps creating new variables, rather than rushing to develop models. It became clear that my effort and willingness to learn compensated for my lack of experience in these processes. Although I am satisfied with the final performance and grateful for the opportunity to learn from my colleagues, the company's solution could have been better. I could have translated the models into more tangible financial terms for the business.


