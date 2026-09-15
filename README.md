[README.md](https://github.com/user-attachments/files/32246578/README.md)
# Project 2: Exploratory Data Analysis (EDA)

## Goal
Analyze an e-commerce orders dataset to understand patterns, trends, and distributions in sales, fulfillment, and customer behavior.

## Dataset
- **1,200 orders**, January 2023 – June 2025
- **14 columns**: OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, TotalPrice
- No missing data except `CouponCode` (309 orders used no coupon)

## Tools Used
Python — pandas, matplotlib, seaborn

## Key Requirements Covered
- Basic statistics (mean, median, count)
- Trend and outlier identification
- Summary of key observations

## Key Observations

### Sales and Pricing
- Average order value is **₦1,053.97**, but the median (**₦823.62**) is notably lower — the distribution is right-skewed, pulled up by a small number of large bulk orders.
- Product demand is fairly evenly spread: Printer (181), Tablet (179), Chair (178), Laptop (173), Desk (170), Monitor (163), and Phone (156) orders — no single product dominates sales.

### Revenue Trend
- Monthly revenue fluctuates between **₦27,752 and ₦68,069** with no sustained upward or downward trend — the business appears flat over the two-and-a-half-year period rather than growing.
- June 2024 was the strongest month; April 2023 was the weakest, with no obvious seasonal pattern.

### Order Fulfillment
- Only about **19%** of orders (231 of 1,200) reach "Delivered" status. Cancelled (250), Returned (247), Pending (237), and Shipped (235) orders are each nearly as common — a bigger operational concern than the topline sales figures suggest.
- Cancellations are spread evenly across products (31–45 each), so no single product is driving the cancellation rate.

### Outliers
- **8 orders** exceed the upper IQR bound on `TotalPrice` (above ₦3,330), topping out at ₦3,456.40. All are legitimate bulk purchases (Quantity = 5 at high unit prices), not data-entry errors — no cleaning action needed.

### Coupons and Channels
- **FREESHIP** is the most-used coupon (313 orders); roughly 26% of orders used no coupon at all.
- **Instagram** (259) and **Email** (250) are the top referral sources, with Facebook and direct referrals trailing slightly.

## Repository Structure
```
├── README.md              # This file
├── eda_notebook.ipynb      # Full analysis with code, charts, and inline commentary
└── data/                   # Dataset (or a link, if data is private/large)
```
