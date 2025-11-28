#Professional Climbing Performance Analysis

This project explores trends in **professional sport climbing performance** using historical competition data. We analyze how performance changes with **age, gender, and country**, as well as how the professional climbing landscape has evolved over time.

The goal is to extract meaningful insights about:
- Peak performance age  
- Long-term shifts in competitor demographics  
- Countries that historically produce top climbers  
- How national dominance has changed over time  

---

##Dataset Summary

This dataset consists of professional climbing competition results collected across multiple decades.

### Key Features:
- **Athlete demographics:** Age, gender, country  
- **Performance metrics:** Raw score ("true score") and engineered averages  
- **Temporal features:** Competition year  
- **Participation data:** Number of climbers per country per year  

---

##Project Objectives

1. Analyze how **age impacts performance** for male and female climbers.
2. Investigate whether the **average age of competitors** is trending younger over time.
3. Identify **which countries produce the best climbers** based on performance.
4. Track how the **number of pro climbers per country changes over time**.
5. Explore **country performance trends** across historical periods.

---

##Key Findings

### 1. Age vs Performance
- Raw performance scores were **left-skewed**, with most climbers aged **18–30** scoring between **0–58 points**.
- A strong performance drop occurs after **40 years old** — no athletes surpassed **20 points** beyond this age.
- Polynomial regression on raw scores did not model well due to high variability.
- After feature engineering (using **average score**), performance vs age shows a clearer pattern:
  - **Women peak at ~27**, with a steep rise and fall.
  - **Men peak at ~31**, with a much flatter performance curve — indicating longer high-performance longevity.

---

### 2. Competitor Age Trends Over Time
Average competitor age is decreasing:

| Group  | Age Change Per Year |
|--------|---------------------|
| Men    | -0.0585 years/year  |
| Women  | -0.1775 years/year  |

- The trend is visually clear even before regression.
- Regression confirmed a **negative slope** for both.
- Female competitors are getting younger faster than males.

---

### 3. Countries Producing the Best Climbers
Based on **average performance scores**, the top three countries were:

1. 🇫🇷 **France (~29 points)**
2. 🇦🇹 **Austria (~24 points)**
3. 🇯🇵 **Japan (~21 points)**

---

### 4. Pro Climbers by Country Over Time
- **France dominated in 1995** in terms of competitor count.
- By ~2005, most countries were fairly evenly represented.
- By 2019, **USA, Slovenia, Japan, and Russia** had the highest number of professional climbers.

This suggests a globalization of elite climbing talent.

---

### 5. Country Performance Trends Over Time
Performance leadership changed frequently:

- 🇯🇵 Japan had extreme dominance early (1991 peak ~80 average score), but declined rapidly afterward.
- Other countries had individual "winning periods":
  - 🇺🇸 USA ~53 average score peak
  - 🇸🇮 Slovenia ~52
  - 🇦🇹 Austria ~50
  - 🇫🇷 France ~45  

By 2019:
- All leading countries converged to **similar average scores (10–30)**.
- Suggests increasing global parity in professional climbing performance.

---

##Model Insights

- Polynomial regression only worked effectively **after feature engineering** via score averaging.
- Raw climbing performance shows high variance and noise—aging effects are clearer when smoothing is applied.
- Trends over time show consistent structural change in demographics and national participation.

---

##Limitations

1. **Data completeness:** Not all competitions or athletes may be represented.
2. **Scoring consistency:** Scoring systems may have evolved over time.
3. **Survivorship bias:** Older climbers that remain may represent unusually strong performers.
4. **Country bias:** Some countries may underreport or have lower participation rates historically.
5. **External factors:** Social, economic, or Olympic inclusion effects were not modeled.

---

##Deliverables

This project includes:
- Full EDA notebook
- Data cleaning and preprocessing pipeline
- Visual analysis of:
  - Age vs performance
  - Country dominance
  - Participation trends
- Final report with findings and limitations

---

##Final Notes

This project reveals a clear evolution of professional sport climbing:
- Performance peaks are well-defined by age and gender.
- The sport is getting younger, especially among women.
- Country dominance evolves over time — with increasing international parity.

Future work could explore:
- Event-specific performance differences
- Predictive models for performance decline
- Impact of Olympic inclusion on participation
