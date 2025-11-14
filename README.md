<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Answerly Rev Lost Calculator</title>

<style>
  body {
    margin: 0;
    padding: 40px;
    background: linear-gradient(135deg, #4f46e5, #3b82f6);
    font-family: "Inter", sans-serif;
    color: #fff;
  }

  .calculator {
    max-width: 450px;
    margin: auto;
    background: #ffffff;
    color: #333;
    padding: 35px;
    border-radius: 18px;
    box-shadow: 0 10px 35px rgba(0, 0, 0, 0.25);
    animation: fadeIn 0.9s ease forwards;
  }

  h2 {
    text-align: center;
    margin-top: 0;
    font-size: 26px;
    color: #3b82f6;
  }

  label {
    display: block;
    margin-top: 20px;
    font-weight: 600;
    margin-bottom: 6px;
  }

  input {
    width: 100%;
    padding: 14px;
    border-radius: 10px;
    border: 2px solid #d6d6d6;
    font-size: 16px;
    transition: 0.3s ease;
  }

  input:focus {
    border-color: #3b82f6;
    box-shadow: 0 0 8px rgba(59, 130, 246, 0.4);
    outline: none;
  }

  button {
    width: 100%;
    margin-top: 30px;
    padding: 15px;
    font-size: 18px;
    border: none;
    border-radius: 12px;
    background: #3b82f6;
    color: white;
    cursor: pointer;
    transition: 0.3s;
  }

  button:hover {
    background: #2563eb;
    transform: translateY(-2px);
  }

  .result {
    margin-top: 25px;
    font-size: 22px;
    font-weight: 700;
    text-align: center;
    opacity: 0;
    transform: translateY(10px);
    transition: 0.4s ease;
    color: #111;
  }

  .result.show {
    opacity: 1;
    transform: translateY(0);
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>
</head>

<body>

<div class="calculator">
  <h2>Answerly Rev Lost Calculator</h2>

  <label>Calls Lost</label>
  <input type="number" id="callsLost" placeholder="Enter number of calls lost">

  <label>Average Job Price ($)</label>
  <input type="number" id="jobPrice" placeholder="Enter average job price">

  <button onclick="calculateRevenue()">Calculate Revenue Lost</button>

  <div id="result" class="result"></div>
</div>

<script>
function calculateRevenue() {
  let calls = document.getElementById("callsLost").value;
  let price = document.getElementById("jobPrice").value;
  let resultBox = document.getElementById("result");

  if (calls === "" || price === "") {
    resultBox.textContent = "Please fill in both fields.";
    resultBox.classList.add("show");
    return;
  }

  let total = calls * price;

  resultBox.textContent = "Total Revenue Lost: $" + total.toLocaleString();
  resultBox.classList.add("show");
}
</script>

</body>
</html>
# Calculator
