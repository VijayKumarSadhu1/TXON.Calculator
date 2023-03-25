# TXON.Calculator
<!DOCTYPE html>
<html>

<head>
    <title>Calculator</title>
    <script src="https://kit.fontawesome.com/c9e7cf9fc2.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="container">
        <div class="calculator">
            <div class="top-card">
                <h1 class="heading"><span style="color:white">C</span><span style="color:#eb7609">A</span><span style="color:black">L</span><span style="color:#192ee6">C</span><span style="color:#671cc9">U</span><span style="color:#c1eb09">L</span><span style="color:#d60d24">A</span><span style="color:#2cd7f5">T</span><span style="color:#ffffff">O</span><span style="color:#27eb09">R</span></h1>
                <i class="fa-solid fa-calculator fa-bounce fa-2xl icon"></i>
            </div>
            <div class="screen">

                <input type="text" id="result" class="input" disabled>
            </div>
            <div class="buttons">
                <button onclick="clearResult()">C</button>
                <button onclick="deleteChar()">CE</button>
                <button onclick="addToResult('/')">/</button>
                <button onclick="addToResult('*')">*</button>
                <button onclick="addToResult('7')">7</button>
                <button onclick="addToResult('8')">8</button>
                <button onclick="addToResult('9')">9</button>
                <button onclick="addToResult('-')">-</button>
                <button onclick="addToResult('4')">4</button>
                <button onclick="addToResult('5')">5</button>
                <button onclick="addToResult('6')">6</button>
                <button onclick="addToResult('+')">+</button>
                <button onclick="addToResult('1')">1</button>
                <button onclick="addToResult('2')">2</button>
                <button onclick="addToResult('3')">3</button>
                <button onclick="calculate()">=</button>
                <button onclick="addToResult('0')">0</button>
                <button onclick="addToResult('.')">.</button>
            </div>
        </div>
    </div>
    <!-- <script src="script.js"></script> -->
</body>

</html>






@import url('https://fonts.googleapis.com/css2?family=Bree+Serif&family=Caveat:wght@400;700&family=Lobster&family=Monoton&family=Open+Sans:ital,wght@0,400;0,700;1,400;1,700&family=Playfair+Display+SC:ital,wght@0,400;0,700;1,700&family=Playfair+Display:ital,wght@0,400;0,700;1,700&family=Roboto:ital,wght@0,400;0,700;1,400;1,700&family=Source+Sans+Pro:ital,wght@0,400;0,700;1,700&family=Work+Sans:ital,wght@0,400;0,700;1,700&display=swap');

* {}

.container {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #89b3b2;
    background-size: cover;
    height: 100vh;
}

.calculator {
    width: 340px;


    padding: 10px;
    border: 1px solid black;
    border-radius: 10px;
    box-shadow: 10px 10px black;
    height: 400px;
    background-image: linear-gradient(to right, #4084b8, #627371);
    /* background-color:black; */
    background-size: cover;
}

.top-card {
    display: flex;
}

.icon {
    align-self: center;
    margin-left: 10px;
    color: black;
}

.screen {

    margin-bottom: 10px;


}

.heading {
    color: #2f574b;
    font-size: 33px;
    font-weight: bold;
    text-shadow: 0px 0px;
    font-family: "#POUND, sans-serif";
    font-style: italic;
}

.buttons {
    margin-top: 10px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
    height: 200px;

}

button {
    font-size: 20px;
    padding: 5px 10px;
    border: none;
    border-radius: 5px;
    background-color: #eee;
    cursor: pointer;
    margin: 5px;
}

button {
    background-color: blue;
    color: #ffffff;
    font-size: 20px;
    border-radius: 40%;
    box-shadow: 3px 3px;

}

button:hover {
    /* font-size:33px; */
    background-color: #ffffff;
    color: black;
    /*     box-shadow:1px 1px
 */
}

.input {
    font-size: 20px;
    color: black;
    height: 30px;
    width: 300px;
    border: 2px solid;
    background-color: white;
    box-shadow: 3px 3px;
    margin-left: 4px;
    margin-bottom: 20px;
}



let result = document.getElementById('result');

function addToResult(char) {
    result.value += char;
}

function clearResult() {
    result.value = '';
}

function deleteChar() {
    result.value = result.value.slice(0, -1);
}

function calculate() {
    result.value = eval(result.value);
}
