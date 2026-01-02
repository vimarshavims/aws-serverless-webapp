# AWS Serverless Student Management System

This project demonstrates a serverless application deployed on AWS. It allows for managing student data (inserting and retrieving) using AWS Lambda, DynamoDB, and API Gateway.

## Project Structure

- **`scripts.js`**: Frontend logic to interact with the API Gateway endpoints. Handles inserting student data and fetching the list of students.
- **`insertStudentData.py`**: AWS Lambda function code to insert a new student record into DynamoDB.
- **`getStudents.py`**: AWS Lambda function code to retrieve all student records from DynamoDB.
- **`screenshots/`**: Contains visual documentation/screenshots of the project setup and deployment.

## Prerequisites

- **AWS Account**: Access to AWS console.
- **Python 3.x**: For local testing or packaging Lambda functions.
- **Breswer**: A modern web browser to run the application.

## Setup & Deployment

1.  **DynamoDB**: Create a table named `studentData` with `studentid` as the Partition Key.
2.  **Lambda**:
    -   Create a function for inserting data and paste the code from `insertStudentData.py`.
    -   Create a function for getting data and paste the code from `getStudents.py`.
    -   Grant the Lambda functions appropriate IAM permissions to access DynamoDB.
3.  **API Gateway**:
    -   Create a REST API.
    -   Create generic resources and methods (POST for insert, GET for retrieve).
    -   Enable CORS.
    -   Deploy the API and obtain the **Invoke URL**.
4.  **Frontend**:
    -   Update the `API_ENDPOINT` variable in `scripts.js` with your API Gateway Invoke URL.
    -   Open `index.html` (Note: Ensure `index.html` is present in the root directory) in your browser.

## Technologies Used

-   AWS Lambda
-   Amazon DynamoDB
-   Amazon API Gateway
-   HTML/CSS/JavaScript (jQuery)
-   Python (Boto3)
