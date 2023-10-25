# Airline Passenger Booking Analysis

This project focuses on interacting with an Airline Passenger Booking database to perform various data analyses. It uses Python, SQL Server, pandas, and visualization libraries to analyze and present the booking data.

## Table of Contents

- [Installation](#installation)
- [Database Structure](#database-structure)
- [Usage](#usage)
- [Scripts](#scripts)
- [Visualizations](#visualizations)

---

## Installation

To run the code, you will need to install the following:

- Python 3.x
- SQL Server
- pandas
- matplotlib
- seaborn
- pyodbc
- SQLAlchemy

You can install the Python libraries using pip:

\```bash
pip install pandas matplotlib seaborn pyodbc SQLAlchemy
\```

## Database Structure

The database (`AirlinePassengerBookingDataBase3`) contains multiple tables:

- `PassengerBooking`
- `Passenger`
- `Flight`
- `Booking`

These tables are created and populated by the Python script, and they store different types of booking information.

---

## Usage

1. Ensure that SQL Server is running and accessible.
2. Run the Python scripts to create the tables and populate them with data.
3. Run the Python scripts for data visualization.

## Scripts

- `CreateTables.py`: This script creates the required tables in the SQL database.
- `DataCleaning.py`: Reads the CSV file, performs data cleaning, and populates the SQL tables.
- `DataVisualization.py`: Fetches data from the SQL database and creates visualizations.

### Create Tables

This section is responsible for creating the `PassengerBooking` table in SQL Server.

\```python
# Database connection parameters
server = 'JOEGAO\\MSSQLSERVER01'
database = 'AirlinePassengerBookingDataBase5'
# ... (code for table creation)
\```

### Data Cleaning and Insertion

This section reads a CSV file and cleans the data before inserting it into the SQL tables.

\```python
df = pd.read_csv(r'C:\Path\To\CSV\File', low_memory=False)
# ... (code for data cleaning)
\```

### Data Visualization

We use pandas along with matplotlib and seaborn for data visualization. Here are some examples:

#### Top 15 Booking Origins by Count

\```python
# ... (SQL query to get top 15 booking origins)
sns.barplot(x='count', y='booking_origin', data=booking_data)
\```

#### Distribution of Flight Hours by Class

\```python
# ... (SQL query to get flight hours by class)
sns.boxplot(x='flight_hour', y='Class', data=filtered_flight_df)
\```

#### In-flight Meals Preference by Group Size

\```python
# ... (SQL query to get in-flight meals preferences)
pivot_data.plot(kind='bar', stacked=True)
\```

## Visualizations

The scripts produce the following visualizations:

1. Bar chart of the top 15 booking origins.
2. Box plot of the distribution of flight hours by class.
3. Stacked bar chart showing in-flight meals preferences by group size.
