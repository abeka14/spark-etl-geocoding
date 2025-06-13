# spark-etl-geocoding

This project uses Apache Spark for data cleansing, enrichment, and geospatial data integration.


The goal of this ETL pipeline is to:

- Clean restaurant data by identifying and replacing missing latitude/longitude using OpenCage Geocoding API.
- Generate a 4-character geohash for each valid location using the `geohash` library.
- Join the restaurant and weather datasets using the geohash, ensuring no data duplication (idempotency preserved).
- Store the final enriched dataset in **Parquet format**, partitioned appropriately in the **local file system**.

---

## ⚙️ Tech Stack

- Apache Spark (local setup)
- Python (PySpark)
- OpenCage Geocoding API
- geohash library (`python-geohash`)
- Parquet file format
