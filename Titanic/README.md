# Titanic Power BI Dashboard

I created this interactive Power BI dashboard using the Titanic dataset. Both the Power BI `.pbix` file and the `.pdf` version of the dashboard are available in this repository.

## Dashboard Overview

At the top of the dashboard, there are two slicers:

- **Gender** – allows users to filter the dashboard by gender.
- **Passenger Status** – allows users to select between **Deceased** and **Survived** passengers.

### KPI Cards

The dashboard includes four cards:

- **Sum Of Fare** – shows the total ticket fare.
- **Total Number Of Passengers** – shows the total number of passengers.
- **Number Of Deaths** – shows the total number of passengers who did not survive. This measure was created using DAX.
- **Number Of Survivors** – shows the total number of surviving passengers.

### Top 7 Passengers With Highest Fare

The first column chart shows:

- **X-axis:** Passenger Full Name
- **Y-axis:** Total Fare
- **Legend:** Passenger Status

A DAX calculated column was created to display passenger status as **Deceased** for passengers with a value of `0` in the `Survived` column and **Survived** for passengers with a value of `1`.

Since the passenger names have high cardinality, a filter was applied to display only the **Top 7 passengers by fare**. Among these seven passengers, **5 survived and 2 were deceased**.

### Passengers by Class and Gender

The next bar chart shows the number of passengers in each passenger class, broken down by gender.

For better readability, I created a DAX column for `Pclass` to display the values as **Class 1**, **Class 2**, and **Class 3** instead of the original values `1`, `2`, and `3`.

The analysis shows that **Class 3 had the highest number of passengers**, with:

- **347 male passengers**
- **144 female passengers**
- **491 passengers in total**

### Interactive Matrix

The next visual is an interactive matrix. Its columns can be changed using the bookmarks placed next to the matrix.

The rows represent **age groups**, which were created using DAX. The available bookmarks are:

- **Gender**
- **Passenger Status**
- **Passenger Class**
- **Embarkation Port**

The matrix shows the **total fare for each age group** based on the selected category. This allows for quick and easy analysis of the data from different perspectives.

### Survivors and Deceased by Age Group

The next visual is a **pie chart** showing the number of deceased passengers across different age groups. Both the age groups and the deceased passenger count were created using DAX.

The final visual is a **donut chart** showing the number of surviving passengers across different age groups.

## Files

- `.pbix` – Power BI dashboard file
- `.pdf` – PDF version of the dashboard

Thank you for taking the time to view this project.
