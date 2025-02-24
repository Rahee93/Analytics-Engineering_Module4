# Analytics-Engineering_Module4

Questions
Question 1. Model resolution (1 point)

1. select * from dtc_zoomcamp_2025.raw_nyc_tripdata.ext_green_taxi
2. select * from dtc_zoomcamp_2025.my_nyc_tripdata.ext_green_taxi
3. select * from myproject.raw_nyc_tripdata.ext_green_taxi  ========> CORRECT ANSWER
4. select * from myproject.my_nyc_tripdata.ext_green_taxi
5. select * from dtc_zoomcamp_2025.raw_nyc_tripdata.green_taxi

Question 2. Change the query (1 point)

1. Add ORDER BY pickup_datetime DESC and LIMIT {{ var("days_back", 30) }}
2. Update the WHERE clause to pickup_datetime >= CURRENT_DATE - INTERVAL '{{ var("days_back", 30) }}' DAY
3. Update the WHERE clause to pickup_datetime >= CURRENT_DATE - INTERVAL '{{ env_var("DAYS_BACK", "30") }}' DAY
4. Update the WHERE clause to pickup_datetime >= CURRENT_DATE - INTERVAL '{{ var("days_back", env_var("DAYS_BACK", "30")) }}' DAY
5. Update the WHERE clause to pickup_datetime >= CURRENT_DATE - INTERVAL '{{ env_var("DAYS_BACK", var("days_back", "30")) }}' DAY    ========> CORRECT ANSWER
   
Question 3. Lineage (1 point)

1. dbt run
2. dbt run --select +models/core/dim_taxi_trips.sql+ --target prod
3. dbt run --select +models/core/fct_taxi_monthly_zone_revenue.sql
4. dbt run --select +models/core/
5. dbt run --select models/staging/+  ========> CORRECT ANSWER
   
Question 4. Macros and Jinja (1 point)

1. Setting a value for DBT_BIGQUERY_TARGET_DATASET env var is mandatory, or it'll fail to compile   ========> CORRECT ANSWER
2. Setting a value for DBT_BIGQUERY_STAGING_DATASET env var is mandatory, or it'll fail to compile
3. When using core, it materializes in the dataset defined in DBT_BIGQUERY_TARGET_DATASET   ========> CORRECT ANSWER
4. When using stg, it materializes in the dataset defined in DBT_BIGQUERY_STAGING_DATASET, or defaults to DBT_BIGQUERY_TARGET_DATASET   ========> CORRECT ANSWER
5. When using staging, it materializes in the dataset defined in DBT_BIGQUERY_STAGING_DATASET, or defaults to DBT_BIGQUERY_TARGET_DATASET    ========> CORRECT ANSWER
   
Question 5. Taxi Quarterly Revenue Growth (1 point)

1. green: {best: 2020/Q2, worst: 2020/Q1}, yellow: {best: 2020/Q2, worst: 2020/Q1}
2. green: {best: 2020/Q2, worst: 2020/Q1}, yellow: {best: 2020/Q3, worst: 2020/Q4}     ========> CORRECT ANSWER
3. green: {best: 2020/Q1, worst: 2020/Q2}, yellow: {best: 2020/Q2, worst: 2020/Q1}
4. green: {best: 2020/Q1, worst: 2020/Q2}, yellow: {best: 2020/Q1, worst: 2020/Q2}
5. green: {best: 2020/Q1, worst: 2020/Q2}, yellow: {best: 2020/Q3, worst: 2020/Q4}
   
Question 6. P97/P95/P90 Taxi Monthly Fare (1 point)

1. green: {p97: 55.0, p95: 45.0, p90: 26.5}, yellow: {p97: 52.0, p95: 37.0, p90: 25.5}   ========> CORRECT ANSWER
2. green: {p97: 55.0, p95: 45.0, p90: 26.5}, yellow: {p97: 31.5, p95: 25.5, p90: 19.0}
3. green: {p97: 40.0, p95: 33.0, p90: 24.5}, yellow: {p97: 52.0, p95: 37.0, p90: 25.5}
4. green: {p97: 40.0, p95: 33.0, p90: 24.5}, yellow: {p97: 31.5, p95: 25.5, p90: 19.0}
5. green: {p97: 55.0, p95: 45.0, p90: 26.5}, yellow: {p97: 52.0, p95: 25.5, p90: 19.0}
   
Question 7. Top #Nth longest P90 travel time Location for FHV (2 points)

1. LaGuardia Airport, Chinatown, Garment District    ========> CORRECT ANSWER
2. LaGuardia Airport, Park Slope, Clinton East
3. LaGuardia Airport, Saint Albans, Howard Beach
4. LaGuardia Airport, Rosedale, Bath Beach
5. LaGuardia Airport, Yorkville East, Greenpoint

   
