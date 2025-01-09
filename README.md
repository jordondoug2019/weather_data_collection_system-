# Weather_Data_Collection_System

### **Weather Data Collection System- Day 1 \#30DayDevOpsChallenege**

---

### **A. PURPOSE**

To build a weather data collection system using AWS S3 and Openweather API. This project demonstrates External API Integration (OpenWeather API), Cloud Storage (AWs S3), Version Control (Git), Python development, and error handling. The Collection System supports multi-city tracking, automatically stores weather data in AWS S3, and timestamps all data for historical tracking. 

---

### **B. STEPS**

Below are the steps taken and their importance:

1. Git Clone Repository  
   * Clone repository for version control  
2. Install dependencies  
   * Installed boto3, python-dotenv, and requests.   
     * Boto3 is an Aws SDK for python.   
       1. For this use case, it simplified the process of integrating AWS services (creating s3 buckets) into your python Application.  
     *  Python-dotenv is installed to help load environment variables from a .env file.   
       1. In this project, it was used to retrieve the API Key and S3 bucket name.   
     * Requests is a python library for making HTTP requests to APIs.   
       1. It was used to fetch data from Openweather API.  
3. Configure environment variables (.env)  
   * Add Openweather API Key and name of S3 Bucket name  
4. Install AWS Cli  
   * Installed AWS Cli to manage aws services from the Command Line.   
5. Configure AWS  
   * Set up IAM user and permissions   
6. Install Python locally   
7. Run Application  
   * python weatherdashboard.py 

---

### **C. SYSTEM DESIGN DIAGRAM**

![Weather-Collections-Systems](https://github.com/user-attachments/assets/05e0ab25-1787-4dbb-b10c-bc0cdb0647f7)

---

### **D. ISSUES/TROUBLESHOOTING**

1. Ran into Pip issue w/Boto3   
   * **Error**: “pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.”  
   * **Troubleshoot:** pip was encountering conflicting versions of dependencies between installed packages.   
     1. Upgrade boto3 to compatible version for pip   
2. Issues w/AWS Cli installation   
   * **Error:** “ Exception: Traceback (most recent call last): File "/usr/local/aws/lib/python3.11/site-packages/pip/\_internal/cli/base\_command.py", line 180, in exc\_logging\_wrapper”  
   * **Troubleshoot:** Python was missing. Installed latest version of Python.  
3. Error creating S3 Bucket  
   * **Error: “**Creating bucket None Error creating bucket: expected string or bytes-like object, got 'NoneType'”  
   * **Troubleshoot:** I added a print statement to check if the bucket was being called from .env  
     1. Moved .env file to src folder   
4. S3 Bucket was not being created   
   * **Error:** “Error creating bucket: An error occurred (AccessDenied) when calling the CreateBucket operation: User: arn:aws:iam::140023377824:user/jdouglas is not authorized to perform: s3:CreateBucket on resource: "arn:aws:s3:::weather-dashboard-01" because no identity-based policy allows the s3:CreateBucket action”  
   * **Troubleshoot:** Updated permissions for IAM User 

---

### **E. OPTIMIZATION**

1. Set up CI/CD Pipeline   
2. Add Hourly Forecast   
3. Add Daily/weekly forecast   
4. Add data visualization with Maps  
5. Include more cities

---

### **F.  What I learned**

I learned

*  IAM User creation and policy management  
* AWS S3 bucket creation and management   
* What Boto3 is and how to use   
* API Integration 
