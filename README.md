# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

## Date:28.05.2026
## Name: RAGSUDHA R
## Register no.212224230215
## Aim: 
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

#AI Tools Required:

## Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

## Conclusion:
## Stage 1: Prompt for Python Code Generation
Prompt

“Generate Python code to fetch current weather data from two APIs using city name input. Use requests library and display temperature, humidity, and weather conditions.”

AI-Generated Response
Code
```
import requests

city = "Chennai"

api1 = f"https://api.weatherapi.com/v1/current.json?key=API_KEY&q={city}"
api2 = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid=API_KEY"

response1 = requests.get(api1).json()
response2 = requests.get(api2).json()

print("Weather API:")
print("Temperature:", response1['current']['temp_c'])
print("Humidity:", response1['current']['humidity'])

print("\nOpenWeather API:")
print("Temperature:", response2['main']['temp'])
print("Humidity:", response2['main']['humidity'])
```
Explanation
Uses the requests library to call APIs.
Fetches weather information from two different services.
Displays temperature and humidity values.
## Stage 2: Prompt for API Output Comparison
Prompt

“Write Python code to compare temperature and humidity values obtained from two weather APIs and display the differences clearly.”

AI-Generated Response
Code
```
temp_diff = abs(response1['current']['temp_c'] - response2['main']['temp'])
humidity_diff = abs(response1['current']['humidity'] - response2['main']['humidity'])

print("Temperature Difference:", temp_diff)
print("Humidity Difference:", humidity_diff)
```
Explanation
Calculates absolute differences between outputs.
Helps identify inconsistencies between APIs.
Useful for data validation.
## Stage 3: Prompt for Insight Generation
Prompt

“Analyze the compared weather data and suggest meaningful insights if there are major differences between API outputs.”

AI-Generated Response
Output
The temperature values differ significantly.
One API may use Celsius while another may use Kelvin.
Humidity values are nearly similar, indicating reliable readings.
Recommended step: Normalize units before comparison.
Explanation
AI identifies possible causes of variation.
Provides actionable recommendations.
Helps improve project accuracy.
## Stage 4: Advanced Prompt with Constraints
Prompt

“Act as a software engineering assistant. Generate optimized Python code for comparing weather data from multiple APIs. Include:

Error handling
API timeout handling
Unit conversion
Clear comments
Insight generation
JSON formatted output”
AI-Generated Response
Features Included
Exception handling using try-except.
Timeout support for API requests.
Automatic temperature unit conversion.
Structured JSON response format.
Insight generation based on threshold differences.
Explanation
Advanced prompts produce production-level code.
Constraints improve reliability and readability.
AI behaves like a professional coding assistant.
## Analysis of Prompt Effectiveness
Basic prompts generate general outputs.
Structured prompts improve clarity.
Context-aware prompts provide relevant code.
Constraint-based prompts produce professional-quality solutions.
Role-based prompts improve explanation quality.
# Result: 
The corresponding Prompt is executed successfully.
