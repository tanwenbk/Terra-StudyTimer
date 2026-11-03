JS:
var redslider = document.getElementById("red")
var greenslider = document.getElementById("green")
var blueslider = document.getElementById("blue")
var redval = document.getElementById("redval")
var greenval = document.getElementById("greenval")

let box = document.getElementById("box")

function changebg() {
    redval.textContent = redslider.value
    greenval.textContent = greenslider.value
    blueval.textContent = blueslider.value

    box.style.backgroundColor =
        "rgb(" + redslider.value + ", " + greenslider.value + ", " + blueslider.value + ")"
}

changebg()
redslider.addEventListener("input", changebg)
greenslider.addEventListener("input", changebg)
blueslider.addEventListener("input", changebg)


console.log("hi")
console.log(redval)

CSS: 


.slidecontainer {
    width: 100%;
}

/* Slider code from w3schools https://www.w3schools.com/howto/howto_js_rangeslider.asp */
/* The slider itself */
.slider {
  -webkit-appearance: none;  /* Override default CSS styles */
  appearance: none;
  width: 20%;
  height: 25px; /* Specified height */
  background: #d3d3d3; /* Grey background */
  outline: none; /* Remove outline */
  opacity: 0.7; /* Set transparency (for mouse-over effects on hover) */
  -webkit-transition: .2s; /* 0.2 seconds transition on hover */
  transition: opacity .2s;
}

/* Mouse-over effects */
.slider:hover {
  opacity: 1; /* Fully shown on mouse-over */
}

/* The slider handle (use -webkit- (Chrome, Opera, Safari, Edge) and -moz- (Firefox) to override default look) */
.slider::-webkit-slider-thumb {
  -webkit-appearance: none; /* Override default look */
  appearance: none;
  width: 25px; /* Set a specific slider handle width */
  height: 25px; /* Slider handle height */
  background: #04AA6D; /* Green background */
  cursor: pointer; /* Cursor on hover */
}

.slider::-moz-range-thumb {
  width: 25px; /* Set a specific slider handle width */
  height: 25px; /* Slider handle height */
  background: #04AA6D; /* Green background */
  cursor: pointer; /* Cursor on hover */
}

HTML:
<!DOCTYPE html>
<html>
    <head>
        <link rel = "stylesheet" href = "styling.css">
    </head>
    <body>
        <script src = "studytimer.js" defer></script>
        <p>hi</p>
        <div class="slidecontainer">
            <input type="range" min="1" max="255" value="255" class="slider" id="red">
            <p>Red: <span id = "redval"></span></p>
            <input type="range" min="1" max="255" value="155" class="slider" id="green"><br>
            <p>Green: <span id = "greenval"></span></p>
            <input type="range" min="1" max="255" value="155" class="slider" id="blue"><br>
            <p>Blue: <span id = "blueval"></span></p>
        </div>
        <div id = "box" style = "height: 100vh;"></div>
    </body>
</html>
