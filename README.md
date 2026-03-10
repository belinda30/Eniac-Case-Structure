# Eniac A/B Test Analysis: Optimising User Engagement

## 🚀 Project Overview

This project performs a rigorous statistical analysis of an A/B test conducted for **Eniac**. The goal was to determine which combination of button color (White vs. Red) and Call-to-Action text ("Shop Now" vs. "See Deals") yields the highest Click-Through Rate (CTR) on the landing page.

## 📊 The Dataset

The analysis is based on four distinct website versions tested over a 14-day period with a total sample size of over 100,000 visits:

* **Version A:** White Button - "Shop Now" (25,326 visits)
* **Version B:** Red Button - "Shop Now" (24,747 visits)
* **Version C:** White Button - "See Deals" (24,876 visits)
* **Version D:** Red Button - "See Deals" (25,233 visits)

## 🛠️ Methodology

To ensure the results were not due to random chance, a two-stage statistical approach was used:

1. **Chi-Square Test of Independence:** Used to determine if there is a significant relationship between the button version and user clicks.
* **Null Hypothesis ($H_0$):** All versions have the same CTR.
* **Result:** $p \approx 0$ ($2.71 \times 10^{-48}$), indicating a highly significant difference.


2. **Post-Hoc Analysis (Pairwise Testing):** Since the Chi-Square test only indicates that *a* difference exists, I performed 6 pairwise comparisons using a **Post-hoc Analysis**.
* **Adjusted Alpha:** $0.05 / 6 = 0.0083$.



## 📈 Key Findings

* **The Winner:** **Version C (White - "See Deals")** achieved the highest raw CTR (2.12%), though it was statistically tied with **Version A**.
* **Color is King:** White buttons significantly outperformed Red buttons across all text variations ($p < 0.001$).
* **Text Impact:** For Red buttons, "Shop Now" performed significantly better than "See Deals." However, for White buttons, the text change did not produce a statistically significant difference ($p = 0.46$).

## 💻 Tech Stack

* **Python** (Pandas, NumPy)
* **SciPy** (Statistical testing)
* **Matplotlib/Seaborn** (Data visualisation)
