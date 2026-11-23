1. Project Title / Headline
Zing Customer Payback Prediction: End-to-End Machine Learning Workflow in Dataiku

2. Short Description / Purpose
This project was built for Payback prediction. It uses Dataiku to predict customer payback status for Zing, a gaming company, and to find out whether distinct customer groups exist among customers with a Good RFM score. The work covers cleaning the customer data, engineering a new TAG feature from customer bios, training and comparing models over two trials, and deploying a final Logistic Regression model. It ends with a clustering attempt on high-value customers, and the screenshots in this folder document each stage of the flow.

3. Tech Stack
Dataiku DSS: data preparation recipes, visual flow, split recipe, AutoML training, model deployment and scoring
Logistic Regression: final deployed model
Decision Tree: compared against Logistic Regression during the trials
Clustering: used to look for customer segments among Good RFM customers
Feature engineering: TAG column built with a Dataiku formula

5. Data Source
Excel file - Middlesex University

6. Features / Highlights
Data cleaning: filled empty Customer Bio values with "Nil" and empty RFM Score values with the previous row's value. Payback Status was changed from integer to text because it holds multiple categories.
Feature engineering: created a TAG column that is TRUE if the customer bio contains Shopaholic, Geek or Fitness, otherwise FALSE.
Train/test strategy: 80% of the data for training and 20% for testing.
Model trials: two trials. In the second trial the RFM score was removed because the new RFM variable is based entirely on it, and variables contributing less than 5% to training were dropped.
Final model: Logistic Regression, chosen for its better reasoning and formula-based training.
Key drivers: Profile Picture on Social Media and Payback Status had the strongest influence on predictions.
Evaluation: accuracy and other metrics reviewed, with predicted probabilities checked on the test data.
Full flow: the final flow runs prepare, split, train, score and deploy.
Clustering finding: no clear clusters were found among Good RFM customers, because outliers kept forming
