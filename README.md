📌 Project Overview
This project is designed to gain insights into Data Engineering job postings on LinkedIn. Using the LinkedIn Jobs API from RapidAPI, the project extracts job posting data, transforms it into a clean tabular format, and loads it into a SQL Server database. The database is then connected to Power BI to create an interactive dashboard that visualizes hiring trends and requirements for data engineers.
The primary goal is to analyze job market demand for data engineers within the last 7 days and answer questions such as:
•	Total number of Data Engineering postings in the past week
•	Number of remote positions available
•	Number of full-time postings
•	Distribution of employment types (%)
•	Number of job postings by employer
•	Number of job postings by state
•	Top skills required for Data Engineering roles
This project demonstrates a full ETL (Extract, Transform, Load) pipeline with insights delivered through Power BI dashboards.
________________________________________
🛠 Tech Stack
•	Python → for API requests & data extraction
•	Pandas → for data cleaning and transformation
•	SQL Server → for structured data storage
•	Power BI → for visualization and dashboard reporting
________________________________________
🔄 ETL Workflow
1. Extract
•	Retrieve Data Engineering job postings from the LinkedIn Jobs API (RapidAPI).
•	Pull job title, company name, location, employment type, posting date, and skills.
2. Transform
•	Convert API response into a tabular format using Pandas.
•	Clean and standardize fields (dates, employer names, job locations, employment types).
•	Derive features such as remote vs. on-site, employment type categories, and skill frequency counts.
3. Load
•	Insert transformed data into SQL Server database tables.
•	Store both raw data and cleaned data for reproducibility.
4. Visualize
•	Connect Power BI to the SQL Server database.
•	Build interactive dashboards to show:
o	Total postings (7 days)
o	Remote vs. onsite jobs
o	Full-time vs. part-time vs. contract distributions
o	Top employers hiring data engineers
o	Job postings by state
o	Top technical skills required

⚡ This way, recruiters, hiring managers, or aspiring data engineers can quickly understand where the demand is highest, which companies are hiring, and what skills are most valuable in the current job market.

🚀 How to Run
1. Clone the Repository
git clone https://github.com/your-username/data-engineering-job-postings.git
cd data-engineering-job-postings
________________________________________
2. Set Up Python Environment
Make sure you have Python 3.9+ installed. Then install dependencies:
pip install -r requirements.txt
________________________________________
3. Configure Environment Variables
This project requires a RapidAPI key and SQL Server connection details.
1.	Create a .env file in the root directory:
2.	RAPIDAPI_KEY=your_api_key_here
3.	SQL_SERVER=your_server_name
4.	SQL_DATABASE=your_database_name
5.	SQL_USERNAME=your_username
6.	SQL_PASSWORD=your_password
7.	These values are loaded inside the Python script to keep credentials secure.
⚠️ Never commit .env files to GitHub.
________________________________________
4. Run the ETL Script
Execute the Python script to extract, transform, and load the data into SQL Server:
Python Script.ipnyb
•	The script will fetch Data Engineering postings from LinkedIn’s API (last 7 days).
•	It will clean and transform the dataset using Pandas.
•	Finally, it will insert the cleaned data into your SQL Server database.
________________________________________
5. Verify Data in SQL Server
•	Open SQL Server Management Studio (SSMS).
•	Run queries against your database to confirm that the tables have been populated, for example:
SELECT TOP 10 * FROM LinkedInJobs;
________________________________________
6. Open the Power BI Dashboard
1.	Open powerbi/linkedin_jobs_dashboard.pbix in Power BI Desktop.
2.	Update the database connection to match your SQL Server credentials.
3.	Refresh the data to see the latest job postings.
________________________________________
7. Explore the Insights
The Power BI dashboard includes:
•	Total postings in the last 7 days
•	Remote vs. onsite jobs
•	Full-time vs. contract distribution
•	Job postings by employer
•	Job postings by U.S. state
•	Top technical skills required





