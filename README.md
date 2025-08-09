# Hospital Meal Planning Optimization  
#### *"Optimizing cost-effective and nutritionally balanced meal plans for hospital patients with diverse dietary needs."*

![](https://github.com/SnehaEkka/BA885-Meal-Planning-Optimization-Model/blob/main/meal-planning.jpg)

## About  
This project develops an optimization framework for planning hospital meals that meets patient-specific nutritional requirements and dietary restrictions, while minimizing overall food purchasing costs. The approach balances cost efficiency, food diversity, and dietary practicality for a retirement home setting with 50 residents over a weekly planning horizon.

## Problem Statement  
Hospitals and healthcare facilities face the challenge of providing nutritionally adequate, diverse, and cost-effective meals tailored for patients with different medical conditions such as diabetes and cardiovascular diseases. This project models the weekly meal ordering process to optimize cost savings while satisfying these complex dietary constraints.

## Optimization Model

- **Objective:** Minimize total weekly food purchase cost for all residents.  
- **Decision Variables:** Quantities of 24 food items assigned per resident per week.  
- **Constraints:**  
  - Nutritional constraints (calories, protein, carbohydrates, lipids, fiber, added sugar) based on individual patient needs scaled from ESPEN guidelines.  
  - Dietary restrictions including lactose and gluten sensitivities.  
  - Food group minimum portions (e.g., vegetables, fruits) to ensure variety.  
  - Scenario 2 introduces a minimum variety requirement with binary variables to encourage food diversity per resident.  
  - Scenario 3 adds daily serving limits to balance variety and practical meal portions.

## Data

- Nutritional values and prices for 24 food items sourced from Amazon Business and nutritional info tables.  
- Patient weight and dietary requirements based on a synthetic dataset simulating 50 residents with realistic variability in body weights and nutritional needs.  

## Key Scenarios and Outcomes

| Scenario                         | Cost (Weekly) | Notes                                                  |
|---------------------------------|---------------|--------------------------------------------------------|
| Baseline (Min Cost)              | $3,059.87     | Lowest cost but minimal diversity; impractical for meals. |
| Added Food Diversity             | $3,151.45     | Encourages variety but can misalign with daily serving needs. |
| Balanced Variety + Serving Limits| $4,744.63     | Most practical daily plan with diverse and balanced portions. |

## Sensitivity and Analysis

- Nutritional constraints are binding in many cases, particularly minimum requirements for carbohydrates, lipids, and vegetables.  
- Allowable price increase analysis indicates some food items are price sensitive, impacting optimized solution stability.  
- Shadow price analysis highlights which constraints restrict cost minimization and where trade-offs occur.

## Business Impact

- **Cost Savings:** Demonstrates potential to minimize food expenses while respecting patient health needs.  
- **Operational Efficiency:** Provides actionable, practical meal orders to support hospital procurement teams.  
- **Patient Care:** Incorporates dietary restrictions and nutritional guidelines, supporting individualized patient health outcomes.  
- **Scalability:** Framework can be extended to other healthcare or institutional food service settings for optimized meal logistics.

## How to Run  

1. Clone the repository.  
2. Install necessary Python packages (e.g., pandas, numpy, scipy, Pyomo or another solver interface).  
3. Open the main Excel file and Jupyter notebooks provided for data modeling, optimization, and sensitivity analysis.  
4. Run optimization scenarios sequentially to compare cost and diversity trade-offs.  
5. Customize nutritional parameters or cost inputs to adapt to different patient populations or suppliers.

## Future Improvements

- Integrate more granular meal timing constraints (breakfast, lunch, dinner).  
- Expand dataset to include additional dietary restrictions and patient demographics.  
- Automate order generation and interface with hospital procurement software.  
- Incorporate stochasticity in supply and demand for dynamic meal planning.

## Coursework & Contributors
- **Coursework:** Completed as part of **BA885 - Advanced Analytics & Optimization** course (Boston University MSBA program) with a focus on optimization modeling, healthcare analytics, and operational research.
- **Contributors:** Riris Grace, Victor, Ya Ya, Sneha Ekka  

## Additional Resources  

- [Presentation Deck](https://www.canva.com/design/DAGX-rLYj1Q/KHFH45tZrQV9TbDDOFtpfg/view?utm_content=DAGX-rLYj1Q&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hefcca586bb)  
- [Full Project Report](BA885-Team-10-Project-Report.pdf)
