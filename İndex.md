# Hesap-makinesi-

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hesap Makinesi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
          
        }
        .calculator {
            margin: 0 auto;
            width: 300px;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #f9f9f9;
        }
        .button {
            width: 60px;
            height: 40px;
            margin: 5px;
            font-size: 18px;
            border-radius: 5px;
            border: 1px solid #ccc;
            background-color: #fff;
            cursor: pointer;
        }
        .button:hover {
            background-color: #e6e6e6;
        }
        .display {
            width: 100%;
            height: 40px;
            margin-bottom: 10px;
            font-size: 18px;
            padding: 5px;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" class="display" readonly>
        <br>
        <button class="button" onclick="addToDisplay('1')">1</button>
        <button class="button" onclick="addToDisplay('2')">2</button>
        <button class="button" onclick="addToDisplay('3')">3</button>
        <button class="button" onclick="addToDisplay('+')">+</button>
        <br>
        <button class="button" onclick="addToDisplay('4')">4</button>
        <button class="button" onclick="addToDisplay('5')">5</button>
        <button class="button" onclick="addToDisplay('6')">6</button>
        <button class="button" onclick="addToDisplay('-')">-</button>
        <br>
        <button class="button" onclick="addToDisplay('7')">7</button>
        <button class="button" onclick="addToDisplay('8')">8</button>
        <button class="button" onclick="addToDisplay('9')">9</button>
        <button class="button" onclick="addToDisplay('*')">*</button>
        <br>
        <button class="button" onclick="addToDisplay('0')">0</button>
        <button class="button" onclick="addToDisplay('.')">.</button>
        <button class="button" onclick="calculate()">=</button>
        <button class="button" onclick="addToDisplay('/')">/</button>
        <br>
        <button class="button" onclick="clearDisplay()">Clear</button>
    </div>
  <h1>BEBE TECHNLOGY GROUP</h1>
    <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                var result = eval(document.getElementById('display').value);
                document.getElementById('display').value = result;
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>
</html>
