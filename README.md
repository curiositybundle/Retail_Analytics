Retail Intelligence Optimization (RIO) Dashboard

🚀 Overview

The Retail Intelligence Optimization (RIO) Dashboard is a data analytics application built with Streamlit and Python's scientific stack (Pandas, Scikit-learn, Matplotlib). It executes a full end-to-end retail analysis pipeline, including customer segmentation (using PCA/K-Means), multi-touch attribution modeling, and product/funnel performance analysis.

The entire application logic is contained within app.py.

⚙️ Requirements & Installation

This project relies on the Conda package manager for reliable installation of complex scientific dependencies on Windows/macOS/Linux.

Prerequisites

Miniconda/Anaconda: Install Miniconda (recommended lightweight option).

GitHub Repository: The code is hosted in the curiositybundle/Retail_Analytics repository.

Data Files (7 CSVs): You must have all 7 required CSV files ready for upload in the dashboard interface.

Local Setup (Using Conda)

Follow these steps exactly in your Anaconda/Miniconda Prompt:

Navigate to the Project Folder:

cd /path/to/your/Retail_Analytics


Create and Activate Environment: Create a new environment named rio_env.

conda create -n rio_env python=3.10
conda activate rio_env


Install Dependencies: Install all required packages using the provided requirements.txt.

pip install -r requirements.txt


Run the Application:

streamlit run app.py


Your application will launch in your browser at http://localhost:8501.

📈 How to Use the Dashboard

Launch the App: Open the application (either locally or via Streamlit Cloud).

Upload Data: In the "1. Data Input" section, click the file uploader and upload all 7 required CSV files simultaneously:

interactions.csv

journeys.csv

orders.csv

products_master.csv

reviews.csv

customers.csv

customer_profiles_extended.csv

Run Analysis: Click the "🚀 Run RIO Analysis" button.

Review Results: The dashboard will update with the following sections (optimized for speed by running the heavy clustering analysis on a randomized sample of 10,000 customers):

Customer Segmentation: View the cluster descriptive summaries and a Radar Plot comparing key behavioral metrics (Recency, Frequency, Monetary).

Funnel Analysis: Analyze overall drop-off rates, highlighting the biggest points of abandonment (e.g., checkout).

Attribution Strategy: Compare marketing channel performance using models like First Touch, Last Touch, Linear, and a simplified Markov model.

Product Efficiency: Review conversion rates by category, channel, and device, including the Product Quality Metrics derived from the reviews.csv data.

☁️ Cloud Deployment (Streamlit Community Cloud)

Since this project is hosted on GitHub and includes the requirements.txt file, deployment is done in just a few clicks:

Go to share.streamlit.io and log in.

Click New App.

Select the curiositybundle/Retail_Analytics repository.

Set the Main file path to app.py.

Click Deploy. The app will be live and shareable in minutes.

End of README