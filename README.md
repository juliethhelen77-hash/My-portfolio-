<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculator - by Julieth</title>
<style>
body{display:flex;justify-content:center;align-items:center;min-height:100vh;background:#0a192f;margin:0;font-family:Arial}
.calc{background:#fff;padding:20px;border-radius:15px;box-shadow:0 10px 30px rgba(0,0,0,0.3);width:300px}
#display{width:100%;height:60px;font-size:28px;text-align:right;padding:10px;box-sizing:border-box;border:2px solid #0a192f;border-radius:8px;margin-bottom:15px;background:#e6f1ff}
.buttons{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
button{padding:20px;font-size:20px;border:none;border-radius:8px;cursor:pointer;background:#e6e6e6;font-weight:bold}
button:hover{background:#d1d1d1}
.op{background:#64ffda;color:#0a192f}
.equal{background:#0a192f;color:white;grid-column:span 2}
.clear{background:#ff6b6b;color:white}
</style>
</head>
<body>
<div class="calc">
<input type="text" id="display" disabled placeholder="0">
<div class="buttons">
<button class="clear" onclick="clearDisplay()">C</button>
<button onclick="deleteLast()">DEL</button>
<button class="op" onclick="append('/')">/</button>
<button class="op" onclick="append('*')">*</button>

<button onclick="append('7')">7</button>
<button onclick="append('8')">8</button>
<button onclick="append('9')">9</button>
<button class="op" onclick="append('-')">-</button>

<button onclick="append('4')">4</button>
<button onclick="append('5')">5</button>
<button onclick="append('6')">6</button>
<button class="op" onclick="append('+')">+</button>

<button onclick="append('1')">1</button>
<button onclick="append('2')">2</button>
<button onclick="append('3')">3</button>
<button onclick="append('.')">.</button>

<button onclick="append('0')">0</button>
<button class="equal" onclick="calculate()">=</button>
</div>
<p style="text-align:center;font-size:12px;margin-top:15px;color:#888">Built by Okeke Julieth Ujunwa</p>
<p> <a href="https://juliethhelen77-hash/calculator/" target="_blank" style="color:#64ffda; background:#0a192f; padding:5px 10px; border-radius:5px; text-decoration:none;">View Live -></a>
</p>




</div>

<script>
let display = document.getElementById('display');
function append(val){ display.value += val; }
function clearDisplay(){ display.value = ''; }
function deleteLast(){ display.value = display.value.slice(0,-1); }
function calculate(){
  try{ display.value = eval(display.value); }
  catch{ display.value = 'Error'; }
}
</script>
</body>
</html>
