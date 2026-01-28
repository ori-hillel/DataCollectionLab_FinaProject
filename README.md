# Airbnb ROI Optimizer

This Databricks notebook provides a data-driven decision support system for Airbnb hosts. It combines machine learning with combinatorial optimization to recommend the specific amenity upgrades that will maximize your revenue within a fixed budget.

## Usage Guide

### 1. Configure Your Property (Input)
Navigate to the **Input** cell at the very top of the notebook. Update the variables to match your current listing:

* **Location:** Set `user_state` to your property's full state name (e.g., `'New York'`).
* **Ratings:** Enter your current average star ratings (Cleanliness, Check-in, etc.).
* **Amenities:** Configure the status of each amenity using these codes:
    * `1`: **Already Owned** (You currently have this).
    * `0`: **Potential Upgrade** (You don't have it, but are willing to install it).
    * `2`: **Forbidden** (You don't have it and *cannot* or *do not want* to install it).
* **Budget:** Set `user_budget` to your maximum available investment in USD.

**Example:**
```python
user_state = 'California'
user_air_conditioning = 1  # Already have AC
user_pool = 2              # Cannot build a pool (Forbidden)
user_bbq_grill = 0         # Don't have a grill, but willing to buy one
user_budget = 5000         # Maximum budget
