# Vodafone Order Delivery Performance Tracker

A Power BI dashboard analyzing the end-to-end order fulfillment funnel for 
Vodafone product orders (SIM cards, routers, smartphones, smartwatches, 
tablets), tracking confirmation, shipping, and delivery performance, 
logistics partner reliability, payment method mix, and delivery status 
across cities.

## Tools Used
- Power BI (data modeling, DAX measures, interactive visuals)
- Excel / CSV for source data

## Dataset
177 orders covering product category, order date, ship date, delivery date, 
delivery status, logistics partner, payment method, and delivery city.

## Key Insights

- **Funnel drop-off is concentrated at delivery, not shipping:** the 
  Order Confirmation Rate (90.40%) and Ship Rate (99.38%) are both strong, 
  but Delivery Rate falls to 94.34% — meaning most fulfillment failures 
  happen after an order ships, not before.
- **Nearly half of deliveries are late:** only 57.33% of deliveries are 
  on-time, against a 42.67% delay rate — this is the dashboard's single 
  biggest red flag and the natural starting point for a root-cause deep dive.
- **SIM cards and electronics dominate order volume:** SIM Card (47) and 
  Router (36) lead by product, while Electronics (63) is the largest order 
  category overall, ahead of Lines (47), AT HOME (36), and Wearables (31).
- **Logistics partners perform unevenly:** DHL handles the largest share 
  of orders (55, 31.07%), followed by Bosta (50, 28.25%), Aramex (38, 
  21.47%), and FedEx (34, 19.2%) — worth cross-referencing partner share 
  against the 42.67% delay rate to see which partner is driving late 
  deliveries.
- **Cash on Delivery is the leading payment method** (69, 38.98%), ahead of 
  Card (48, 27.12%) and Wallet (60, 33.9%) — a high COD share can itself 
  contribute to delivery friction (failed collections, refused orders) and 
  is worth flagging alongside the delay analysis.
- **Order volume is volatile with sharp spikes:** both order-date and 
  delivery-date trends show irregular peaks (e.g., a spike to 5 orders in 
  one week vs. a baseline of 1–2) rather than steady, predictable volume — 
  suggesting demand is driven by specific promotions or launch events rather 
  than organic steady-state ordering.
- **City-level delivery counts drop off gradually:** East Market leads at 
  86 orders, tapering steadily down to ~61 for the lowest cities shown — no 
  single city is a dramatic outlier, indicating fairly even geographic 
  distribution rather than concentration in one region.

## Dashboard Pages
1. **Order Delivery Performance Tracker** — full funnel KPIs, product/category 
   breakdown, logistics partner and payment method analysis, order/delivery 
   date trends, and city-level delivery status

## How to Use
1. Download the `.pbix` file from this repo
2. Open in Power BI Desktop
3. Use the filter panel (left sidebar) to slice by logistics partner, 
   payment method, or product category
