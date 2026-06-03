# E-Commerce Customer Segmentation — RFM Analysis

Full RFM (Recency, Frequency, Monetary) customer segmentation model for an e-commerce business with **2,000 customers** and **£6M+ revenue**. Segments customers into 7 behavioural clusters and maps each to a targeted marketing action.

## Business Problem
- No visibility on which customers are high-value vs about to churn
- Generic email blasts with no personalisation — low conversion
- Retention team had no framework to prioritise outreach

## BA Approach
1. Applied RFM methodology — scored each customer on Recency, Frequency, and Monetary value (quintile-based)
2. Mapped R/F score combinations to 7 named behavioural segments
3. Produced a **Segment-to-Action Mapping** document: channel, message type, priority, and business goal per segment

## Key Findings
| Segment | Customers | Revenue Share | Action |
|---------|-----------|---------------|--------|
| Champions | ~30% of base | 87.3% of revenue | Retain & upsell |
| At Risk | 185 customers | £172K recoverable | Win-back campaign |
| Loyal Customers | — | High | Grow share of wallet |
| Lost | — | Low | Low-cost reactivation |

## Tech Stack
`Python` `Pandas` `NumPy` `Scikit-Learn` `Matplotlib`

## Setup
```bash
pip install -r requirements.txt
python rfm_analysis.py
```

## Output Files
```
outputs/
├── rfm_dashboard.png             # Visual dashboard (4 panels)
├── rfm_scored_customers.csv      # All customers with R, F, M scores + segment
├── segment_action_mapping.csv    # Segment-level summary + marketing actions
└── at_risk_customers.csv         # At-Risk + Cant Lose Them — filtered for CRM upload
```

## Dashboard Panels
1. **KPI Cards** — Total customers, revenue, Champions share, at-risk recovery value
2. **Revenue Share by Segment** — Horizontal bar ranked by value contribution
3. **Customer Distribution** — Donut breakdown by segment size
4. **RFM Scatter** — Recency vs Monetary coloured by segment
5. **Avg Customer Value** — Per-segment average CLV

---
*Segment-to-Action mapping designed to be imported directly into CRM (HubSpot / Salesforce) for automated campaign triggers.*
