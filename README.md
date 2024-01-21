# Logging Configuration in Spring Boot

In your Spring Boot application, logging is configured using properties in the `application.properties` file, and logging functionality is implemented in the `MessageController` class. Below are key advantages of using log files and how they are configured:

## Advantages of Log Files

1. **Centralized Logging:**
   - Log files provide a centralized location to store and view application logs. This is crucial for monitoring and troubleshooting in production environments.

2. **Historical Analysis:**
   - Log files capture a historical record of application events, errors, and warnings. This information is valuable for analyzing past issues and understanding the behavior of the application over time.

3. **Performance Monitoring:**
   - Log files can be used to monitor the performance of the application. You can track response times, identify bottlenecks, and analyze resource utilization.

4. **Security Auditing:**
   - Log files play a significant role in security auditing, allowing tracing and investigating security-related events or suspicious activities within the application.

5. **Debugging and Troubleshooting:**
   - Log files contain detailed information about the application's execution flow. This aids developers in debugging issues and troubleshooting problems, especially in production environments where direct debugging may not be possible.

## Logging Configuration in `application.properties`

```properties
# Set log level for the controller package to DEBUG
com.example.springbootlogging.controller = DEBUG

# Logging pattern for the console
logging.pattern.console = %date{ISO8601} %-5level %class{0}:%L - [%X] %msg%n

# Logging pattern for the file
logging.pattern.file = %date{ISO8601} %5level %class{0}:%L - [%X] %msg%n

# Output file for logs
logging.file.name = application.log
