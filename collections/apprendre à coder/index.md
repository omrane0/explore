
Resources to help people learn to code
<html>
<body>
<h2>My First JavaScript</h2>
<button type="button"
onclick="document.getElementById('demo').innerHTML = Date()">
Click me to display Date and Time.</button>
<p id="demo"></p>
</body>
</html> 
Mon premier JavaScript
  Cliquez sur moi pour afficher la date et l'heure.




 2. JavaScript peut changer le contenu HTML

<!DOCTYPE html>
<html>
<body>
<h2>What Can JavaScript Do?</h2>
<p id="demo">JavaScript can change HTML content.</p>
<button type="button" onclick='document.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click Me!</button>
</body>
</html>
Que peut faire JavaScript?
JavaScript peut modifier le contenu HTML.
  Cliquez sur moi!



 3. JavaScript peut modifier les valeurs d'attribut HTML
<!DOCTYPE html>
<html><body>
<h2>What Can JavaScript Do?</h2>
<p>JavaScript can change HTML attribute values.</p>
<p>In this case JavaScript changes the value of the src (source) attribute of an image.</p>
<button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>
<img id="myImage" src="pic_bulboff.gif" style="width:100px">
<button onclick="document.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light</button>
</body></html>


Que peut faire JavaScript?
JavaScript peut modifier les valeurs d'attribut HTML.
Dans ce cas, JavaScript modifie la valeur de l'attribut src (source) d'une image.
Allume la lumière  Éteindre la lumière




 4.  Utilisation de innerHTML

<!DOCTYPE html>
<html>
<body>
<h2>My First Web Page</h2>
<p>My First Paragraph.</p>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
</body>
</html> 
Ma première page Web
Mon premier paragraphe.
11


 5.  La déclaration JavaScript Switch
<!DOCTYPE html>
<html> <body>
<p id="demo"></p>
<script>
var day;
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case  6:
    day = "Saturday";
} document.getElementById("demo").innerHTML = "Today is " + day;
</script> </body>
</html>

Aujourd'hui, c'est mardi


JS Versions
Formulaires JS
Objets JavaScript


 6.  JavaScript peut valider une entrée numérique
<html>
<body>
<h2>JavaScript Can Validate Input</h2>
<p>Please input a number between 1 and 10:</p>
<input id="numb">
<button type="button" onclick="myFunction()">Submit</button>
<p id="demo"></p>
<script>
function myFunction() {
  var x, text;
  // Get the value of the input field with id="numb"
  x = document.getElementById("numb").value;
  // If x is Not a Number or less than one or greater than 10
  if (isNaN(x) || x < 1 || x > 10) {
    text = "Input not valid";
  } else {
    text = "Input OK";
  }   document.getElementById("demo").innerHTML = text;
} </script>
</body>
</html> 

JavaScript peut valider l'entrée
Veuillez saisir un nombre entre 1 et 10:
 Nous faire parvenir


Fonctions JS

 7.  Fermetures JavaScript
<!DOCTYPE html>
<html>
<body>
<p>A function can access variables defined inside the function:</p>
<button type="button" onclick="myFunction()">Click Me!</button>
<p id="demo"></p>
<script>
function myFunction() {
  var a = 4;
  document.getElementById("demo").innerHTML = a * a;
}  </script>
</body>
</html>
Une fonction peut accéder aux variables définies à l'intérieur de la fonction :
   Cliquez sur moi !

Classes JS
JS Async

 8.  JavaScript asynchrone
<html>
<body>
<h2>JavaScript setInterval()</h2>
<p>Using setInterval() to display the time every second (1000 milliseconds).</p>
<h1 id="demo"></h1>
<script>
setInterval(myFunction, 1000);
function myFunction() {
  let d = new Date();
  document.getElementById("demo").innerHTML=
  d.getHours() + ":" +
  d.getMinutes() + ":" +
  d.getSeconds();
} </script>
</body>
</html>
JavaScript setInterval ()
Utilisation de setInterval () pour afficher l'heure toutes les secondes (1000 millisecondes).
11:23:13

  9. DOM HTML JS
<!DOCTYPE html>
<html>
<body> <script>
document.write(Date());
</script> </body>
</html> 

Mer 17 Fév 2021 11:58:58 GMT + 0100 (heure normale d'Europe centrale)


  10. JavaScript HTML DOM EventListener
<html> <head>
<style>
#myDIV {
  background-color: coral;
  border: 1px solid;
  padding: 50px;
  color: white;
  font-size: 20px;
} </style>
</head> <body>
<h2>JavaScript removeEventListener()</h2>
<div id="myDIV">
  <p>This div element has an onmousemove event handler that displays a random number every time you move your mouse inside this orange field.</p>
  <p>Click the button to remove the div's event handler.</p>
  <button onclick="removeHandler()" id="myBtn">Remove</button>
</div> <p id="demo"></p>
<script>
document.getElementById("myDIV").addEventListener("mousemove", myFunction);
function myFunction() {
  document.getElementById("demo").innerHTML = Math.random();
} function removeHandler() {
  document.getElementById("myDIV").removeEventListener("mousemove", myFunction);
} </script> </body>
</html>
JavaScript removeEventListener ()
Cet élément div a un gestionnaire d'événements onmousemove qui affiche un nombre aléatoire à chaque fois que vous déplacez votre souris dans ce champ orange.
Cliquez sur le bouton pour supprimer le gestionnaire d'événements du div.
Supprimer


  11. Chronométrage JS
<html> <body>
<p>A script on this page starts this clock:</p>
<p id="demo"></p> <script>
var myVar = setInterval(myTimer, 1000);
function myTimer() {
  var d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
} </script>
</body> </html>
Un script sur cette page démarré cette horloge:
15:45:54

JS AJAX

  12. Exemple XML AJAX
<!DOCTYPE html>
<html> <style>
table,th,td {
  border : 1px solid black;
  border-collapse: collapse;
} th,td {
  padding: 5px;
} </style>
<body>
<h2>The XMLHttpRequest Object</h2>
<button type="button" onclick="loadDoc()">Get my CD collection</button>
<br><br>
<table id="demo"></table>
<script> function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      myFunction(this);
    }  };
  xhttp.open("GET", "cd_catalog.xml", true);
  xhttp.send();
} function myFunction(xml) {
  var i;  var xmlDoc = xml.responseXML;
  var table="<tr><th>Artist</th><th>Title</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i <x.length; i++) { 
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }  document.getElementById("demo").innerHTML = table;
} </script> </body> </html>

L'objet XMLHttpRequest
Obtenez ma collection de CD

Artist
Title
Bob Dylan
Empire Burlesque
Bonnie Tyler
Hide your heart
Dolly Parton
Greatest Hits
Gary Moore
Still got the blues
Eros Ramazzotti
Eros
Bee Gees
One night only
Dr.Hook
Sylvias Mother
Rod Stewart
Maggie May
Andrea Bocelli
Romanza
Percy Sledge
When a man loves a woman
Savage Rose
Black angel
Many
1999 Grammy Nominees
Kenny Rogers
For the good times
Will Smith
Big Willie style
Van Morrison
Tupelo Honey
Jorn Hoel
Soulsville
Cat Stevens
The very best of
Sam Brown
Stop
T'Pau
Bridge of Spies
Tina Turner
Private Dancer
Kim Larsen
Midt om natten
Luciano Pavarotti
Pavarotti Gala Concert
Otis Redding
The dock of the bay
Simply Red
Picture book
The Communards
Red
Joe Cocker
Unchain my heart


  13. JS contre jQuery
<!DOCTYPE html>
<html> <body>
<p id="demo">JavaScript can change the style of an HTML element.</p>
<script>
var myElement = document.getElementById("demo");
myElement.style.fontSize = "35px";
</script> </body>
</html>
JavaScript peut changer le style d'un élément HTML.
