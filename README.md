# Coming-Soon-Page

## HTML

<!DOCTYPE HTML>
<html>
    <head>
        <link href="style.css" rel="stylesheet" type="text/css">
      </head>
    
<body>
    <header>
	<div class="Tech">
	    <h1> SOMETHING EXCITING IS COMING AT YOUR DOOR STEPS </h1>
        <hr>
	    <h2>COMING  SOON</h2>
		
		<hr>
		
		<p id="Release"></p>
    </div>
    </header>
</body>
</html>

## CSS
#### Style.css

*{
    margin: 0px;
    padding: 0;
}
  
header{
    background-color: #dea5a4;
    background-position: center;
    background-size: 50%;
    height: 100vh;
}
  
.Tech{
    top: 50%;
    left: 50%;
    position: absolute;
    transform: translate(-50%, -50%);
    color: rgb(20, 158, 212);
    text-align: center;
    font-size: 20px;
    
}
  
h1{
    color: rgb(16, 145, 219); 
    font-size: 40px;
    letter-spacing: 16px;
}
  
hr{
    width: 90%;
    margin: 30px auto;
    border: 3px solid rgb(17, 17, 15);
}
  
p{
    font-size: 20px;
    margin-bottom: 30px;
}
  
#Release{
    color:rgb(209, 34, 34);
    font-size: 70px;
    word-spacing: 20px;
}

## JAVASCRIPT
## page.js

    var RemainingTime = new Date("Feb 17, 2022 00:00:00");
    var RemainingTime = RemainingTime.getTime();
    var x = setInterval(function() {
        var now = new Date().getTime();
        var distance = RemainingTime - now;
      
var din = Math.floor(distance / (1000 * 60 * 60 * 24));
var ghnte = Math.floor(din / (1000 * 60 * 60));
var x1 = distance % (1000 * 60 * 60);
var minutes = Math.floor(x1 / (1000 * 60));
var x2 = distance % (1000 * 60);
var seconds = Math.floor(x2 / 1000);

  document.getElementById("Release").innerHTML = din + " : " + ghnte + " : " + minutes + " : " + seconds;

  if (distance < 0) {
      clearinterval(x);
      document.getElementById("Release").innerHTML = "EXPIRED";
    }
    
}, 1000);
