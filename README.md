# Retail Promotions Analysis Using Chi-Square Tests

## Project Overview

This project investigates customer engagement and purchasing behavior within a retail loyalty program using statistical inference for categorical data.

As a marketing analyst, I examined customer responses to three promotional channels—Email, SMS, and App Notifications—to determine whether engagement varies by time of day and whether promotion type is associated with purchase behavior.

The analysis uses Python, data visualization, and chi-square hypothesis testing to identify patterns that can inform marketing strategy.

This project was completed as part of my statistical analysis coursework.

## Research Questions

**1. Time-of-Day Engagement**

Do customers engage with promotional campaigns equally across Morning, Afternoon, and Evening?

- **Null Hypothesis (H₀):** Engagement frequencies are equally distributed across the three time periods.
- **Alternative Hypothesis (H₁):** Engagement frequencies differ from a uniform distribution.

**2. Promotion Type and Purchase Behavior**

Is promotion type associated with whether a customer makes a purchase within seven days?

- **Null Hypothesis (H₀):** Promotion type and purchase behavior are independent.
- **Alternative Hypothesis (H₁):** Promotion type and purchase behavior are associated.

Both tests use a significance level of α = 0.05.

## Technologies Used

- Python
- Pandas and NumPy
- SciPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset

The dataset, `retail_promotions.csv`, contains 3,500 observations and three categorical variables:

| Column | Description |
|---|---|
| TimeOfDay | Morning, Afternoon, or Evening |
| PromotionType | Email, SMS, or AppNotification |
| MadePurchase | Yes or No, indicating purchase within seven days |

Initial exploration confirmed that all 3,500 observations contained values for each column, with no missing values.

## Methodology

### Exploratory Data Analysis

I used Pandas to examine the dataset, calculate category frequencies, and check for missing values.

I created three visualizations:

- Bar chart showing the distribution of promotion types.
- Histogram showing engagement frequency by time of day.
- Pie chart showing the proportion of customers who made a purchase.

### Chi-Square Goodness-of-Fit Test

I tested whether observed engagement frequencies across Morning, Afternoon, and Evening differed significantly from an expected uniform distribution.

Expected frequencies were calculated by dividing the total number of observations equally across the three categories.

### Chi-Square Test of Independence

I constructed a contingency table using promotion type and purchase behavior.

I then used SciPy's `chi2_contingency()` function to test whether the two categorical variables were statistically associated.

Purchase rates were calculated separately for each promotional channel.

## Statistical Results

### 1. Time-of-Day Engagement

| Statistic | Result |
|---|---:|
| Chi-square statistic | 719.59 |
| P-value | < 0.0001 |
| Significance level | 0.05 |
| Decision | Reject H₀ |

The goodness-of-fit test found statistically significant differences in engagement frequencies across the three time periods.

Morning had the highest observed engagement frequency, with 1,906 observations.

These findings suggest that customer engagement is not uniformly distributed throughout the day.

### 2. Promotion Type and Purchase Behavior

| Statistic | Result |
|---|---:|
| Chi-square statistic | 74.07 |
| Degrees of freedom | 2 |
| P-value | < 0.0001 |
| Decision | Reject H₀ |

The test of independence found a statistically significant association between promotion type and purchase behavior.

### Purchase Conversion Rates

| Promotion Type | Purchases | Total Observations | Purchase Rate |
|---|---:|---:|---:|
| App Notification | 255 | 708 | 36.0% |
| SMS | 237 | 993 | 23.9% |
| Email | 354 | 1,799 | 19.7% |

App notifications demonstrated the highest observed purchase rate, despite representing the smallest number of promotions in the dataset.

## Business Recommendations

Based on these findings, I recommend:

1. **Investigating Morning Engagement:** Examine whether scheduling more promotional campaigns in the morning improves engagement rates.
2. **Testing App Notifications:** Conduct controlled experiments to evaluate whether app notifications consistently outperform other promotional channels.
3. **Optimizing Channel Strategy:** Consider purchase conversion rates alongside campaign costs, customer preferences, and overall return on investment.
4. **Monitoring Performance:** Continue tracking engagement and purchasing behavior to identify changing customer patterns.

## Limitations

Although the chi-square tests identified statistically significant patterns, the analysis does not establish causation.

Higher morning engagement counts could reflect differences in the number of promotions delivered or accessed during each period rather than an inherent preference for morning engagement.

Similarly, differences in purchase rates across promotional channels may be influenced by customer demographics, campaign targeting, or other confounding variables.

Further controlled experiments would help determine which marketing strategies produce the strongest results.

## Conclusion

This project demonstrates how statistical inference for categorical data can support evidence-based marketing decisions.

The analysis found significant differences in engagement frequencies by time of day and a significant association between promotion type and purchasing behavior.

Morning engagement and app notifications emerged as promising areas for further investigation, providing the marketing team with actionable directions for future experimentation and campaign optimization.