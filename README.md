# Simple--calculator-
Python and html based calculator project 
<!DOCTYPE html>
<html>
<head>
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial;
      background-color: #f0f0f0;
      text-align: center;
      padding: 50px;
    }
    .calculator {
      background: white;
      display: inline-block;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    input, select, button {
      margin: 10px;
      padding: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>

  <div class="calculator">
    <h2>Simple Calculator</h2>
    <input type="number" id="num1" placeholder="First Number"><br>
    <input type="number" id="num2" placeholder="Second Number"><br>

    <select id="operation">
      <option value="add">Add</option>
      <option value="subtract">Subtract</option>
      <option value="multiply">Multiply</option>
      <option value="divide">Divide</option>
    </select><br>

    <button onclick="calculate()">Calculate</button>
    <h3 id="result"></h3>
  </div>

  <script>
    function calculate() {
      const n1 = parseFloat(document.getElementById('num1').value);
      const n2 = parseFloat(document.getElementById('num2').value);
      const op = document.getElementById('operation').value;
      let result;

      if (op === "add") result = n1 + n2;
      else if (op === "subtract") result = n1 - n2;
      else if (op === "multiply") result = n1 * n2;
      else if (op === "divide") result = n2 !== 0 ? n1 / n2 : "Cannot divide by zero";

      document.getElementById('result').innerText = "Result: " + result;
    }
  </script>

</body>
</html>
