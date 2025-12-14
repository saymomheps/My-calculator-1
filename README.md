# My-calculator-1
My new calculator
inde.html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial;
            background: #f2f2f2;
        }
        .calculator {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }
        input {
            width: 100%;
            height: 40px;
            font-size: 20px;
            margin-bottom: 10px;
            text-align: right;
        }
        button {
            width: 60px;
            height: 40px;
            font-size: 18px;
            margin: 3px;
        }
    </style>
</head>
<body>

<div class="calculator">
    <input type="text" id="result" disabled>

    <div>
        <button onclick="clearResult()">C</button>
        <button onclick="deleteOne()">DEL</button>
        <button onclick="add('/')">/</button>
        <button onclick="add('*')">*</button>
    </div>
    <div>
        <button onclick="add('7')">7</button>
        <button onclick="add('8')">8</button>
        <button onclick="add('9')">9</button>
        <button onclick="add('-')">-</button>
    </div>
    <div>
        <button onclick="add('4')">4</button>
        <button onclick="add('5')">5</button>
        <button onclick="add('6')">6</button>
        <button onclick="add('+')">+</button>
    </div>
    <div>
        <button onclick="add('1')">1</button>
        <button onclick="add('2')">2</button>
        <button onclick="add('3')">3</button>
        <button onclick="calculate()">=</button>
    </div>
    <div>
        <button onclick="add('0')" style="width: 190px;">0</button>
        <button onclick="add('.')">.</button>
    </div>
</div>

<script>
    function add(value) {
        document.getElementById("result").value += value;
    }

    function calculate() {
        document.getElementById("result").value =
        eval(document.getElementById("result").value);
    }

    function clearResult() {
        document.getElementById("result").value = "";
    }

    function deleteOne() {
        let x = document.getElementById("result").value;
        document.getElementById("result").value = x.slice(0, -1);
    }
</script>

</body>
</html>
