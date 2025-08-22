
# Power-BI-Sales-Analytics-Dashboard
Sales Analysis Dashboard (Power BI Project)
🔹 Introduction

This Power BI dashboard was developed to analyse sales and shipment performance using a dummy dataset. The goal of the project is to transform raw transactional data into meaningful insights through interactive visuals, DAX measures, and Power Query transformations.

The report provides a summarized overview of business performance by combining revenue, cost, and shipment activity into one place, enabling users to quickly evaluate profitability, operational efficiency, and month-over-month trends.

This report will also help provide managers with a single source to take data driven decisions and plan strategically accordingly.

🔹 Key Features of the Dashboard

Revenue & Profitability Tracking:

Measures like Total Sales, Total Cost, Total Profit, and Profit % give a complete financial picture.

Operational Metrics

Shipment activity tracked by Total Shipments, Total Boxes, and Low-Box Shipments % to evaluate logistics efficiency.
Assess shipment sizes (via Low-Box Shipments %) to evaluate fulfillment patterns and operational efficiency.

Month-over-Month (MoM) Comparisons:

Dynamic calculations for sales, cost, shipments, and profit changes relative to the previous month.

Spot positive or negative momentum through MoM comparisons of sales, profit, and shipments.

Most Recent Performance

Automatically identifies the latest month in the dataset to highlight current KPIs.

Data Quality & Modeling

Built on a structured model with a calendar dimension, enabling accurate time intelligence calculations.
This project analyzes sales performance using a star-schema-like model (shipments fact with a products dimension and a 'calendar' date table).

Insights and take away:
Profitability: While overall profit remains positive, the Profit % measure shows volatility, suggesting the need for tighter cost control.
Order Mix: The shipment analysis visual shows high number of shipments with 20-500 boxes and very low number of shipments with higher number of boxes ( 2000 or more) showing logistical and cost inefficiency.
Business Health: Month-over-month comparisons across sales, costs, shipments, and profit provide an early-warning system for shifts in performance, making the report useful for ongoing monitoring.

Description of visuals:
All visuals in this dashboard were self-designed and implemented in Power BI Desktop using custom DAX measures, Power Query transformations, and built-in formatting features. No third-party templates or pre-built reports were used. Each visual was created with a clear analytical purpose:

-Visual 1 – KPI Trends Over Time:
The first visual shows a month on month analysis of all the important KPIs that can be analysed for a data. Since the data is just for a time duration of over a year, this is the only time period based analysis that gives an insight on how important parameters like sales, shipments etc trend with time. The chart can be filtered with a dynamic slicer, which applies only to the visual and not to entire page and one can choose to see in detail change in each KPI individually.

-Visual 2 – Shipment Distribution by Boxes:
The second visuals shows spread of shipments i.e how many shipments take with them how many boxes ( the number of boxes are grouped within a range of number). A new group was created for the boxes column called Boxes Bin and each bin size having 20 boxes in them.
Since number of boxes for each shipment range from 0 to upto 2000 boxes , its a large range and hence zoom slider is used for axis with number of boxes to choose the range of selection and then analyse. The LBS KPI card is also incorporated in the visual. It is interactive with first visual where you can choose any particular month and see what % of shipments in that particular month were having low no. of boxes.

-Visual 3 – Salesperson & Product Performance:
The third visual helps in analysing product performance and sales person performance in one visual. The performance of sales person has been categorized into three levels based on whether their sale of product has met the target profit percentage. For the sake of analysis the target % is set to 60 ( The average profit %).An if conditional dax query is used to classify the performance, good if profit % is greater than target, okay if 90% of target has been achieved by sales person and not okay if target profit % is not reached. Conditional formatting is used to assign icons ( dynamic icons change automatically with change in profit%) which makes understanding the sales person performance through table easy.
Also in order to highlight the profit % a data bar is placed along the profit% column. A small trick has been used to make the value more readable. The bar length was almost equal for each row, since profit% for most sales persons are around same value. This made it difficult to compare profit % within different sales persons. Then in conditional formatting the maximum and minimum value of profit % was changed from 0 to 120 so that this scale can change the length of data bars making them more readable.

A similar analysis of the product performance is also shown in the visual. This visual is same as the third visual i.e the parameters against which the performance of the product is analysed are same- summarizing the product sales, profit, profit%, LBS etc. Also, a target profit% is set against each category of product to access how the product delivers in terms of profit, which products always achieve the target profit and which are underperforming.

A bookmark is created so that the user can switch between the two visuals, analysing product and sales person performance individually with the click of a button. This means the third visual has to tables in it- the sales person Analysis and product analysis which change with clicking on the side buttons. Special attention has been paid that bookmarks retain the filter context of the page. This means it is important that data is not taken with the visual in bookmark, else if bookmark is selected after filter is applied, the filter will not hold true for the bookmarked visual.

-Interactivity & Tooltips:
The dashboard has been designed interactively, which means that if you click on any data point on one visual, for eg- if you click on March'23 data on first visual to analyse it separately, the data of all other will automatically change to show their respective data also for March'23. This makes readability really easy.

Also, a tool tip has been added to the shipment analysis to highlight the monthly value of the chosen KPI and distribution of the KPI value for the month in different locations. This helps management get a overview of data without needing to understand the complete chart.

This Power BI dashboard was developed to analyse sales and shipment performance using a dummy dataset. The goal of the project is to transform raw transactional data into meaningful insights through interactive visuals, DAX measures, and Power Query transformations.
