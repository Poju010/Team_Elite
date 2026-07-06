# ZenithMart Retail Group — Branch Performance Analysis

Branch performance and sales trend analysis across ZenithMart's 5 Nigerian branches (FY2023–FY2024), built for a board review presentation using Microsoft Excel.

![Dashboard Placeholder](C:\Users\HomePC\Desktop\DEC HACKATHON)

## Business Problem

HQ received 24 months of raw transactional data from all five branches and needed to know: which branches and categories are actually performing, why, and what to do about it — since raw sales totals alone don't account for branch size, targets, or category mix.

**Core questions:**
- Which branch generates the most value, and which underperforms its target?
- Which categories drive revenue, and which are under-target?
- Do satisfaction and returns vary meaningfully across branches?
- What does the 2-year trend say about seasonality and growth?

## Dataset

- **5,500 transactions** (1,100 per branch) across **Lagos Island, Abuja Central, Port Harcourt, Ibadan, Kano**
- **Period:** Jan 2023 – Dec 2024
- **18 fields**: date, branch, rep, customer, category, product, qty, price, sales, discount, payment method, satisfaction, returns, stock, target

## Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Cleaning, SUMIFS/COUNTIFS/AVERAGEIFS, PivotTables, dashboard |
| Microsoft PowerPoint | Board presentation |

## Data Cleaning

- Trimmed trailing whitespace in branch names (e.g. `"Lagos Island "`)
- Fixed a full column swap between Satisfaction Score and Return Flag on one branch
- Excluded out-of-range satisfaction scores (0, 6, 7) and invalid return flags from calculations (not imputed)
- Left missing Payment Method (20.5%), Discount % (16.6%), and Phone (17.0%) blank rather than guessing

## Visualizations

> Add screenshots to `docs/images/` and link them here.

- Branch performance ranking (bar chart)
- 2-year sales trend (line chart)
- Branch contribution to total sales (donut chart)
- Category performance vs. target (clustered bar)

## Key Findings

- **NGN 3.76B** total group sales, **104.1%** of target, but growth was nearly flat YoY (**+3.1%**)
- **Port Harcourt** leads at NGN 861.7M (112.4% of target); **Lagos Island** is the only branch below target (97.6%)
- **Electronics** is at 181.5% of target while **Groceries** sits at just 22.4% — targets are miscalibrated, not poorly executed
- Satisfaction (~3.0/5) and return rate (~28–29%) are flat across all branches — **basket size**, not service quality, explains the performance gap (Port Harcourt: NGN 783K avg basket vs. Lagos Island: NGN 658K)
- **Port Harcourt** alone drives 22.9% of group revenue — a concentration risk if operations there are disrupted
- 20.5% of transactions have no recorded payment method, weakening confidence in channel-mix conclusions

## Recommendations

- [ ] Re-baseline category sales targets using 2-year actuals
- [ ] Run a basket-building/upsell program at Lagos Island and Kano
- [ ] Fix payment-method data capture at point of sale
- [ ] Build a Port Harcourt business-continuity plan
- [ ] Launch a mid-quarter promotion for the recurring June/March dip

## How to Reproduce

```bash
git clone https://github.com/<your-username>/zenithmart-branch-performance.git
```
Open `TEAM_ELITE.xlsx` for the cleaned dataset, pivots, and dashboard, and `TEAM_ELITE_EFM.pptx` for the full board presentation.

## Team

**Team Elite** — Olokooba Fuwad, Ogunleye Mariam, Adepoju Emmanuel
