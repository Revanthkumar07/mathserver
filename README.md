# Ex.05 Design a Website for Server Side Processing
# Date:21-04-2025
# Name: BEEDA VENKATA REVANTH KUMAR
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Light Bulb Power Calculator</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        .container {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
        }
        input {
            width: 100px;
            padding: 5px;
            text-align: center;
        }
        .result {
            font-weight: bold;
            font-size: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>
            <span style="font-size: 24px;">&#128161;</span> Light Bulb Power Calculator
        </h1>
        <label>Voltage (V): </label>
        <input type="number" id="voltage" value="10"> V
        <br><br>
        <label>Current (A): </label>
        <input type="number" id="current" value="5"> A
        <br><br>
        <div class="result">Power (W): <span id="power">50.00</span> W</div>
    </div>
    
    <script>
        function calculatePower() {
            let voltage = parseFloat(document.getElementById('voltage').value);
            let current = parseFloat(document.getElementById('current').value);
            let power = voltage * current;
            document.getElementById('power').innerText = power.toFixed(2);
        }
        
        document.getElementById('voltage').addEventListener('input', calculatePower);
        document.getElementById('current').addEventListener('input', calculatePower);
    </script>
</body>
</html>
```
views.py
```
from django.shortcuts import render

def index(request):
    return render(request, 'index.html')  # Ensure 'index.html' is inside the 'templates' folder

```
urls.py
```
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]

```
# SERVER SIDE PROCESSING:
![image](https://github.com/user-attachments/assets/edcbced0-bcf8-4f99-baa0-28f56e06491f)

# HOMEPAGE:
![image](https://github.com/user-attachments/assets/90682431-b86b-496c-a560-18a30dc563b1)

# RESULT:
The program for performing server side processing is completed successfully.
