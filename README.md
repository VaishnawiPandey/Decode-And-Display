# Decode-And-Display
Reverse Logistics Optimization through Data Visualization
Project Overview

ABC Logistics, a leading player in e-commerce fulfillment and shipping, experienced a noticeable rise in product returns. To address this, a detailed dataset was analyzed to uncover the main causes of returns and to propose improvements for reverse logistics. The project focused on data cleaning, preprocessing, and the creation of interactive dashboards that highlighted key factors such as delivery delays, size and fit mismatches, product pricing, manufacturer variations, and customer demographics.

Dataset Summary

Size: 481,092 rows × 14 columns

Key Variables:

Order Details: orderItemID, orderDate, deliveryDate, price, manufacturerID

Customer Information: customerID, salutation, dateOfBirth, creationDate, state

Product Attributes: itemID, size, color

Return Metrics: returnShipment, delay

Data Quality & Cleaning Steps

Missing Values Identified:

deliveryDate: 39,419 nulls

color: 143 nulls

dateOfBirth: 48,889 nulls

Imputation Strategy:

Color → Mode imputation

dateOfBirth → creationDate - 47 years

deliveryDate → orderDate + 10 days

Size Grouping:
Standardized into categories (XS, S, M, L, XL, XXL, XXXL, Outlier, Unsized, Others) under a new field SizeCategory.

Methodology
Data Preparation

Addressed missing values with suitable imputations.

Engineered new metrics:

Delivery Delay (deliveryDate – orderDate)

Customer Age (creationDate – dateOfBirth)

Normalized size data into grouped categories.

Data Visualization

Power BI dashboards were developed to visualize:

Delivery timeliness vs. return probability.

Size & fit issues across categories.

Impact of price and manufacturer on return rates.

Customer demographics and state-level return trends.

Analysis Approach

Studied correlations between delivery delays, price, size mismatch, and return behavior.

Segmented customer demographics to identify return patterns.

Compared regional return behavior across German states.

Key Insights

Delivery Delays: Returns increase sharply when orders are delivered after 10 days, suggesting customer dissatisfaction due to lateness.

Size & Fit Issues: Products in extreme size groups (below size 34, L, and XXXL) had significantly higher return rates.

Price & Manufacturer Influence: Expensive items showed higher return tendencies. Manufacturers displayed wide variability in return ratios, indicating inconsistency in product design/quality.

Customer & Regional Behavior:

Customers aged 30–60 returned fewer items than younger/older groups.

Regions such as Saxony and Thuringia reported higher return frequencies.

Female customers in regions like Saxony-Anhalt exhibited above-average return activity.

Tools & Technologies

Data Processing: Python (Pandas, NumPy)

Visualization & Dashboarding: Power BI
