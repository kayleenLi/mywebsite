<!DOCTYPE html><html> <head>  <meta charset="UTF-8">  <title></title>  <style type="text/css">   .clock{    width: 200px;    height: 200px;    border: 4px solid #000;    margin: 40px auto;    border-radius: 50%;    position: relative;   }   .clock > div{    position: absolute;    transform-origin: bottom center;   }   .hour{    width: 8px;    height: 40px;    background-color: darkviolet;    left: 96px;    top: 60px;   }   .minutes{    width: 6px;    height: 60px;    background-color: deeppink;    left: 97px;    top: 40px;   }   .second{    width: 4px;    height: 80px;    background-color: blue;    left: 98px;    top: 20px;   }   .round{    width: 6px;    height: 6px;    background-color: cornflowerblue;    border-radius: 50%;    left: 97px;    top: 97px;   }     </style> </head> <body>  <div class="clock">   <div class="hour"></div>   <div class="minutes"></div>   <div class="second"></div>   <div class="round"></div>  </div>  <script type="text/javascript">   var hour=document.querySelector('.hour');   var minutes=document.querySelector('.minute');   var second=document.querySelector('.second');      setInterval(function(){    var date=new Date();    var h=date.getHours()%12;    var m=date.getMinutes();    var s=date.getSeconds();    var milliseconds=date.getMilliseconds();    hour.style.transform=`rotate(${(h+m/60)/12*360}deg)`;    minutes.style.transform=`rotate(${(m+s/60)/60*360}deg)`;    second.style.transform=`rotate(${(s+milliseconds/1000)/60*360}deg)`;       },16);  </script> </body></html>
