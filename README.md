# Revenue-Insights-Dashboard-HospitalityDomain
**PROJECT TITLE**

Revenue-Insights-Dashboard-HospitalityDomain

**📌PURPOSE**

The Revenue Insights Dashboard is a Power BI project designed to help a hospitality chain analyze and monitor key revenue metrics. The dashboard provides a consolidated view of property performance, booking trends, occupancy, revenue drivers, and other KPIs that support data-driven decision-making.

**🗂️ DATA SOURCES**

The Dashboard uses the following databases:

|Table|Description|
|-----|-----------|
|dim_date|Date, Month-Year, Week no, day_type|
|dim_hotels|Category, city, property_id, property_name|
|dim_rooms|room_class, room_id|
|fact_aggregated_bookings|property_id, check_in_date, room_category, successful_bookings, capacity|
|fact_bookings|property_id, booking_date, check_in_date, check_out_date, no_guests, room_category, booking_platform, ratings_given, booking_status, revenue_generated, revenue_realized|

**🛠️TECH STACK**

The dashboard was built using following Tools and Technologies:
**Power BI Desktop** – Dashboard development & visualization

**Power Query** – Data cleaning & transformation

**DAX (Data Analysis Expressions)** – Calculated measures

**Excel/CSV** – Raw data sources

**🧩DASHBOARD SECTIONS**

**1. Executive Summary**

This section provides the core KPIs such as:

* Revenue

* ADR (Average Daily Rate)

* DSRN (Daily Sellable Room Nights)

* Occupancy %

* RevPAR

* Realisation %

**2. Revenue by Category**

A donut chart highlights the contribution of Luxury and Business room categories to total revenue.

**3. Trends by Key Metrics**

A weekly performance line chart that tracks:

* Occupancy %

* ADR

* RevPAR

**4. Day-Type Performance (Weekday vs Weekend)**

A comparative table showing:

* ADR

* Occupancy %

* RevPAR

Realisation %

**5. Property-Level Performance Table**

A detailed table listing each property with:

* Revenue

* RevPAR

* Occupancy %

* ADR

* DSRN / DBRN

* Realisation %

* Cancellation %

* Average Rating

This helps in evaluating the property performance across cities and identifies top and low performers.

**6. Realisation % and ADR by Booking Platform:**

A bar and line combo chart that compares Realisation % and ADR across booking platforms such as:

* Journey

* Inspire

* MakeYourTrip

* Direct Offline

* Direct Online

* Others

* Tripser

This section helps identify which channels provide higher revenue realisation and better ADR.

**7. Filter Panel**

This panel includes slicers for:

* Month

* Week Number

**🔍KEY INSIGHTS AND FINDINGS**

* Weekend occupancy is higher than weekdays.

* ADR remains constant regardless of occupancy changes, indicating that pricing is not being adjusted based on demand.

* The consistent pricing pattern highlights a flat pricing strategy, where room rates stay the same regardless of market conditions or demand levels.

* Occupancy levels show a direct relationship with average guest ratings, as hotels with lower ratings consistently experience lower occupancy.

* Realisation and ADR by booking category show that Direct Offline bookings outperform Direct Online bookings made through the hotel’s website.

**🧮SAMPLE DAX MEASURES**

ADR = DIVIDE([Revenue],[Total bookings],0)

Total Successful bookings = SUM(fact_aggregated_bookings[successful_bookings])

Total Capacity = sum(fact_aggregated_bookings[capacity])

Occupancy% = DIVIDE([Total Successful bookings], [Total Capacity],0)

RevPAR = DIVIDE([Revenue],[Total Capacity])

Revenue = sum(fact_bookings[revenue_realized])

