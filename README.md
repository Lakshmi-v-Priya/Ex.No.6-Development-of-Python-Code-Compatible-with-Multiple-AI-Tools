# Ex.No: 6 Development of Python Code Compatible with Multiple AI Tools  
**Name :** Lakshmi Priya.V   **Reg No :** 212223220049 

---

# Aim

To write and implement Python code that integrates with multiple AI tools to automate tasks such as interacting with APIs, comparing outputs, and generating actionable insights.

---

# AI Tools Required

- ChatGPT (GPT-5.2)
- Google Gemini (or any second AI tool)
- Python 3.x
- Requests library
- JSON library

---

# Objective

Learners will design effective prompts that guide AI tools to:

- Generate Python code for interacting with multiple APIs.
- Compare outputs from different APIs.
- Highlight differences in responses.
- Suggest meaningful insights based on results.

---

# Selected Application Domain

AI-based Weather Data Comparison System  
(Useful for smart city or IoT-based climate monitoring projects)

---

# Activity

## Stage 1: Persona Pattern Prompt (Programmer Role)

### Prompt Designed

> You are a professional Python developer working on a Smart Climate Monitoring System.  
> Write Python code to fetch weather data (temperature and humidity) from two different weather APIs.  
> Use the requests library.  
> Store both API responses in JSON format.  
> Handle errors properly.  
> Add comments explaining each section of the code.

---

## AI Tool 1: ChatGPT – Generated Code

```python
import requests

API_KEY_1 = "your_api_key_1"
API_KEY_2 = "your_api_key_2"

city = "Chennai"

def fetch_api_1():
    url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY_1}&units=metric"
    response = requests.get(url)
    if response.status_code == 200:
        return response.json()
    else:
        print("Error fetching from API 1")
        return None

def fetch_api_2():
    url = f"http://api.weatherapi.com/v1/current.json?key={API_KEY_2}&q={city}"
    response = requests.get(url)
    if response.status_code == 200:
        return response.json()
    else:
        print("Error fetching from API 2")
        return None

data1 = fetch_api_1()
data2 = fetch_api_2()

if data1 and data2:
    print("API 1 Temperature:", data1["main"]["temp"])
    print("API 2 Temperature:", data2["current"]["temp_c"])
```

### Explanation

- Fetches weather data from two APIs.
- Uses proper error handling.
- Extracts temperature data.
- Clean and structured format.

---

## AI Tool 2: Gemini – Generated Code (Summary)

- Similar structure using requests
- Added try-except blocks
- Included timeout parameter
- Better error exception handling

---

# Stage 2: Prompt for Comparing Outputs

### Prompt Designed

> Write Python code to compare temperature and humidity values obtained from two weather APIs.  
> Calculate the difference between both APIs.  
> Display a warning if the difference exceeds 2°C.  
> Add meaningful print statements.

---

### ChatGPT Output (Comparison Logic)

```python
if data1 and data2:
    temp1 = data1["main"]["temp"]
    temp2 = data2["current"]["temp_c"]
    
    difference = abs(temp1 - temp2)
    
    print(f"Temperature from API 1: {temp1}°C")
    print(f"Temperature from API 2: {temp2}°C")
    print(f"Difference: {difference}°C")
    
    if difference > 2:
        print("Warning: Significant temperature difference detected!")
```

---

# Evaluation & Comparative Analysis

## Evaluation Method Used: Rubric-Based Analysis

| Criteria | ChatGPT | Gemini |
|----------|----------|---------|
| Code Clarity | Excellent | Very Good |
| Error Handling | Good | Excellent |
| Structure | Well organized | Well organized |
| Depth of Explanation | Detailed | Moderate |
| Practical Insights | Strong | Moderate |

---

# Analysis Discussion

- ChatGPT generated clearer documentation and structured output.
- Gemini provided stronger error-handling mechanisms.
- Both tools produced accurate Python code.
- Prompt clarity significantly influenced output quality.
- Persona pattern improved technical precision.

---

# Conclusion

This experiment demonstrated that well-designed prompts significantly improve AI-generated code quality.

Using multiple AI tools provides:

- Diverse coding approaches
- Better error handling
- More comprehensive insights

Prompt engineering plays a crucial role in AI-assisted project development.

---

# Result

The corresponding prompt is executed successfully.
