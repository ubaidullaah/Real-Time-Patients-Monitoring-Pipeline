# Patient Vital Monitoring and Analytics Pipeline

This project implements a **real-time data pipeline** using **Apache Beam** and **Google Cloud Dataflow** to process patient vital data. The pipeline reads streaming data from **Google Cloud Pub/Sub**, processes it through multiple stages (Bronze, Silver, and Gold layers), and stores the output in **Google Cloud Storage (GCS)** and **BigQuery** for analytics and reporting.

## Key Features:
- **Real-time Data Streaming**: Uses **Apache Beam** with **Google Cloud Dataflow** to process data in real-time.
- **Data Transformation**: Cleans, validates, and enriches patient vital data with health risk metrics.
- **Cloud Integration**: Data is processed and stored using **Google Cloud Pub/Sub**, **Google Cloud Storage (GCS)**, and **BigQuery**.
- **Scalable and Flexible**: The pipeline is scalable, allowing you to configure the number of workers and resource allocation as per the needs of the job.
- **Error Handling**: The pipeline includes robust error handling and logging for easy debugging and monitoring.

## Technologies Used:
- **Apache Beam** for building the data pipeline.
- **Google Cloud Dataflow** for running the pipeline in the cloud.
- **Google Cloud Pub/Sub** for streaming data ingestion.
- **Google Cloud Storage (GCS)** for storing raw and cleaned data.
- **Google BigQuery** for analytics and data aggregation.
- **Python** for pipeline development and scripting.

## Setup Instructions:
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/patient-vital-monitoring.git

Install the required dependencies:

pip install -r requirements.txt


Configure environment variables using a .env file:
Create a .env file and add the following variables with your own GCP project details:

GCP_PROJECT=your-gcp-project-id
PUBSUB_SUBSCRIPTION=projects/your-gcp-project-id/subscriptions/your-subscription-name
BRONZE_PATH=gs://your-bucket/bronze/
SILVER_PATH=gs://your-bucket/silver/
BIGQUERY_TABLE=your-gcp-project-id:your-dataset.your-table
TEMP_LOCATION=gs://your-bucket/temp/
STAGING_LOCATION=gs://your-bucket/staging/
REGION=us-central1


Run the pipeline:

python streaming_medallion_pipeline.py --runner DataflowRunner --project $GCP_PROJECT --region $REGION --staging_location $STAGING_LOCATION --temp_location $TEMP_LOCATION --streaming

Contribution:

Contributions are welcome! Please fork the repository and create a pull request with your changes. Be sure to follow the coding conventions and test thoroughly before submitting.

License:

This project is licensed under the MIT License.


### How to Use:
1. Copy and paste the above `README.md` into your GitHub repository's `README.md` file.
2. Replace the placeholders like `your-gcp-project-id`, `your-subscription-name`, `your-bucket`, etc., with your actual values.
3. The instructions provided in the README will guide users on how to set up and run your pipeline.

This is a fully functional **README** for your GitHub project. Let me know if you need any further changes!
