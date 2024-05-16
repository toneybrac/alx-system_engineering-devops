Issue Summary:
Duration: The outage occurred from 10:00 AM to 12:30 PM on April 15, 2024 (UTC timezone).
Impact: The service outage affected the availability of our main web application, resulting in 80% of users experiencing slow response times and intermittent errors during the outage period.
Root Cause: The root cause of the outage was identified as a misconfiguration in the load balancer settings, which led to an imbalance in traffic distribution across backend servers.
Timeline:
10:00 AM: The issue was detected when monitoring alerts indicated a significant increase in response times and error rates.
10:15 AM: Engineers began investigating the issue, initially suspecting a database or application server issue.
10:45 AM: After ruling out database and application server issues, attention shifted to the load balancer configuration.
11:30 AM: It was discovered that the load balancer was incorrectly configured, causing uneven distribution of traffic to backend servers.
11:45 AM: The incident was escalated to the DevOps team for immediate resolution.
12:30 PM: The load balancer configuration was corrected, restoring normal traffic distribution and resolving the service outage.
Root Cause and Resolution:
The root cause of the outage was traced to a misconfiguration in the load balancer settings. Specifically, the load balancer was configured with outdated server weights, leading to an uneven distribution of traffic. This resulted in some backend servers being overwhelmed with requests while others remained underutilized.
To resolve the issue, the load balancer configuration was updated to ensure equal distribution of traffic across all backend servers. Additionally, automated tests were implemented to regularly validate the load balancer configuration against predefined thresholds to prevent similar misconfigurations in the future.
