# Products-Data-Analysis

## Report link:
https://app.powerbi.com/links/AVyk--QTjy?ctid=5bcca112-41e4-4d5e-a805-c5ba21ed65b6&pbi_source=linkShare

## Problem Statement

This project analyzes agricultural product availability, demand, and profitability using data imported from MySQL Server. The goal is to provide insights into:

- **Availability vs Demand**→ How well supply meets demand

- **Profitability** → Which products and regions generate the most profit

- **Supply Shortages** → Identifying products/regions with frequent shortages

- **Loss Analysis** → Quantifying overall system inefficiencies

- **Demand Trends**→ Understanding consumption patterns for better planning

By using DAX measures and Power BI, this dashboard enables stakeholders to optimize supply chain decisions, reduce shortages, and maximize profit.

## Steps Followed

**Step 1:** Imported agricultural products dataset into MySQL Server and connected to Power BI.

**Step 2:** Cleaned the dataset (handled missing values, duplicates, and invalid quantities).

**Step 3:** Created a Measures Table to store all DAX measures.

**Step 4:** Designed visuals for availability, demand, shortages, and profitability.

**Step 5:** Built KPIs for Profit, Loss, and Shortages.

**Step 6:** Published interactive dashboards to Power BI Service.

## DAX Measures

- Total availability = SUM('Demand/availability'[Availability])

- Total demand = SUM('Demand/availability'[Demand])

- Average availability = AVERAGE('Demand/availability'[Availability])

- Average demand = AVERAGE('Demand/availability'[Demand])

- Average Daily Demand = 
    AVERAGEX(
        VALUES('Demand/availability'[Date]),
        [Total demand]
    )

- Total Profit = SUM('Demand/availability'[Profit])

- Total Loss = SUM('Demand/availability'[Loss])

- Total number of Orders = DISTINCTCOUNT('Demand/availability'[OrderID])

- Total supply shortage = SUM('Demand/availability'[Shortage])

## Insights
- **Demand & Availability**

On average, demand slightly exceeds availability, leading to supply gaps.


- **Supply Shortages**

Total shortages account for ~15–20% of demand.

- **Profitability**

Despite shortages, profit margins remain strong in high-demand products.



- **KPIs**

-  Total Profit → Highlights overall financial gains.

-  Total Loss → Quantifies inefficiencies.

-  Shortage KPI → Helps track unmet demand.

  ## Conclusion

This  Dashboard provides a holistic view of demand, availability, profit, and shortages. With strong DAX measures and interactive Power BI visuals, it supports stakeholders in making data-driven decisions for:

- Better supply-demand alignment

- Reducing shortages & losses

- Improving profit margins
