# ProjetoCalculadorahtml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Simples</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            background-color: black;
            color: white;
        }

        #calculator {
            width: 300px;
            margin: 0 auto;
            border: 4px solid #ccc;
            border-radius: 5px;
            padding: 5px;
            background-color: white;
            box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.1);
        }

        #display {
            width: 100%;
            margin-bottom: 10px;
            padding: 8px;
            box-sizing: border-box;
            font-size: 5em;
            text-align: right;
            border: none;
            outline: none;
            border-bottom: 2px solid #ccc;
            margin-bottom: 15px;
        }

        input[type="button"] {
            width: 48px;
            height: 48px;
            font-size: 1.5em;
            margin: 2px;
            cursor: pointer;
            background-color: #ccc;
            border: 1px solid #aaa;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <div id="calculator">
        <input type="text" id="display" disabled>
        <br>
        <input type="button" value="7" onclick="appendToDisplay('7')">
        <input type="button" value="8" onclick="appendToDisplay('8')">
        <input type="button" value="9" onclick="appendToDisplay('9')">
        <input type="button" value="/" onclick="appendToDisplay('/')">
        <br>
        <input type="button" value="4" onclick="appendToDisplay('4')">
        <input type="button" value="5" onclick="appendToDisplay('5')">
        <input type="button" value="6" onclick="appendToDisplay('6')">
        <input type="button" value="-" onclick="appendToDisplay('-')">
        <br>
        <input type="button" value="1" onclick="appendToDisplay('1')">
        <input type="button" value="2" onclick="appendToDisplay('2')">
        <input type="button" value="3" onclick="appendToDisplay('3')">
        <input type="button" value="+" onclick="appendToDisplay('+')">
        <br>
        <input type="button" value="0" onclick="appendToDisplay('0')">
        <input type="button" value="." onclick="appendToDisplay('.')">
        <input type="button" value="C" onclick="clearDisplay()">
        <input type="button" value="=" onclick="calculate()">
    </div>

    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>

</body>
</html>
