# A/B Testing Analysis Report for TechCorp Digital Platform  

---

## Table of Contents  
1. [Project Name](#project-name)  
2. [Project Background](#project-background)  
3. [Project Goals](#project-goals)  
4. [Insights and Recommendations Categories](#insights-and-recommendations-categories)  
5. [Data Structure & Initial Checks](#data-structure--initial-checks)  
6. [Executive Summary](#executive-summary)  
7. [Insights Deep Dive](#insights-deep-dive)  
8. [Recommendations](#recommendations)  
9. [Technical Details](#technical-details)  
10. [Assumptions and Caveats](#assumptions-and-caveats)  

---

## Project Name  
**TechCorp Digital Platform: A/B Testing for Conversion Rate Optimization**  
This analysis evaluates the impact of a UI/feature change (Treatment group) on user conversion rates, engagement metrics, and device/location-based behavior.  

---

## Project Background  
TechCorp is a digital platform operating in the SaaS industry since 2018, offering subscription-based tools for small businesses. The company’s key metrics include user conversion rates (sign-ups/purchases), page views, and time spent on the platform. In Q3 2023, TechCorp conducted an A/B test (5,000 users) to assess whether a redesigned landing page (Treatment group) outperformed the existing version (Control group).  

---


## Project Goals  
As a data analyst at TechCorp, this analysis aims to:  
1. Determine if the Treatment group’s conversion rate is statistically significant.  
2. Compare engagement metrics (time spent, page views) between groups.  
3. Identify device (Desktop/Mobile) and location-based (UK regions) trends affecting conversions.  
4. Provide actionable recommendations to scale successful variants.  

---

## Insights and Recommendations Categories  
1. **Conversion Rate Analysis**  
2. **User Engagement Metrics**  
3. **Device and Location Impact**  
4. **Statistical Significance**  

---

## Data Structure & Initial Checks  
**Dataset:** Single CSV file (`ab_testing.csv`) with **5,000 records** (collected July–September 2023).  

**Columns:**  
- **User ID**: Unique identifier.  
- **Group**: Control (2,519 users) vs. Treatment (2,481 users).  
- **Page Views**: Total pages viewed per user (range: 1–9).  
- **Time Spent**: Seconds spent on the platform (range: 318–424).  
- **Conversion**: Binary outcome (Yes/No).  
- **Device**: Desktop (52%) or Mobile (48%).  
- **Location**: UK regions (England, Scotland, Wales, Northern Ireland).  


![Screenshot_4-4-2025_0177_dbdiagram io](https://github.com/user-attachments/assets/528349e1-bcdd-4866-86d6-e56f63c46d98)

**Initial Checks:**  
- No missing values or duplicates.  
- Group labels standardized to "Control" and "Treatment."  

---

## Executive Summary  
**Key Findings:**  
1. The Treatment group’s conversion rate (**14.07%**) is **2.6x higher** than the Control group (**5.40%**), with statistical significance (p < 0.001).  
2. Desktop users contributed **61.7%** of total time spent, despite similar device distribution.  
3. Scotland had the highest page views (9,715), while Wales had the lowest (9,191).  
4. The Treatment group drove a **8.67% uplift** in conversions, with a confidence interval of [7.3%, 10%].  



---

## Insights Deep Dive  

### Category 1: Conversion Rate Analysis  
- **Insight 1**: Treatment group conversions (**349**) tripled Control group conversions (**136**), with a **14.07% vs. 5.40%** rate.  
- **Insight 2**: The uplift (**8.67%**) exceeds the minimum detectable effect (delta = 1%).  
- **Insight 3**: Confidence interval [7.3%, 10%] confirms the Treatment’s positive impact.  
- **Insight 4**: Statistical significance (Z-score = 10.44, p < 0.001) rejects the null hypothesis.  

**Visualization:**  
![67514ea6-54f0-40fb-b865-94b4b1d6ffb4](https://github.com/user-attachments/assets/8eac91a1-f420-4664-bae5-5ef6e743435d)



### Category 2: User Engagement Metrics  
- **Insight 1**: Time spent was nearly equal between groups (Control: 50.22%, Treatment: 49.78%).  
- **Insight 2**: Desktop users spent **617,205 seconds** vs. Mobile’s **595,358 seconds**.  
- **Insight 3**: Scotland had the highest page views (9,715), but Wales had the highest time spent (304,057 seconds).  



### Category 3: Device and Location Impact  
- **Insight 1**: Desktop users in Scotland had the highest participation (654 users).  
- **Insight 2**: Mobile users in England showed the lowest conversion rates (5.2%).  
- **Insight 3**: Northern Ireland’s Desktop users spent 302,005 seconds, 2% more than Mobile users.  
 

### Category 4: Statistical Significance  
- **Insight 1**: Pooled variance (0.000069) ensured precise effect size measurement.  
- **Insight 2**: Margin of error (0.83%) validated the robustness of results.  
- **Insight 3**: Critical value (1.64) and test statistic (-10.44) confirmed significance.
  
![Screenshot_4-4-2025_01132_chatgpt com](https://github.com/user-attachments/assets/09d68d5f-199d-4e2a-b26e-e313bf4f2bb6)

---

## Recommendations  
1. **Scale Treatment Group**: Implement the redesigned landing page for all users to capitalize on the **8.67% conversion uplift**.  
2. **Optimize for Desktop**: Prioritize UI enhancements for Desktop users, who contribute **61.7%** of engagement time.  
3. **Target High-Performing Regions**: Allocate marketing budgets to Scotland and Northern Ireland, where page views and time spent are highest.  
4. **Mobile Interface Review**: Investigate low Mobile conversions (e.g., load times, mobile-responsive design).  
5. **Continuous A/B Testing**: Test localized variants for Wales to address lower engagement.  

---

## Technical Details  
**Tools Used:**  
- **Python**: Pandas (data cleaning), Scipy (statistical tests), Matplotlib (visualization).  
- **Jupyter Notebook**: Reproducible analysis and documentation.
- **Figma**
- **Power Bi**
 

---

## Assumptions and Caveats  
1. **Data Completeness**: Assumed no missing data after initial checks.  
2. **Temporal Scope**: Data reflects Q3 2023; seasonal trends (e.g., holidays) were not considered.  
3. **Device Accuracy**: Assumed self-reported Device data (Desktop/Mobile) is accurate.  
4. **Location Granularity**: Regions (e.g., Scotland) were analyzed as broad categories.  

--- 
