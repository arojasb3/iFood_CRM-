# ifood-data-business-analyst-test-latam

This case is used for hiring Data Analysts for the iFood Brain team. Instructions are in the pdf file.

If you are interested in joining our team, or getting to know more about iFood and our team, feel free to send an e-mail to "shadia.reales@ifood.com.co".

Main question : How can we support direct marketing iniciatives whithin the company using clustering algorithms and classification models?

## First Part - Data Analysis

The first part is to analyze the dataset, remove NaNs, remove some outliers, generate new variables and overall try to find features about the customers that accepted the last campaign.


## Second Part - Clustering

The second part aims at clustering the customers using K-Means and K-Prototypes, then analyzing each of the cluster features and how effective was the campaign.

![Cluster_0_pie](https://github.com/arojasb3/iFood_CRM-/tree/master/figures/cluster_piecharts.png)

As we can see in the picture above there is one group (Cluster 0) where customers accepted the campaign in a much higher proportion (28%) than in the complete dataset (15%). This group of customers are the ones with the highest income and they are also the ones that spend the most on every product. They prefer to shop in the actual stores or catalogs instead of visiting the webpage but they are in the middle of the pack for web purchases. It is like they usually don't visit the website, but when they do then they buy. Finally, Age is not a really defining variable of this cluster, we can find customers from all ages.

## Third Part - Classification Models

For the final part we used a logistic regression and a random forest model to try to predict the success of the last campaign on the customers. The imbalanced dataset was undersampled to achieve a 33% of sucess overall. The top 5 most important variables according the random forest can be seen below.

![Top 5 features RF](https://github.com/arojasb3/iFood_CRM-/tree/master/figures/top5_features_rf.png)

This combined with the logistic regression results showed us that old and loyal customers(Low recency and high enrollment time) may have a higher chance to accept the last campaign. Also the ones that prefer to spent money on the store, making sense with the high income conclusion from the cluster analysis.

## Conclusions

- Customers with high enrollment time and low recency should be aimed for the campaign. 

- Amount spent on both meat and gold seem important, but more importantly as we saw on cluster 0, we want to aim at customers with the higest income. As one can guess, the ones with the most income are also customers that can spend a lot more at the store. We would be combining loyal customers with high income.

- Age can be somewhat important but shouldn't be the main choosing factor at the moment of deploying the campaign.

- The customers that approved campaign 3 are somewhat more likely to accept the last campaign. So checking at those old customers that bought stuff in that campaign can be also for the marketing department to review.