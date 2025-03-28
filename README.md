# Weather ETL Pipeline Using Airflow

## Overview
This project implements an **Extract, Transform, Load (ETL) pipeline** for weather data using **Apache Airflow with Astronomer (Astro Airflow)**. The pipeline extracts real-time weather data, processes it, and loads it into a structured database for analysis.

The workflow is containerized using **Docker**, managed through **Astro CLI**, and includes **PostgreSQL (via DBeaver) as the database** for storing processed data.

## Features
- **Automated Data Extraction**: Fetches weather data from an API.
- **Data Transformation**: Cleans and formats the data for analysis.
- **Airflow Orchestration**: Schedules and monitors the workflow.
- **PostgreSQL Storage**: Stores transformed data for further querying.
- **Containerized Deployment**: Runs in Docker for portability.

## Architecture
1. **Extract**: Airflow fetches raw weather data from an external API.
2. **Transform**: Data is cleaned and formatted within an Airflow task.
3. **Load**: Transformed data is inserted into PostgreSQL.
4. **Monitoring**: Airflow DAGs track and visualize execution.

## Installation & Setup
### Prerequisites
- Docker
- Astro CLI
- DBeaver (or any SQL client for PostgreSQL)

### Steps
1. **Clone the Repository**:
   ```sh
   git clone <repository-link>
   cd weather-etl-pipeline
   ```
2. **Start Astro Airflow Environment**:
   ```sh
   astro dev start
   ```
3. **Access Airflow UI**:
   - Navigate to `http://localhost:8080` and check DAG status.
4. **Run DAG Manually**:
   - Trigger the DAG from the Airflow UI to execute the pipeline.
5. **Connect to PostgreSQL via DBeaver**:
   - Use `localhost:5432` and the correct credentials to access the weather data.


1.**Airflow Graph View** - Visualizing task dependencies.

<img width="1276" alt="airflow_graph" src="https://github.com/user-attachments/assets/c0393120-55c4-4245-96a6-67c32da3b593" />


2. **DBeaver** - Verifying stored weather data.
   
<img width="1275" alt="Dbeaver" src="https://github.com/user-attachments/assets/f1e08014-a534-4956-836a-c0b97bf6a36a" />


3. **Airflow DAG Execution** - Successfully running DAG.
   
<img width="1275" alt="Airflow_run" src="https://github.com/user-attachments/assets/24b62a98-48f0-4262-bcc7-2de44926e963" />



4. **Docker Containers** - Running Astro Airflow components.
   
 <img width="1274" alt="Docker_container" src="https://github.com/user-attachments/assets/6fd4cac7-5682-4d12-85f4-b161f32cc0f2" />




## Future Improvements
- Add real-time data processing with Kafka.
- Store data in AWS S3 for scalability.
- Implement data validation checks before loading.



