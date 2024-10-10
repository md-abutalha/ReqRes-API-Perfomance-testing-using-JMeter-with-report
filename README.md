# ReqRes-API-Performance-Testing-Using-JMeter-with-Report

## Overview
This project involves performance testing of the [reqRes](https://reqres.in/) API using Apache JMeter. The objective of the test was to evaluate the performance and reliability of the API under load, specifically focusing on the `POST`, `GET`, `PUT`, and `DELETE` request endpoints for creating, retrieving, updating, and deleting users. The report was generated using JMeter's command-line mode and visualized through HTML reports.

## Tools Used
- **JMeter**: For performance and load testing.
- **Newman**: For command-line reporting and execution.
- **HTML Report**: Generated via JMeter's reporting dashboard for visualization.

## Test Plan and Strategy
The test plan simulates concurrent user traffic to the API and includes the following key components:
- **POST Request**: To create a new user in the system.
- **GET Request**: To retrieve user details from the system.
- **PUT Request**: To update existing user details.
- **DELETE Request**: To remove a user from the system.

The test was executed with different user threads to evaluate the API's behavior under various levels of stress. The API responses were monitored for latency, response time, throughput, and error rates.

## Commands Used
The test was executed using the following JMeter commands:

```bash
# Running the performance test in non-GUI mode and generating JTL file
jmeter -n -t resResTest_t160.jmx -l report/resResTest_t160.jtl

# Generating the HTML report from the JTL file
jmeter -g report/resResTest_t160.jtl -o report/resResTest_t160.html
```
## Results and Analysis
The performance test was conducted with a focus on the following metrics:

- **Response Time (ms)**: Measures the time taken to process requests.
- **Throughput (requests per second)**: Evaluates the number of requests processed per second.
- **Latency (ms)**: Indicates the delay before the response starts.
- **Error Rate (%)**: Tracks the percentage of failed requests.

### Key Metrics from Test
- **Total Requests**: 160
- **Average Response Time**: 1267 ms
- **Throughput**: 5 requests/second
- **Max Response Time**: 12711 ms
- **Minimum Response Time**: 18 ms
- **Error Rate**: 0%

### Visual Report
The detailed performance test report, including graphs and analysis, can be viewed in the HTML file: `report/resResTest_t160.html`.

### Key Findings
- The **POST requests** exhibited higher response times, especially under high load conditions, with a maximum response time of **12.7 seconds**.
- **GET requests** were more consistent with a very low average response time.
- **PUT requests** showed stable performance, although response times were slightly higher than **GET** requests.
- **DELETE requests** had the fastest response times on average, indicating the API handles these requests efficiently under load.
- The throughput decreased as the number of users increased, highlighting potential bottlenecks during peak usage.
- No errors were encountered, indicating stable API behavior.

### Conclusion
The reqRes API performed well under moderate load but showed signs of performance degradation with increased concurrent users, particularly in handling **POST** requests. Further optimization may be required for handling larger traffic volumes. The API is stable with no error occurrences in the tests.

##_Screenshots_
![image](https://github.com/user-attachments/assets/d3ca3883-1e66-435a-a326-6e732965a827)
![image](https://github.com/user-attachments/assets/82b43309-cb10-42a2-b36e-3d819901a5e6)
![image](https://github.com/user-attachments/assets/32d63370-56bf-4a82-bd24-3bf3014f6b47)
![image](https://github.com/user-attachments/assets/c87c2fa5-7e9d-4a9b-aff0-1e55c0e13b08)

## Authors

- [@abutalha](https://github.com/md-abutalha)


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/md-abutalha)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abu-talha1/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/abu_talha0x)

