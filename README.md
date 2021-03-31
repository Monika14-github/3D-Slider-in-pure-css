# 3D-Slider-in-pure-css
.....html......
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <section id="slider">
  <input type="radio" name="slider" id="s1">
  <input type="radio" name="slider" id="s2">
  <input type="radio" name="slider" id="s3" checked>
  <input type="radio" name="slider" id="s4">
  <input type="radio" name="slider" id="s5">
  <label for="s1" id="slide1"></label>
  <label for="s2" id="slide2"></label>
  <label for="s3" id="slide3"></label>
  <label for="s4" id="slide4"></label>
  <label for="s5" id="slide5"></label>
</section>
</body>
    
</html>
......css.......
* {
  margin: 0;
  padding: 0;
}

body {
  padding: 20px;
  background: #eee;
  user-select: none;
}

[type=radio] {
  display: none;
}

#slider {
  height: 35vw;
  position: relative;
  perspective: 1000px;
  transform-style: preserve-3d;
}

#slider label {
  margin: auto;
  width: 60%;
  height: 100%;
  border-radius: 4px;
  position: absolute;
  left: 0; right: 0;
  cursor: pointer;
  transition: transform 0.4s ease;
}

#s1:checked ~ #slide4, #s2:checked ~ #slide5,
#s3:checked ~ #slide1, #s4:checked ~ #slide2,
#s5:checked ~ #slide3 {
  box-shadow: 0 1px 4px 0 rgba(0,0,0,.37);
  transform: translate3d(-30%,0,-200px);
}

#s1:checked ~ #slide5, #s2:checked ~ #slide1,
#s3:checked ~ #slide2, #s4:checked ~ #slide3,
#s5:checked ~ #slide4 {
  box-shadow: 0 6px 10px 0 rgba(0,0,0,.3), 0 2px 2px 0 rgba(0,0,0,.2);
  transform: translate3d(-15%,0,-100px);
}

#s1:checked ~ #slide1, #s2:checked ~ #slide2,
#s3:checked ~ #slide3, #s4:checked ~ #slide4,
#s5:checked ~ #slide5 {
  box-shadow: 0 13px 25px 0 rgba(0,0,0,.3), 0 11px 7px 0 rgba(0,0,0,.19);
  transform: translate3d(0,0,0);
}

#s1:checked ~ #slide2, #s2:checked ~ #slide3,
#s3:checked ~ #slide4, #s4:checked ~ #slide5,
#s5:checked ~ #slide1 {
  box-shadow: 0 6px 10px 0 rgba(0,0,0,.3), 0 2px 2px 0 rgba(0,0,0,.2);
  transform: translate3d(15%,0,-100px);
}

#s1:checked ~ #slide3, #s2:checked ~ #slide4,
#s3:checked ~ #slide5, #s4:checked ~ #slide1,
#s5:checked ~ #slide2 {
  box-shadow: 0 1px 4px 0 rgba(0,0,0,.37);
  transform: translate3d(30%,0,-200px);
}

#slide1 { background:  rgb(26, 22, 241)}
#slide2 { background: rgb(250, 253, 30) }
#slide3 { background: rgb(207, 12, 181) }
#slide4 { background: rgb(17, 235, 243) }
#slide5 { background: rgb(65, 7, 39) }
