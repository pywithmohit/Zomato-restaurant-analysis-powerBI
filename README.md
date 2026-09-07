🍽️ Zomato Restaurant Analysis — Power BI Dashboard

An end-to-end data cleaning, EDA, and interactive dashboard project built on the Zomato Restaurants dataset, designed as a manager-style "market & restaurant performance review" analysis.

<img width="1117" height="617" alt="IMAGE-2" src="https://github.com/user-attachments/assets/7a85b11b-0160-4118-b394-05429ccacc71" />


📌 Project Overview

This project analyzes 9,500+ restaurant records across multiple countries to uncover patterns in restaurant ratings, delivery availability, pricing, and geographic distribution. The goal was to simulate a real analyst task — take messy raw data, clean it with clear documented decisions, and turn it into a decision-ready interactive dashboard.

📂 Dataset
Source: Zomato Restaurants Dataset (Kaggle)
Files used: zomato.csv (9,551 restaurant records), Country-Code.csv (country lookup table)
Additional JSON API dump files were evaluated but excluded — they overlapped almost entirely with the main CSV (only ~26 new records), so were not worth the added flattening complexity.
🛠️ Tools Used
Power BI — data modeling, DAX measures, dashboard design
Power Query — data cleaning and transformation
🧹 Data Cleaning & Key Decisions
Established a relationship between zomato and Country-Code tables on Country Code.
Kept Has Table booking, Has Online delivery, and Is delivering now as their original TRUE/FALSE boolean values rather than converting to Yes/No, for consistency with the source data.
Rows with 0,0 latitude/longitude were kept and flagged as "location unknown" instead of being dropped, to preserve total restaurant counts.
Added a conditional column to translate the raw Has Online delivery boolean into a readable Available / Not Available label for the dashboard card.
📊 Dashboard Features
KPI Cards: Total Restaurants, Average Rating, Online Delivery Availability
Interactive Slicers: Country, City, Restaurant Name, Food Type
Geo Map: Plots restaurant locations globally, color-coded by country
Bar Chart: Total Restaurants by Country (highlights India as the dominant market, followed by the US, UK, and Brazil)
Custom red/Zomato-branded theme for a polished, presentation-ready look
📸 Screenshots

<img width="1115" height="616" alt="Image-1" src="https://github.com/user-attachments/assets/263852d9-6b60-4800-b13a-961c06775576" />
<img width="1117" height="617" alt="IMAGE-2" src="https://github.com/user-attachments/assets/3ff94bab-32b9-4a78-94c4-8686a10f386b" />


🎯 Key Takeaway

Most of the real work in this project wasn't the visuals — it was the decisions behind the data: how to handle missing coordinates, whether to standardize boolean fields, and how to bridge lookup tables cleanly. This project was built to practice thinking like a data analyst, from raw messy data to a dashboard a decision-maker could actually use.

👤 Author

(Mohit Yadav and LinkedIn - https://www.linkedin.com/in/pywithmohit/ )
