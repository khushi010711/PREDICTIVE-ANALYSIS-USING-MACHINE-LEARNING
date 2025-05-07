# PREDICTIVE-ANALYSIS-USING-MACHINE-LEARNING

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*:KHUSHI SHAH

*INTERN ID*:CT04DL131

*DOMAIN*:DATA ANALYTICS

*DURATION*:4 WEEKS

*MENTOR*:NEELA SANTHOSH 

## DESCRIPTION


This Python script builds an interactive web dashboard using the Dash framework to simulate and visualize website user activity data. The dashboard provides a dynamic and intuitive interface to analyze user behavior across different pages of a fictional website, enabling the exploration of engagement metrics such as session duration, frequency, and page-wise distribution.

#### 1. **Library Imports and Data Simulation**

The script starts by importing necessary libraries:

* `dash`, `dcc`, and `html` from Dash for web interface creation.
* `pandas` and `numpy` for data manipulation and simulation.
* `plotly.express` for rich interactive visualizations.
* `datetime` for generating realistic timestamps.

Instead of relying on an external data source, the script simulates a dataset representing user interactions. It defines 100,000 random session records with the following structure:

* `user_id`: Randomly selected from a pool of 50 users (e.g., "user\_1" to "user\_50").
* `page`: Randomly selected from a list of common website pages like 'home', 'products', and 'checkout'.
* `duration`: Generated from an exponential distribution to simulate session time in seconds.
* `timestamp`: Simulated across a range of dates beginning January 1, 2024, by adding random seconds to a base datetime.

This synthetic dataset mimics real-world web usage patterns and serves as the foundation for the dashboard's interactivity.

#### 2. **Dash Application Setup**

A Dash app instance is initialized with a title. The layout of the dashboard is organized using Dash's HTML and core component modules:

* A main heading titled "Interactive User Activity Dashboard".
* A dropdown component (`dcc.Dropdown`) that lets the user select a specific user ID from the dataset.
* Two graphs aligned side-by-side using a flexible box layout:

  * A bar chart of total time spent on each page by all users.
  * A bar chart showing the average session duration per page for the selected user.
* A third graph placed below, which displays a histogram of session durations across all users.

This layout ensures a clean and responsive interface, making it easy for users to draw insights from multiple perspectives.

#### 3. **Callback for Interactivity**

The core logic of the interactivity lies in the Dash callback function, which updates all three graphs whenever a new user is selected from the dropdown:

* **Total Time per Page (`fig1`)**: Aggregates duration across all users, showing which pages are most engaged.
* **Average Session Duration by Page for Selected User (`fig2`)**: Filters the dataset for the selected user and calculates the mean duration spent on each page, giving a personalized view of behavior.
* **Session Duration Distribution (`fig3`)**: A histogram of session durations for all users, providing insights into session length trends and outliers.

These charts are dynamically generated using Plotly Express, which ensures interactive capabilities such as tooltips and zooming.

#### 4. **Execution**

The final block checks if the script is being run as the main module and starts the Dash server with `debug=True`, enabling hot reloading during development.

## OUTPUT



