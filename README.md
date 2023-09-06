# Websites-Monitor-and-Report-F-Secure
This tool is for monitoring web sites and to report their availability. It is useful for web site administrators for detecting problems on their sites and ensuring that service is up.

**Website Monitoring Tool**

**Overview**
Here is a program designed to monitor web sites and report their availability. This tool will help us know in frequent intervals when the service as per the mentioned content requirement is up and if not then display the reason for the same. By this program we will ease the need to manually check as this program will monitor it in the log file.

1.	Reads a list of web pages (HTTP URLs) and corresponding page content requirements from a configuration file.
2.	Periodically makes HTTP requests to each page to check their availability.
3.	Verifies that the page content received from the server matches the specified content requirements.
4.	Measures the time it takes for the web server to complete each request.
5.	Writes detailed log files that show the progress of the periodic checks.
6.	(OPTIONAL) Implement a single-page HTTP server interface in the same process that shows (HTML) each monitored web site and their current (last check) status.

**Prerequisites  :**



-  Ensure you have Python 3.x installed on your system.
-  Required Python packages (e.g., requests, configparser, time, logging, http.server, etc.)

A. **Installation**
-  Clone this repository to your local machine:
-  Navigate to the project directory:

B. **Configuration**:
 -  Create a configuration file (config.json) with a list of websites to monitor and their content requirements.-->Configuration File (config.json)
-  The config.json file contains a list of websites to monitor, their content requirements, and other settings:

  -   Here the websites of the sites to be monitored "websites":

    List of websites to monitor, each with a "url" and "content_requirement".
      
    "interval": The checking period in seconds.
    
    "enable_http_server": (Optional) Whether to enable the single-page HTTP server interface.

C. **Running the Program**:

Execute the program with the following command:
python main.py config.json 
Remember to mention the path of the config file or place it in the same folder as the python program.
Viewing Results:
The program will periodically check the websites and log the results to a file named website_checker.log.

D. **Logging**

The tool will generate a log file (monitor.log) in the project directory. This log file contains information about checked URLs, their status, and response times.

