# Calculator code

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Calculator</title>
  </head>
  <style>
    * {
      margin: 0px;
      padding: 0;
      height: 100;
      width: 100;
      box-sizing: border-box;
      background-color: aliceblue;
      font-family:sans-serif;
    }
  
    .container {
      height: 90vb;
      width: 80vb;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .calculator {
      background-color: rgb(37, 37, 37);
      padding: 40px;
      height: 500px;
      width: 350px;
      border-radius: 50px;
      box-shadow: inset 5px 5px 12px #ffffff rgba(0, 0, 0, 0.16);
      display: grid;
      grid-template-columns: repeat(4, 68px);
    }
    input {
      grid-column: span 4;
      height: 70px;
      width: 260px;
      border: none;
      border-radius: 30px;
      box-shadow: inset5px 5px 12px #ffffff rgba(0, 0, 0, 0.16);
      background-color: aliceblue;
      color: rgb(70, 70, 70);
      text-align: end;
      margin-top: 10px;
      margin-bottom: 5px;
      font-size: 50px;
      padding: 20px;
    }
    .button {
      height: 60px;
      width: 60px;
      border-radius: 50%;
      box-shadow: inset5px 5px 12px #ffffff rgba(0, 0, 0, 0.16);
      background-color: red;
      margin: 8px;
      font-size: 16px;
    }
    .equal {
      width: 140px;
      color: #ffffff;
      border-radius: 40px;
      box-shadow: inset5px 5px 12px #ffffff rgba(0, 0, 0, 0.16);
      background-color: rgb(69, 69, 239);
    }
    .addition{
      background-color: rgb(39, 221, 249);
      font-style: bold;
      color:rgb(249, 9, 13);
      font-size: x-large;
    }
    .subtraction{
      background-color: rgb(39, 221, 249);
      font-style: bold;
      color:rgb(249, 9, 13);
      font-size: x-large;
    }
    .multiplication{
      background-color: rgb(39, 221, 249);
      font-style: bold;
      color:rgb(249, 9, 13);
      font-size: x-large;
    }
    .division{
      background-color: rgb(39, 221, 249);
      font-style: bold;
      color:rgb(249, 9, 13);
      font-size: x-large;
    }
    .percentage{
      background-color: rgb(39, 221, 249);
      font-style: bold;
      color:rgb(249, 9, 13);
      font-size: x-large;
    }
    .clear{
      background-color: rgb(252, 9, 9);
      font-style: bold;
      color:rgb(255, 255, 255);
      font-size: 90;
    }
    .delete{
      background-color: rgb(252, 9, 9);
      font-style: bold;
      color:rgb(255, 255, 255);
      font-size: 90;
    }
  </style>
  <body>
    <div class="container">
      <div class="calculator">
        <input type="text" placeholder="0" id="outputscreen" />
        <button onclick="Clear()"class="clear">Clear</button>
        <button onclick="del()"class="delete">Delete</button>
        <button onclick="display('%')"class="percentage">%</button>
        <button onclick="display('/')"class="division">/</button>
        <button onclick="display('7')">7</button>
        <button onclick="display('8')">8</button>
        <button onclick="display('9')">9</button>
        <button onclick="display('*')"class="multiplication">*</button>
        <button onclick="display('4')">4</button>
        <button onclick="display('5')">5</button>
        <button onclick="display('6')">6</button>
        <button onclick="display('-')"class="subtraction">-</button>
        <button onclick="display('1')">1</button>
        <button onclick="display('2')">2</button>
        <button onclick="display('3')">3</button>
        <button onclick="display('+')"class="addition">+</button>
        <button onclick="display('.')">.</button>
        <button onclick="display('0')">0</button>
        <button onclick="Calculate()" class="equal">=</button>
      </div>
    </div>
    <script>
      let outputscreen = document.getElementById("outputscreen");
      function display(num) {
        outputscreen.value += num;
      }
      function Calculate() {
        try {
          outputscreen.value = eval(outputscreen.value);
        } catch (err) {
          alert("Invaild");
        }
      }
      function Clear() {
        outputscreen.value = "";
      }
      function del() {
        outputscreen.value = outputscreen.value.slice(0, -1);
      }
    </script>
  </body>
</html>
