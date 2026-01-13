
<html>
<head>
    <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
    <title>Robot</title>
    <link rel="stylesheet" href="site.css" />
</head>
<body>
    <div id="OneDdiv" class="OneDiv">
        <button id="redbutt" class="butt" style="background: red; color: white; border:darkred 1px solid">red</button>
        <button id="greenbutt" class="butt" style="background: green; color: white;border:darkgreen 1px solid">green</button>
        <button id="bluebutt" class="butt" style="background: blue; color: white; border:darkblue 1px solid">blue</button>
        <button id="yellowbutt" class="butt" style="background: yellow; color: black; border:black 1px solid">yellow</button>
        <button id="pinkbutt" class="butt" style="background: pink; color: white; border:red 1px solid">pink</button>
        <p id="Sensor" class="OneP"></p>
        <button id="light" class="lightt"></button><br>
        <button id="OnOff" style="height: 30px; background: darkred; color: white; border: black 2px solid;">ON/OFF</button>
        <input id="inp" class="inp" placeholder="Enter text">
        <button class="ent" id="ent">Enter</button>
        <button id="q" class="manybutt">й</button>
        <button id="w" class="manybutt">ц</button>
        <button id="e" class="manybutt">у</button>
        <button id="r" class="manybutt">к</button>
        <button id="t" class="manybutt">е</button>
        <button id="y" class="manybutt">н</button>
        <button id="u" class="manybutt">г</button>
        <button id="i" class="manybutt">ш</button>
        <button id="o" class="manybutt">щ</button>
        <button id="p" class="manybutt">з</button>
        <button id="pp" class="manybutt">х</button>
        <button id="a" class="manybutt">ф</button>
        <button id="s" class="manybutt">ы</button>
        <button id="d" class="manybutt">в</button>
        <button id="f" class="manybutt">а</button>
        <button id="g" class="manybutt">п</button>
        <button id="h" class="manybutt">р</button>
        <button id="j" class="manybutt">о</button>
        <button id="k" class="manybutt">л</button>
        <button id="l" class="manybutt">д</button>
        <button id="ll" class="manybutt">ж</button>
        <button id="lll" class="manybutt">э</button>
        <button id="z" class="manybutt">я</button>
        <button id="x" class="manybutt">ч</button>
        <button id="c" class="manybutt">с</button>
        <button id="v" class="manybutt">м</button>
        <button id="b" class="manybutt">и</button>
        <button id="n" class="manybutt">т</button>
        <button id="m" class="manybutt">ь</button>
        <button id="mm" class="manybutt">б</button>
        <button id="mmm" class="manybutt">ю</button>
        <button id="probel" class="manybutt">Пробел</button>
        <button id="udal" class="manybutt">⌫</button>
        <button id="zap" class="manybutt">,</button>
        <button id="point" class="manybutt">.</button>
    </div>
    <script>
const buttRed = document.getElementById('redbutt');
const buttGreen = document.getElementById('greenbutt');
const buttblue = document.getElementById('bluebutt');
const buttyellow = document.getElementById('yellowbutt');
const buttPink = document.getElementById('pinkbutt');
const ddiv = document.getElementById('OneDdiv');
const znak = document.getElementById('light');
const OnOff = document.getElementById('OnOff');
let Sensor = document.getElementById('Sensor');
const inp = document.getElementById('inp');
const buttEnt = document.getElementById('ent');
let we = false;



buttRed.onclick = function u() {
    ddiv.style.background = "red";
}
buttGreen.onclick = function u() {
    ddiv.style.background = "green";
}
buttblue.onclick = function u() {
    ddiv.style.background = "blue";
}
buttyellow.onclick = function u() {
    ddiv.style.background = "yellow";
}
buttPink.onclick = function u() {
    ddiv.style.background = "pink";
}

OnOff.onclick = function () {
    znak.classList.toggle("green");
    if (znak.classList.contains("green")) {
        Sensor.textContent = "Привет, напиши `помощь` чтобы понять, что делать дальше."
    }
    else { Sensor.textContent = "" }
}

buttEnt.onclick = function () {
    if ((inp.value === "Help" | inp.value === "помощь") && (znak.classList.contains("green"))) {
        Sensor.textContent = "Итак! Это робот Шима. Он будет помогать тебе в твоих маленьких делах. Конечно, в нем мало пока что программ, но со временем он будет развиваться! У него есть 1 функционал: 1) Заметки . Так же он имеет такие команды как:Help, Zam, ";
        inp.value = ""
    }
    if (inp.value === "Zam" | inp.value === "заметки") {
        Sensor.textContent = "А это твои заметки! ";
        inp.value = "";
        const ty = document.createElement('textarea');
        Sensor.appendChild(ty)
    }
    if (inp.value === "кальк") {
        inp.value = "";
        const inpk = document.createElement('input');
        const buttplus = document.createElement('button');
        const buttminus = document.createElement('button');
        const buttdiv = document.createElement('button');
        const buttmul = document.createElement('button');
        const inpkk = document.createElement('input');
        Sensor.textContent = "Твой калькулятор:"
        Sensor.appendChild(inpk);
        Sensor.appendChild(buttplus);
        Sensor.appendChild(buttminus);
        Sensor.appendChild(buttdiv);
        Sensor.appendChild(buttmul);
        Sensor.appendChild(inpkk);
    }
}






//КЛАВИАТУРА!!//
const buttЙ = document.getElementById('q');
buttЙ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "й" }
}
const buttЦ = document.getElementById('w');
buttЦ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ц" }
}
const buttУ = document.getElementById('e');
buttУ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "у" }
}
const buttК = document.getElementById('r');
buttК.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "к" }
}
const buttЕ = document.getElementById('t');
buttЕ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "е" }
}
const buttН = document.getElementById('y');
buttН.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "н" }
}
const buttГ = document.getElementById('u');
buttГ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "г" }
}
const buttШ = document.getElementById('i');
buttШ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ш" }
}
const buttЩ = document.getElementById('o');
buttЩ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "щ" }
}
const buttЗ = document.getElementById('p');
buttЗ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "з" }
}
const buttХ = document.getElementById('pp');
buttХ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "х" }
}
const buttФ = document.getElementById('a');
buttФ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ф" }
}
const buttЫ = document.getElementById('s');
buttЫ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ы" }
}
const buttВ = document.getElementById('d');
buttВ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "в" }
}
const buttА = document.getElementById('f');
buttА.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "а" }
}
const buttП = document.getElementById('g');
buttП.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "п" }
}
const buttР = document.getElementById('h');
buttР.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "р" }
}
const buttО = document.getElementById('j');
buttО.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "о" }
}
const buttЛ = document.getElementById('k');
buttЛ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "л" }
}
const buttД = document.getElementById('l');
buttД.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "д" }
}
const buttЖ = document.getElementById('ll');
buttЖ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ж" }
}
const buttЭ = document.getElementById('lll');
buttЭ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "э" }
}
const buttЯ = document.getElementById('z');
buttЯ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "я" }
}
const buttЧ = document.getElementById('x');
buttЧ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ч" }
}
const buttС = document.getElementById('c');
buttС.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "с" }
}
const buttМ = document.getElementById('v');
buttМ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "м" }
}
const buttИ = document.getElementById('b');
buttИ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "и" }
}
const buttТ = document.getElementById('n');
buttТ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "т" }
}
const buttЬ = document.getElementById('m');
buttЬ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ь" }
}
const buttБ = document.getElementById('mm');
buttБ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "б" }
}
const buttЮ = document.getElementById('mmm');
buttЮ.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "ю" }
}
const buttПробел = document.getElementById('probel')
buttПробел.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + " " }
}
const buttзап = document.getElementById('zap');
buttзап.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "," }
}
const buttточка = document.getElementById('point');
buttточка.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = inp.value + "." }
}
const buttУдалить = document.getElementById('udal');
buttУдалить.onclick = function () {
    if (znak.classList.contains("green")) { inp.value = "" }
}
    </script>
</body>
</html>
