# fraud-ny-property-unsupervised
unsupervised learning for fraud analytics on ny property data 

This data can be found here https://data.cityofnewyork.us/City-Government/Property-Valuation-and-Assessment-Data/yjxr-fw8i

Based on the analysis of property valuation and assessment data, we have developed a predictive model to identify anomalies. We first clean our data and because this project is not based on fraud label, we need to find the unusual records that are outliers. In the cleaning part we want to keep most of the data and filling the missing data with reasonable values. After cleaning the data, we create the meaningful variables and scale the variables before doing a pca for dimensionality reduction. Then we build two score, one from z scale and one from autoencoder. Using rank order scaling to combine the two score as final score and sort with this final score to examine the top records. Repeat this step to see if the algorithm make sense and adjust it with examination feedback. Our results shows that some records with certain variables unusualness are anomaly because of certain inaccurate information for those records. 

After we got our final score, we sort our data with the final score. By looking at the top records, we can check if we find anything unusual. After we get the feedback, we can adjust our model by improving exclusions and variables. Then redo the step until we find something interesting. 
To examine the top properties, we will look at the z scaled variables first and it will immediately see which variables have unusual values. We generate a heatmap of the z scaled variables and we could see which variables cause the high scores.
