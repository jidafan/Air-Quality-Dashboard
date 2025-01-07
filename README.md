# Air Quality Dashboard

This project analyzes the air quality around the GTA and surrounding areas. A data pipeline is created using Python which extracts and transforms data. The final product is a dash dashboard that provides a map of the sensor locations and charts of the air quality.

## Project Files

| Files    | Description       | 
| ------------- |:---------------------| 
| `notebooks/`     | Exploring data and performing data quality checks  |
| `sql/`     | SQL scripts for extracting and transforming data utilizing the DuckDB package |   
| `pipeline/` | CLI applications for extracting, transforming, and managing databases.                     |
| `dashboard/`     | Code for the air quality dashboard using Plotly Dash  |
| `locations.json` | A list of the air quality sensor locations                      |
| `requirements.txt` | List of Python libraries                    |

## How to Run Project
1. Set up Python Environment

   * Create a virtual environment
     ```
      $ python -m venv .venv
     ```

  * Activate the environment
    - Windows: `$ . .venv/Scripts/Activate `
    - Linux: `$ . .venv/bin/activate `

  * Install dependencies
    ```
    $ pip install -r requirements.txt
    ```

2. Initialize Database
  
* Navigate to the pipeline directory
  ```
  $ cd pipeline
  ```
* Create the database using the CLI interface
  ```
  $ python database_manager.py --create
  ```

3. Extract Database
   
  * Run the extraction CLI
  ```
  $ python extraction.py [required arguments]
  ```

4. Transform Data
   
  * Run the transformation CLI to create views in the presentation schema
  ```
  $ python transformation.py
  ```

5. Run Dashboard
   
  * Navigate to the dashboard directory
  ```
  $ cd dashboard
  ```
  * Run the app
  ```
  $ python app.py
  ```

6. Access Results
   
  * Dashboard will be on web browser
