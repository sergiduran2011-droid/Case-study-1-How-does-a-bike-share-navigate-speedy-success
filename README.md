# Cyclistic Bike-Share Case Study: How Does a Bike-Share Navigate Speedy Success?

**Author:** Sergi Durán Sabaté  
**Date:** July 30, 2026  
**Tools Used:** Python (Google Colab), Tableau Public, Google Drive  

---

## Executive Summary
This case study is part of the **Google Data Analytics Professional Certificate**. The primary objective of this analysis is to understand how annual members and casual riders use Cyclistic bikes differently. Based on these insights, the project provides data-driven marketing strategies to convert casual riders into long-term annual members.

---

## Phase 1: Ask
Converting casual riders into annual members is widely recognized as a primary driver for Cyclistic’s long-term business growth. To support this strategic objective, this analysis addresses a central question: **How do annual members and casual riders differ in their usage of Cyclistic bikes?**

By identifying key patterns—such as behavioral differences, ride timing, and usage trends across both user segments—this project aims to replace assumptions with data-driven insights. The resulting findings provide the groundwork for targeted marketing strategies designed to encourage casual riders to transition into long-term memberships.

**Key Stakeholders:**
* **Lily Moreno:** Director of Marketing
* **Cyclistic Executive Team**

---

## Phase 2: Prepare
* **Data Source:** Used Cyclistic’s historical trip data provided by Motivate International Inc. under a public license, covering the period from April 2020 to December 2020 (`202004` to `202012`).
* **Data Organization:** The data was downloaded in monthly `.zip` archives, unzipped, and stored securely in dedicated directories (`01_Raw_Data` for immutable backups and `02_Processed_Data` for manipulation).
* **Credibility & Security (ROCCC):** The data is reliable, original, comprehensive, current, and properly cited. To comply with data privacy policies, personally identifiable information (PII) of riders has been excluded.

---

## Phase 3: Process
* **Tool Selection:** Python (via Google Colab) was chosen to process, clean, and merge the large monthly datasets efficiently, handling millions of rows seamlessly.
* **Data Cleaning & Manipulation Steps:**
  1. Imported and concatenated all monthly datasets (April to December 2020) into a single, unified dataframe.
  2. Standardized date-time formats for `started_at` and `ended_at` columns.
  3. Created a new calculated column named `ride_length` by subtracting the start time from the end time, converting it into minutes.
  4. Created a `day_of_week` column corresponding to the start day of each trip.
  5. Filtered out erroneous records where `ride_length` was less than or equal to zero (e.g., system maintenance rides or invalid logs).
  6. Exported the final cleaned dataset as `cyclistic_2020_clean.csv` into the processed data folder.

---

## Phase 4: Analyze
* **Descriptive Analysis Findings:**
  * **Ride Duration:** Casual riders tend to take significantly longer trips on average (~45.6 minutes) compared to annual members (~16.4 minutes).
  * **Ride Frequency by Day:** Casual riders show peak usage during weekends (Saturday and Sunday), indicating recreational use. Conversely, annual members maintain high, steady usage throughout weekdays (Monday to Friday), consistent with commuting behavior.
* **Business Insight:** Casual riders view Cyclistic primarily for leisure and recreation on weekends, while members rely on it for daily utilitarian transportation. Marketing strategies should focus on highlighting the cost-savings and convenience of annual memberships for frequent or flexible riders.

---

## Phase 5: Share
To effectively communicate these insights to key stakeholders, visualizations were created using Tableau, focusing on clarity, contrast, and professional design.

* **Chart 1 (Average Ride Duration):** This chart clearly illustrates that casual riders take significantly longer trips (averaging over 20 minutes) compared to annual members (around 12 minutes). This highlights a fundamental difference in intent: casual riders use bikes primarily for leisure, recreation, and tourism, while members use them for direct, utilitarian commutes.
  
<img width="225" height="696" alt="Captura de pantalla 2026-07-30 a las 23 46 18" src="https://github.com/user-attachments/assets/2a0a0422-733d-499d-ad45-e8978261bc4d" />


* **Chart 2 (Total Rides by Day of the Week):** This visualization breaks down total ride counts across days of the week by user type. It reveals that casual rider activity surges dramatically during weekends (especially Saturdays and Sundays), whereas annual member usage remains consistently high and stable throughout the weekdays (Monday through Friday).

<img width="605" height="701" alt="Captura de pantalla 2026-07-30 a las 23 48 38" src="https://github.com/user-attachments/assets/fad7c20f-bb28-4192-9b69-961e3d83945d" />

> **Key Story:** The data tells a clear story: Cyclistic has two distinct user segments. Converting weekend leisure riders into routine weekday commuters or offering flexible membership perks for long recreational trips represents our strongest opportunity for growth.

---

## Phase 6: Act

### Conclusion
Based on our comprehensive analysis of Cyclistic’s trip data from April to December 2020, we successfully identified distinct behavioral patterns between annual members and casual riders. Casual riders use bikes primarily for recreational and leisure purposes, with trip durations averaging over 20 minutes and a significant surge in activity during weekends. In contrast, annual members rely on Cyclistic for routine transportation, exhibiting shorter, more direct trips and a steady, high volume of usage during weekdays. 

To maximize annual memberships—the core driver for future company growth—our marketing strategies must bridge the gap between weekend leisure riding and practical, long-term utility.

### Top Three Strategic Recommendations
1. **Targeted Weekend Digital Marketing Campaigns:** Launch focused digital and social media ad campaigns during weekends (specifically Saturdays and Sundays), when casual rider activity peaks. These campaigns should feature promotional discounts or targeted messaging on how upgrading to an annual membership reduces the cost of frequent weekend leisure rides.
2. **Introduce Flexible or Leisure-Oriented Membership Tiers:** Since casual riders take significantly longer trips, design seasonal or leisure-focused membership perks (such as bonus ride minutes or weekend-specific benefits) that provide immediate, tangible financial value to riders who use the service for extended periods.
3. **Strategic QR Code Placement at High-Leisure Stations:** Place informational kiosks or QR codes at docking stations located near major parks, waterfronts, and tourist hotspots in Chicago (high-traffic zones for casual users). These touchpoints should display comparative cost breakdowns, demonstrating how much money frequent casual riders would have saved by purchasing an annual membership.
