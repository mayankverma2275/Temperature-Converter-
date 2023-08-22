# Temperature-Converter-
#HTML CODE :-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="input-group">
            <label for="celsius">Celsius:</label>
            <input type="number" id="celsius" placeholder="Enter temperature in Celsius">
        </div>
        <div class="input-group">
            <label for="fahrenheit">Fahrenheit:</label>
            <input type="number" id="fahrenheit" placeholder="Enter temperature in Fahrenheit">
        </div>
        <button id="convertBtn">Convert</button>
    </div>
    <script src="script.js"></script>
</body>
</html>



#CSS CODE :-
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container {
    background-color: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
    text-align: center;
}

.input-group {
    margin: 10px 0;
}

label {
    display: inline-block;
    width: 100px;
    text-align: left;
}

input {
    width: 150px;
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

button {
    padding: 10px 20px;
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}


#JS CODE :-
const celsiusInput = document.getElementById("celsius");
const fahrenheitInput = document.getElementById("fahrenheit");
const convertBtn = document.getElementById("convertBtn");

convertBtn.addEventListener("click", convertTemperature);

function convertTemperature() {
    const celsiusValue = parseFloat(celsiusInput.value);
    const fahrenheitValue = parseFloat(fahrenheitInput.value);

    if (!isNaN(celsiusValue)) {
        const fahrenheitCalculated = (celsiusValue * 9/5) + 32;
        fahrenheitInput.value = fahrenheitCalculated.toFixed(2);
    }

    if (!isNaN(fahrenheitValue)) {
        const celsiusCalculated = (fahrenheitValue - 32) * 5/9;
        celsiusInput.value = celsiusCalculated.toFixed(2);
    }
}

#CSS CODE
