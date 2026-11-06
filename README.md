# tip-calculator-
<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Tip Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      background-color: #f5f5f5;
    }
    input, button {
      display: block;
      width: 100%;
      box-sizing: border-box;
      margin: 10px 0;
      padding: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <h1>Tip Calculator</h1>
  <input id="bill" type="number" placeholder="Bill amount">
  <input id="tip" type="number" placeholder="Tip %">
  <button onclick="calculate()">Calculate</button>
  <p id="result"></p>

  <script>
    function calculate() {
      let bill = Number(document.getElementById("bill").value);
      let tip = Number(document.getElementById("tip").value);
      let total = bill + (bill * tip / 100);
      document.getElementById("result").textContent = "Total: " + total.toFixed(2);
    }
  </script>
</body>
</html>
