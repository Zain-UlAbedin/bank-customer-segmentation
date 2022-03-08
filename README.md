# Customer Segmentation for Bank
## Overview of the project
### Problem to be solved/answered
XYZ Bank wants to focus on its credit card customer base in the next financial year. But to do so they have to run personalized campaigns to target 
new customer and upsell to existing customers. Another insight from the market research was that the customers perceive the support services of the 
back poorly. To tackle this we have to dig deep into the customers data extract the most useful information for the bank

### Objectives:
- Explore and visualize the dataset.
- Build a Clustering model to make customer segmentation
- Generate a set of insights and recommendations that will help the bank

### Key Questions
- How many different types (clusters/segments) of customers can be found from the data?
- How do these different groups of customers differ from each other?
- Do you get slightly different solutions from two different techniques? How would you explain the difference?


### Data Attributes 
- Sl_No: Primary key of the records
- Customer Key: Customer identification number
- Average Credit Limit: Average credit limit of each customer for all credit cards
- Total credit cards: Total number of credit cards possessed by the customer
- Total visits bank: Total number of Visits that customer made (yearly) personally to the bank
- Total visits online: Total number of visits or online logins made by the customer (yearly)
- Total calls made: Total number of calls made by the customer to the bank or its customer service department (yearly)


## Resoruces and Code used
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, scipy, yellowbrick

## EDA
I started with Univariate analysis to get an overviews of each individual attribute, and see how spread it is, what type of distribution it have etc. Afterwards I did Bivariate 
analysis of the dataset to get an idea of colinearity between the attributes and in ideal case we need less colinearity between the independent variable and want as much
corelation between the independent and dependent/target variable.


## Model Building
K-Means was chosen for clustering as it is the simpler yet effective algorithm, Elbow Method and Silhouette score were used to measure the validity of our clusters, the closer
the score of silhoutte to 1 the better our clusters are seperable from others. Below are some sample pictures that conveys some usefule information
![alt text](https://github.com/Zain-UlAbedin/bank-customer-segmentation/blob/master/clusters_with_attributes.png "Different Clusters group values for different attributes")
![alt text](https://github.com/Zain-UlAbedin/bank-customer-segmentation/blob/master/silhouette_score.png "Silhoutte Score")

## Insights and Recommendations
Some insights that were extracted during the whole EDA analysis.
- **Cluster 0**: These are the Tier 3 Customers with less credits cards and have less limit on their cards, have more calls made to the bank, with moderate 
visits **Bank looking for the average/low salary customers can approach this cluster for quantity sales rather then qualtiy sales**


- **Cluster 1**: These are the Tier 2 Customer or middle upper class, These customer spendings are much based on their credit limits and number of credit cards. 
 These customer prefer visiting the bank or visiting online then calling the bank. **Bank should approach these customers, they will be more willing to 
 purchase from the bank, bank should also work on thier online presence and physical space.**


- **Cluster 2**: These are the Tier 1 Customer or elite class, These customer spendings are way higher then other clusters based on their credit limits 
 and number of credit cards. These customer are very busy so instead of calling or going to bank they visits online. **The bank should first work on improving 
 their online presence, and there should be no delayed in the response from the website, Bank should also work on their customer support, after having best of 
 both then should they target these customers, They might be less in quantity but they are worth more then cluster 1 and cluster 0 combined.**
