# 📊 A/B Testing Analysis: Evaluating the Impact of a New Website Feature

## 🚀 Introduction

This project aims to determine whether the introduction of a **new feature** on a website leads to an **increase in user engagement**, measured by the **average time spent on the website**. To achieve this, we conducted an **A/B test** comparing two groups:

- **Test Group:** 100 participants using the website **with** the new feature.
- **Control Group:** 100 participants using the website **without** the new feature.

The goal is to evaluate if the observed difference in average time spent between these two groups is **statistically significant**.

---

## 📋 Plan of Action

To determine whether the new feature increases user engagement, we need to assess if there is a **statistically significant difference** between the **means of the two samples**. This requires performing a **hypothesis test for the difference in means**.

### ✅ Steps:

1. **Check for Normality:**  
   Determine if the data in both samples follow a **normal distribution** using the **Shapiro-Wilk test**.

2. **Identify the Relationship Between Samples:**  
   Determine if the samples are **paired** (dependent) or **independent**.  
   - Since the test and control groups consist of **different participants**, they are **independent samples**.

3. **Assess Variance Homogeneity:**  
   Verify if the two samples have **equal variances** using tests such as **Levene's test** or **Brown-Forsythe test**.  
   - If variances are equal, we'll use the standard **independent samples t-test**.  
   - If variances are unequal, we'll apply **Welch’s t-test**.

4. **Choose the Appropriate Test:**  
   - If both samples are normally distributed and have equal variances: **Independent Samples t-test**.  
   - If normality is violated: **Mann-Whitney U test** (non-parametric alternative).  
   - If variances are unequal: **Welch’s t-test**.

---

## 📊 Results Interpretation

We can conclude that the difference in the means of the two samples is **statistically significant**, allowing us to **reject the null hypothesis**, which states that there is no difference in the population means. Therefore, we can infer that the new feature effectively **increases user engagement**.

Moreover, since the **variance** in the test group is higher, we can conclude that while the **average time spent on the website has increased**, the **duration varies more significantly between users**.

---

## 🧪 Hypotheses

- **Null Hypothesis (H₀):** There is **no difference** in the average time spent on the website between users with and without the new feature.  
- **Alternative Hypothesis (H₁):** There **is a difference** in the average time spent, indicating the new feature impacts user engagement.

---

## 📦 Project Files

- `AB Testing example.ipynb` - The Jupyter Notebook containing the full statistical analysis, code implementation, and results.

---

## ⚡ Technologies Used

- **Python**
- **NumPy** & **Pandas** for data manipulation
- **SciPy** for statistical tests
- **Matplotlib** & **Seaborn** for data visualization
