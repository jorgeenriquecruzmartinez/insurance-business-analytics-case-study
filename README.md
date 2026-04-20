# Insurance Business Analytics Case Study: Revenue, Claims, Churn, and Customer Value

## Executive Summary

This project analyzes a synthetic but deliberately messy telematics-based insurance portfolio.

Instead of starting from polished tables, I created a multi-table environment where customer records, policy data, driving behavior, support tickets, and claims interact in ways that are useful, inconsistent, and sometimes irritating. That was the point.

The project is not just about reporting premiums or counting claims. The real objective is to study how **operational friction, claims burden, pricing logic, and retention behavior combine to create or destroy customer value**.

At its core, this is a business analytics case study with an economic layer:
not just *what happened*, but *where value leaks*, *which segments carry the portfolio*, and *how operational failures show up financially*.

---

## Why This Project Exists

A lot of portfolio projects look clean because the data is clean. Real work usually is not.

So instead of pretending that analysis starts with perfect tables, I built a synthetic insurance environment with intentional operational noise:
- inconsistent labels
- missing values
- outliers
- duplicate-looking records
- dirty categorical fields
- broken-looking service data
- uneven customer behavior across policies, claims, and support activity

The goal was to simulate something closer to what analysts actually face: a system that broadly makes sense, but still forces you to question, validate, standardize, and decide what is trustworthy.

---

## Business Objective

The main goal of the project is to understand how the portfolio is performing and where business value is being protected or lost.

More specifically, the analysis focuses on:
- portfolio scale and premium generation
- support burden and service friction
- claim cost exposure
- churn and renewal patterns
- customer and policy level profitability

This project is built around one central idea:

**Revenue alone is not the story.**
A customer can pay premiums and still destroy value through claims, support burden, or churn dynamics. So the real task is to identify which parts of the book of business are actually worth keeping, fixing, repricing, or monitoring.

---

## Dataset Structure

The project uses a synthetic relational dataset across multiple CSV tables:

- `customers.csv`
- `vehicles.csv`
- `policies.csv`
- `driving_behavior.csv`
- `support_tickets.csv`
- `claims.csv`
- `financial_summary.csv`

Together, these tables simulate a small insurance operating environment with enough complexity to support both business and economic interpretation.

### Main data themes
- customer demographics and segmentation
- vehicle characteristics
- policy pricing and discounts
- telematics-style driving behavior
- support operations
- claims outcomes and cost
- churn and renewal
- estimated customer value

---

## Technical Approach

The raw dataset was generated in Python using synthetic logic and Faker-based records, but the value of the project is not the fake names or fake emails. The value is in the structure and the mess.

I built the environment so it would require actual cleaning and validation before analysis. That included problems such as:
- inconsistent category labels across tables
- null-heavy operational fields
- messy service data
- malformed or uneven date formats
- outlier values in claims and driving metrics
- duplicate-like entities and noisy identifiers

This created a more realistic workflow:
1. generate the system
2. profile the damage
3. clean only what is necessary
4. preserve useful mess
5. extract business insight

That last part matters. Over-cleaning would make the project feel fake again.

---

## Analytical Framework

The analysis is organized into five business sections:

---

## Section A — Executive KPIs

This is the portfolio-level snapshot.

### Core metrics
- total customers
- total policies
- total premium revenue
- total support cost
- total claim cost
- estimated net value
- churn rate
- renewal rate

### Why it is relevant: This section establishes the basic health of the portfolio and acts as the top-level view of scale, revenue, cost pressure, and retention.

---

## Section B — Operations Health

This section looks at support as a source of friction, cost, and customer dissatisfaction.

### Core metrics
- tickets by issue type
- average resolution time by issue type
- CSAT by channel
- escalation rate by issue type
- refund rate by issue type

### Why it is relevant: Support is not just a service layer. It is an operational cost center and, in some cases, a churn trigger. This section is meant to show where service operations are functioning well and where they are quietly damaging customer value.

---

## Section C — Risk and Claims

This section focuses on risk exposure and realized cost.

### Core metrics
- claims by severity
- claim cost by vehicle type
- claim cost by policy type
- high-risk vs low-risk premium comparison

### Why it is relevant: This is where the insurance logic becomes more than operational reporting. The point is to compare premium intake against claim burden and see whether risk appears to be priced coherently across segments.

---

## Section D — Churn and Retention

This section studies how customers leave, stay, or renew.

### Core metrics
- churn by segment
- churn by premium band
- churn by support burden
- renewal by discount band

### Why it is relevant:Retention is where operations, pricing, and customer experience collide. This section is designed to show whether churn is being driven by cost, support friction, discount behavior, or some combination of all three.

---

## Section E — Profitability

This is the core business value section.

### Core metrics
- net value by segment
- net value by policy type
- negative-value customer share
- top/bottom customer groups
- support cost vs net value
- claim cost vs net value

### Why it is relevant: This project is not interested in success theater.It is interested in value. A portfolio can look healthy in premium terms and still contain segments that are structurally weak once support and claims are accounted for. This section is where those distortions become visible.

---

## Economic Value Interpretation

One of the main ideas behind the project is that business performance should not stop at volume metrics.

To make that concrete, I use an estimated net value framing at the policy level:

**Net Value = Premium Revenue - (Support Cost + Claim Cost)**

This is not meant to be a perfect actuarial model.
It is meant to be a business-facing profitability lens that helps separate:
- revenue-rich but costly customers
- low-friction, high-value segments
- customers who are operationally expensive relative to what they bring in
- policy types that may need repricing or closer monitoring

This is the bridge between standard KPI analysis and economic interpretation.

---

## Main Questions Behind the Analysis

This case study is built to answer questions like:

- Which customer segments generate strong net value?
- Which issue types create the most operational drag?
- Where are support costs and claims costs eroding portfolio value?
- Are discounts helping retention enough to justify margin loss?
- Which policy types appear strongest economically?
- How much churn appears linked to service burden rather than price alone?

---

## Workflow

### 1. Synthetic data generation
A multi-table insurance environment was generated in Python with intentionally messy business logic.

### 2. Data cleaning and validation
The raw tables were profiled, standardized, validated, and prepared for analysis without removing all the friction that made them realistic in the first place.

### 3. KPI and portfolio analysis
The cleaned data was used to evaluate portfolio performance, support operations, claims burden, churn patterns, and policy/customer profitability.

---

## Tools Used

- Python
- pandas
- numpy
- Faker
- JupyterLab


## Dashboard Preview

### Executive Overview

<img width="1179" height="660" alt="1  Executive Overview" src="https://github.com/user-attachments/assets/4e78f2a6-55e1-409c-8a48-415108ae5ac1" />

### Operations Health

<img width="1168" height="656" alt="2  Operations Health" src="https://github.com/user-attachments/assets/dae16fb3-ec20-4b4a-bbe7-43acfd628563" />

### Churn and Retention

<img width="1278" height="712" alt="3  Churn and Retention" src="https://github.com/user-attachments/assets/49bf545d-43ff-43b6-ba9e-b5e09321109e" />

### Risk and Claims

<img width="1276" height="711" alt="4  Risk and Claims" src="https://github.com/user-attachments/assets/11ad3c93-2eb2-4d56-9956-744969a510ee" />

### Profitability

<img width="1269" height="712" alt="5  Profitability" src="https://github.com/user-attachments/assets/31e5a718-f6be-41f6-8317-5b36f007d23a" />

---

## What This Project Demonstrates

This project was built to show more than dashboarding.

It demonstrates:
- synthetic data environment design
- relational data thinking
- messy data cleaning
- operational KPI analysis
- churn and retention analysis
- claims and cost interpretation
- customer value framing
- business storytelling grounded in imperfect data

In other words, this is not just a data visualization exercise. It is an attempt to model how analysis moves from dirty records to business judgment.

---

## Possible Extensions

The project could be extended into:
- churn prediction
- customer value scoring
- risk segmentation models
- claim likelihood modeling
- discount scenario analysis
- interactive dashboards in Power BI, Tableau, or Streamlit

---

## Final Note

This project uses synthetic data only.
No real customer information or real company records are included.

What is real is the analytical problem:
how to extract something useful from a system that is noisy, imperfect, and still expected to produce business answers.
