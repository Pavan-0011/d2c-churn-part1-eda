# Data Quality Report

## Missing Values

### customers.csv

- loyalty_tier contains substantial missing values.
- skin_type contains moderate missing values.

### orders.csv

- rating contains missing values.

## Duplicate-like Records

orders.csv contains records ending with _DUP.

Recommendation:
Investigate before model development.

## Outliers

gross_amount contains extreme values above normal purchasing range.

Recommendation:
Use IQR or percentile-based capping.

## Join Issues

All datasets join through customer_id.

Some customers do not have support tickets.

This is expected behavior.

## Leakage Risk

orders after 2025-09-30 must not be used for feature creation.

Target window information must never be used as model input.