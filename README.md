# Exploring Customer Segmentation Via PCA and Clustering

## Project Description

In this activity, I will profile customer groups for a large telecommunications company.  The data provided contains information on customers purchasing and useage behavior with the telecom products.  My goal is to use PCA and clustering to segment these customers into meaningful groups, and report my findings.

## Overview

I wanted to see what would happen if I used principal component analysis to assist my clustering and my results are fairly interesting.

I changed all binary categorical features to 0/1 and removed the remaining 8 categorical columns. Due to Euclidean distance, I cannot perform clustering on nominal data, however, I can use PCA to reduce data dimensionality, extract the data signal, and create more meaningful orthogonal features which should enhance clustering via noise reduction.

I created a scree plot to determine how many principal components should be included in my analysis. The elbow was noted at 5, possibly 6. Therefore, I created a chart that showed 50% of the variability is explained by 5 components. However, to reach 80% (rule of thumb) required 15 features! This highlights the curse of dimensionality. I created a 3d scatter plot of the first 3 components and arbitrarily chose to color by Churn Value. Clusters were noted.

I also created a loading table to measure how each numeric feature loaded during the principal component analysis.

I fitted the K-Means clustering model onto the previously calculated PCA scores. An inertia scree plot elbow identified a 3-cluster solution and seaborn was employed for the analysis and interpretation.

## Summary of Analysis and Interpretation of K-mean clustering of PCA scores:

### Blue Cluster(0): Most Loyal Customer Segment, Highest Utilizer of Services, High Referral Rate, Minimal Customer Service Requirements
- This customer segment is the most likely to have the longest tenure and refer another customer. 
- This customer segment is the most likely to have multiple phone lines, online security, online backup, online protection plan, device protection plan, premium tech support, streaming services.
- This customer segment is most likely to make up the under 30 portion of users, most likely to be married, if they have dependents then it is likely that they have 1, 2, 3 dependents.
- This customer segment is likely to have miniAL customer service requestS or product service issueS reported.
- This customer segment isn't likely to churn.
### Business Recommendations:
- This customer segment is the most likely to refer another customer. Therefore, they should be better incentivized due to do so - to further increase market share.
- These customers are the most loyal. Therefore, they should be rewarded with a gift certificate for their business or no intervention is necessary because it is likely they will remain customers. 
- This customer segment should be targeted for customer surveys to serve as a baseline against other customer segments who have high churn rates.
- This customer segment should be targeted for company credit cards that offer higher rewards for the services they purchase.

### Orange Cluster(1): Loyal Customer Segment, Lowest Utilizer of Services, Lowest Customer Service Requirements
- This customer segment is the least likely to have internet service, to download GB of data, have an online protection plan, have unlimited data, or have paperless billing.
- This customer segment is least likely to be a senior citizen or under 30; if this customer segment has dependents then they are likely to have 1, 2, or 3 dependents; this customer segment is also likely to be married.
- This customer segment is least likely to have a customer service request and isn't likely to churn.

### Business Recommendations:
- This customer has the lowest utilization of services. Therefore, they may respond positively to reasonably priced-packages to increase their service utilization.

### Green Cluster(2): Unloyal Customer Segment, Focus on Internet/Phone Service, Value-Focused, High Customer Service Requirements
- This customer segment is most likely to have the shortest tenure.
- This customer segment is the most likely to have phone service, internet service and paperless billing.
- This customer segment is the least likely to have online security, online backup, device protection plan, premium tech support or multiple phone lines.
- This customer segment is significantly more likely to make up the senior citizen portion of the age distribution and the least likely to have dependents.
- This customer segment is the most likely to have customer service requests of 2 or more, report product/service issues, and has the highest frequency of churning.
### Business Recommendations:
- This customer has the highest rate of churning. Therefore, contracts could help retain their business that have obvious savings to promote their business. 
- Any calls to customer service should be answered quickly and issues resolved efficiently to maintain their business.
- This customer segment should also be targeted for customer surveys to assess for any areas of improvement.
