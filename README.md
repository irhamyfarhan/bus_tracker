# GTFS Realtime Data Pipeline

## Overview
An ETL pipeline that processes GTFS Realtime transit data from the [Malaysia Government Open Data API](https://developer.data.gov.my/realtime-api/gtfs-realtime). It extracts, transforms, and loads data into a PostgreSQL database for analysis and visualization.

## What is GTFS Realtime Data?
GTFS Realtime (General Transit Feed Specification) is a standardized format for transmitting real-time public transit data, providing live updates on:
- **Vehicle Positions**: Current locations of buses, trains, or other transit vehicles.
- **Trip Updates**: Delays, cancellations, and route changes.
- **Service Alerts**: Notifications about disruptions, detours, or important transit announcements.

## Source of GTFS Realtime Data
The GTFS Realtime API incorporates data from various transport agencies in Malaysia. Currently, the following agencies contribute their transit data:
- **myBAS Johor Bahru**: A bus service operator in Johor Bahru, Malaysia, providing bus transportation on 19 routes across 5 corridors, including Kota Tinggi, Masai, Kulai, Gelang Patah, and Pontian.
- **KTMB (Keretapi Tanah Melayu Berhad)**: A railway operator providing train services across the country.
- **Prasarana**: A public transport operator responsible for managing various modes of transportation, including LRT (Light Rail Transit), MRT (Mass Rapid Transit), monorail, and bus services.

## Architecture
- **Apache Airflow**: Orchestrates and schedules the ETL process.
- **PostgreSQL (Docker)**: Stores structured transit data.
- **Python (requests, pandas)**: Handles data extraction, transformation, and loading.
- **Power BI**: Provides interactive dashboards and insights.

- ![image](https://github.com/user-attachments/assets/f7aa33ca-875e-43c0-a44c-213c90fdf5ca)


## Key Features
- **Automated Data Processing**: Fetches GTFS Realtime data at scheduled intervals.
- **Scalability & Portability**: Uses Docker for easy deployment.
- **Seamless Visualization**: Enables transit analysis via Power BI dashboards.
- **Extensibility**: Easily integrates with other databases and visualization tools.

## Challenges Faced
- **Dependency Issues**: Conflicts between Airflow and package versions required manual resolution.
- **Data Inconsistencies**: Realtime data varied in structure, requiring additional transformations.
- **Docker Networking**: Initial connectivity issues between Airflow, PostgreSQL, and the host machine.
- **Airflow Configuration**: Required fine-tuning for scheduler stability and DAG performance.

## Future Enhancements
- Implement data validation and quality checks.
- Develop a real-time dashboard.
- Optimize database performance.

## License
MIT License

## Author
[Irhamy Farhan](https://github.com/irhamyfarhan)

