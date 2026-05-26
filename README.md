Starlink API Testing Project

A comprehensive API testing project for the SpaceX Starlink API using Postman and Newman.
This project validates API responses, response headers, performance, schema structure, and data integrity through automated test scripts.

📌 Project Overview

This project tests the Starlink satellite API endpoints from the SpaceX public API.

The collection includes:

✅ Positive API test cases
✅ Response validation
✅ Header validation
✅ Performance testing
✅ Schema & datatype validation
✅ Dynamic environment variables
✅ Automated Newman HTML reporting

The tests were executed using Newman CLI, generating a detailed dashboard report showing:

9 Total Requests
300 Assertions
11 Failed Tests
0 Skipped Tests

Dashboard preview available in the generated report image.

🛠️ Tech Stack
Postman
Newman
Node.js
HTML Reporter
JavaScript (Postman Scripts)
📂 Project Structure
├── Starlink.postman_collection.json
├── Starlink.postman_environment.json
├── Postman_Test_Report_from_JSON.pdf
├── API report.jpg
└── README.md
🔗 API Used

SpaceX Starlink API:

https://api.spacexdata.com/v4/starlink

Environment configuration contains API base URLs and dynamic variables.

✅ Test Scenarios Covered
📍 GET All Starlink Satellites
Status code validation
Response time validation
Response size validation
JSON structure validation
Headers validation
Data type validation
Object property validation
Satellite orbital parameter validation
Dynamic environment variable creation

Example validations from collection:

📍 GET Single Starlink Satellite

Validated:

Satellite ID
Object name
Orbital values
Country code
Launch date
Height, latitude, longitude
Velocity values
TLE data
Headers and response structure

Report details available in PDF report.

🧪 Assertions Implemented

Some major assertions include:

pm.response.to.have.status(200);

pm.expect(pm.response.responseTime).to.be.below(600);

pm.expect(item).to.have.property("spaceTrack");

pm.expect(targetObject.spaceTrack.OBJECT_TYPE)
.to.equal("PAYLOAD");

Collection scripts include extensive validations for:

Headers
Body fields
Numerical values
Null checks
Array validation
Dynamic IDs

📊 Newman Report Summary
Metric	Count
Total Requests	9
Total Assertions	300
Failed Tests	11
Skipped Tests	0

The generated Newman dashboard visually represents execution statistics and failures.

▶️ How to Run the Project
1️⃣ Install Newman
npm install -g newman
2️⃣ Install HTML Reporter
npm install -g newman-reporter-htmlextra
3️⃣ Run Collection
newman run Starlink.postman_collection.json \
-e Starlink.postman_environment.json \
-r cli,htmlextra
📈 Features
Dynamic environment handling
Random satellite ID generation
Automated validations
Performance benchmarking
Detailed HTML reporting
Reusable test scripts
Real-world API testing workflow
📸 Report Preview

Add your report screenshot here:

![Newman Dashboard](API%20report.jpg)
🎯 Learning Outcomes

Through this project, I gained hands-on experience in:

API automation testing
Postman scripting
Newman CLI execution
JSON schema validation
Response assertions
API performance testing
Automated report generation
