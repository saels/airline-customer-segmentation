# ✈️ Airline Customer Segmentation with K-Means

## 💼 Business Use Case

Airline loyalty customers do not all behave the same way. Differences in tenure and mileage balance can point to different levels of engagement and may justify different retention, re-engagement, or loyalty offers.

This project uses clustering to turn those differences into customer groups that are easier to interpret and discuss from a marketing perspective.

## 🎯 Principal Objective

The objective is to use K-Means clustering to identify customer segments based on **account age** and **current mileage balance**, then interpret the resulting clusters as potential starting points for differentiated campaign strategies.

The analysis is intentionally small and illustrative, so the emphasis is on the clustering workflow and the decisions that would need to be revisited before using the approach on real customer data.

## 🔍 Key Takeaways

The three-cluster solution separates the sample into a newer high-mileage group, a mid-tenure high-mileage group, and a longer-tenure lower-mileage group. These patterns suggest different marketing hypotheses, such as status acceleration for newer high-engagement members or re-engagement offers for long-standing customers with lower balances.

The technical limitations are just as important as the segments themselves. The dataset contains only 20 manually defined observations, and the two features are not standardized in the current implementation. Because K-Means is distance-based and mileage balance operates on a much larger numeric scale than account age, it can disproportionately influence the clusters.

A production segmentation would need a larger dataset, feature scaling, richer behavioral variables, cluster-stability checks, quantitative validation, and campaign experiments to confirm that the segments are commercially useful.

## 💻 Explore the Notebook

The [notebook](https://github.com/saels/airline-customer-segmentation/blob/430beb365cce9b4e38f924e8eb9d64241c74d0d9/Airline_customer_segmentation.ipynb) contains the full exploratory analysis, elbow-method selection, K-Means fitting, cluster centers, and visualization. Check the code for the implementation details and for the assumptions that should be tested before taking the segmentation beyond a demonstration.
