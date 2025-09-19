
# Agriculture bi project

A brief description of what this project does and who it's for

🌾 Agriculture Data Analytics Dashboard
Dashboard Link : [Add your Power BI Service link here]
📌 Problem Statement

This project focuses on analyzing agriculture data using AWS, Snowflake, and Power BI. The dataset contains information about rainfall, temperature, humidity, and yield, which are critical factors for agricultural productivity.

The goal of this dashboard is to:

Identify average rainfall, temperature, humidity, and yield across years, seasons, locations, and crops.

Provide insights that help in predicting crop yield patterns and improving agricultural planning.

Enable stakeholders to monitor climatic conditions and their direct impact on crop production.

By analyzing the data, farmers, researchers, and policymakers can make data-driven decisions to improve yield and optimize resource usage.

🔄 Steps Followed

Step 1 : Data ingested into AWS S3 for storage.

Step 2 : Data cleaning & transformation performed in Snowflake.

Step 3 : Snowflake queries created to prepare fact & dimension tables.

Step 4 : Data imported into Power BI Desktop via Snowflake connector.

Step 5 : Created relationships between Year, Season, Location, Crop dimensions.

Step 6 : Developed DAX measures to calculate climatic metrics.

Step 7 : Designed Power BI visuals including line charts, bar charts, slicers, and KPI cards.

Step 8 : Added slicers for Year, Season, Location, Crop.

Step 9 : Enhanced design with themes, titles, and crop-specific visuals.

Step 10 : Published the final report to Power BI Service.

🧮 Sample DAX Expressions

1. Average Rainfall (mm)

Avg Rainfall = AVERAGE(agriculture_data[Rainfall])


2. Average Temperature (°C)

Avg Temperature = AVERAGE(agriculture_data[Temperature])


3. Average Humidity (%)

Avg Humidity = AVERAGE(agriculture_data[Humidity])


4. Average Yield (kg/hectare)

Avg Yield = AVERAGE(agriculture_data[Yield])


5. Total Yield (for selected filters)

Total Yield = SUM(agriculture_data[Yield])


6. Yearly Yield Growth %

Yield Growth % = 
DIVIDE(
    [Total Yield] - CALCULATE([Total Yield], DATEADD(Calendar[Date], -1, YEAR)),
    CALCULATE([Total Yield], DATEADD(Calendar[Date], -1, YEAR))
)


7. Crop-wise Yield Contribution %

Crop Yield % = 
DIVIDE([Total Yield], CALCULATE([Total Yield], ALL(agriculture_data[Crop])))
* 100

📸 Snapshots of Dashboard

📊 Replace with your actual screenshots:

🔍 Insights
[1] Rainfall Analysis
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/acb4e886-d998-4009-9acc-3693d39d2a1b" />


Monsoon shows the highest rainfall, strongly impacting crop yield.

Regions with low rainfall show reduced productivity.

[2] Temperature Analysis

Summer seasons have temperature spikes, reducing crop yield in certain crops.

Crops like wheat perform best under moderate temperature.

[3] Humidity Analysis

Rice yield increases with higher humidity.

Some dry crops perform poorly in humid conditions.

[4] Yield Analysis

Kharif season shows maximum yield due to optimal rainfall & humidity.

Rabi season crops are more dependent on irrigation than rainfall.

[5] Correlations

Balanced rainfall + moderate temperature + humidity = higher yields.

Yield decreases sharply when rainfall < average and temperature > average.

⚙️ Tools & Technologies Used

AWS S3 → Data storage

Snowflake → Data cleaning & transformation

Power BI → Visualization & reporting

✅ Conclusion

This dashboard provides a comprehensive analysis of climatic factors and their impact on crop yield.
It helps in:

Understanding regional & seasonal patterns

Supporting policy decisions

Enabling farmers to plan cultivation better
