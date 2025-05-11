# E‑commerce Growth & Retention Case Study

## 1. Business Story & Context
An online retailer doubled his SKU count in 2019 and wants to understand:
- How new vs existing customers fuel revenue ?
- Seasonality in acquisition and retention ?
- Which marketing channels yield the best ROI ?
- The operational levers (region, delivery fees, taxes) that move order value ?

## 2. Information about data 
| File                   | Rows   | Grain                   | Key Variables                                         |
|------------------------|--------|-------------------------|-------------------------------------------------------|
| `Online_Sales.csv`     | 52,924 | Line‑item transactions  | `transaction_date`, `avg_price`, `delivery_charges`   |
| `CustomersData.xlsx`   | 1468   | Customer master         | `customerid`, `demographics`                          |   
| `Marketing_Spend.csv`  | 365    | Monthly budget          | `online_spend`, `offline_spend`                       |
| `Discount_Coupon.csv`  | 204    | Campaign plan           | `month`, `product_category`, `discount_pct`           |
| `Tax_Amount.xlsx`      | 20     | Tax schedule            | `product_category`, `gst`                             |

## 3. EDA & Analytical Logic
1. **Data hygiene** – Type & null scans; unified column names.  
2. **Customer lifecycle**  
   - Monthly acquisition & retention rates  
   - New vs existing revenue mix  
   - Cohort heatmap & cumulative Lifetime value
3. **Marketing efficiency**  
   - ROI calculation (revenue vs spend)  
   - Online vs offline correlation  
4. **Segmentation & targeting**  
   - RFM tiers & revenue share  
   - Top‑10 SKU concentration  
5. **Operational drivers**  
   - Geographical & delivery‑fee impact  
   - Regression of net_revenue on GST & delivery charges  
   - Category/time seasonality  

## 4. Key Visualizations
See `/figures/`:  
- `acquisition_rate.png`, `retention_rate.png`,  
- `new_vs_existing_revenue.png`, `marketing_roi.png`,  
- `rfm_tier_revenue_share.png`, `cohort_heatmap.png`,  
- `category_seasonality.png`, `weekday_revenue.png`, etc.

## 5. Insights & Recommendations
- **Seasonal acquisition:** Ramp up campaigns in January & March; scale back in September/November.  
- **Retention focus:** Peak retention ~ 70 % in August → analyze what drove these cohorts.  
- **Reallocate spend:** Shift ~ 15 % of offline budget to online (r_online 0.85 > r_offline 0.79).  
- **Loyalty program:** Top 6 % of customers deliver 34 % of revenue—launch VIP perks.  
- **Delivery strategy:** High fees correlate with larger baskets but risk churn—test tiered shipping.  
- **Inventory timing:** Stock electronics heavily in Q4; plan Friday‑focused promotions.
