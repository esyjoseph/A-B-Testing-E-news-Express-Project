# E-news Express A/B Test Analysis

This repository contains a statistical analysis of an A/B test conducted by me for the data and buiness of **E-news Express** to evaluate whether a **new landing page** leads to greater user engagement and higher conversion rates compared to the **old (control) landing page**.

---

## Table of Contents
1. [Project Overview](#project-overview)  
2. [Dataset Description](#dataset-description)  
3. [Objectives & Key Questions](#objectives--key-questions)  
4. [Methodology](#methodology)  
5. [Findings & Results](#findings--results)  
6. [Recommendations](#recommendations)  
7. [License](#license)

---

## Project Overview
E-news Express suspected that its **existing landing page** was less effective at retaining visitors and converting them into subscribers.  
- A **new landing page** was designed to address these concerns.  
- An **A/B test** was carried out to compare user behavior between the **old** and **new** pages.  

This analysis aims to determine if the new design significantly impacts **time on page**, **conversion rates**, and whether any differences depend on **preferred language**.

---

## Dataset Description
- **File Name**: `abtest.csv`  
- **Number of Rows**: 100 (randomly assigned users)  
- **Columns**: 6  
  - **user_id**: Unique user identifier  
  - **group**: Group assignment (`control` or `treatment`)  
  - **landing_page**: Landing page type (`old` or `new`)  
  - **time_spent_on_the_page**: The amount of time (in minutes) a user spent on the page  
  - **converted**: Whether the user subscribed (`yes` or `no`)  
  - **language_preferred**: The user’s preferred language (`English`, `Spanish`, `French`)  

This dataset was carefully balanced to ensure 50 users in the **control/old** group and 50 in the **treatment/new** group.

---

## Objectives & Key Questions
1. **Time Spent**  
   - Are users spending **more time** on the new landing page than on the old landing page?

2. **Conversion Rate**  
   - Does the **new landing page** yield a significantly **higher conversion rate** compared to the old page?

3. **Language Dependence**  
   - Does **preferred language** influence the likelihood of conversion? Are these two variables independent?

4. **Time by Language**  
   - For the **new** landing page, does **time on page** differ significantly among English, Spanish, or French users?

By answering these, the project helps E-news Express decide whether to **deploy** the new design and how user behavior varies by **language** or page type.

---

## Methodology
1. **Data Exploration**  
   - Verified data quality: no missing values or duplicates.  
   - Calculated summary statistics for `time_spent_on_the_page`.

2. **Statistical Tests**  
   - **Independent Two-Sample t-Test**: Compared mean time on page (old vs. new).  
   - **Two-Proportion Z-Test**: Compared conversion rates (old vs. new).  
   - **Chi-Square Test**: Checked if conversion status and language are independent.  
   - **One-Way ANOVA**: Determined if time on the new page differs among languages.

3. **Significance Level**  
   - Used **α = 0.05** (5% significance) for all hypothesis tests.

4. **Tools & Libraries**  
   - Python (pandas, numpy, seaborn, matplotlib, scipy)  
   - Jupyter Notebook environment for coding and analysis.

---

## Findings & Results
1. **Time on Page**  
   - Users on the **new landing page** spent significantly **more time** than those on the old page (p-value < 0.05).

2. **Conversion Rate**  
   - The **new page** showed a **significantly higher** conversion rate compared to the old page (p-value < 0.05).

3. **Language & Conversion**  
   - **No significant association** was found between preferred language and conversion status (Chi-square p-value > 0.05).

4. **Time by Language**  
   - Among users on the new page, **no significant difference** in time spent across English, Spanish, and French speakers (ANOVA p-value > 0.05).

Overall, the A/B test results strongly suggest adopting the **new landing page** due to its positive impact on engagement and conversions.

---

## Recommendations
1. **Roll Out the New Page**  
   - Implement the **new landing page** as the default, given its improved performance in user engagement and conversions.

2. **Further Optimization**  
   - Continue refining page elements (calls-to-action, layout, content) to maintain or enhance the **time on page** advantage and **conversion** gains.

3. **Targeted Experiments**  
   - While language did not statistically affect conversions, consider micro-tests (e.g., localized content or personalized language) to see if incremental changes can benefit specific language groups.

4. **Ongoing A/B Testing Strategy**  
   - Use smaller iterative A/B tests to optimize **individual components** (headline, images, button placement) on top of the new design.

---


## License
This project is released under the [MIT License](LICENSE.txt). You’re free to use, share, or modify the code and findings. 

---

**Thank you for exploring the E-news Express A/B Test Analysis!** 
Feel free to share any issues, suggestions, or feedback on improvements.
theestherjoseph@gmail.com
