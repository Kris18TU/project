<!DOCTYPE html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Cute Monster</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <div class="monster">
        <div class="eye"></div>
        <div class="details"></div>
        <div class="mouth">
          <div class="teeth"></div>
        </div>
        <div class="hand-l"></div>
        <div class="hand-r"></div>
        <div class="leg"></div>
      </div>
    </div>
  </body>
</html>A

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  background-color: #f4c600;
}
.container {
  height: 31.25em;
  width: 31.25em;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
}
.monster {
  height: 18.75em;
  width: 15.62em;
  background-color: #b66750;
  border-radius: 3.75em 3.75em 1.87em 1.87em;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
}
.monster:before,
.monster:after {
  position: absolute;
  content: "";
  height: 3.75em;
  width: 1.25em;
  background-color: #b66750;
  border-radius: 0.62em;
}
.monster:before {
  top: -2.5em;
  left: 6.56em;
  transform: rotate(-15deg);
}
.monster:after {
  top: -1.56em;
  right: 6.56em;
  transform: rotate(15deg);
}
.eye,
.eye:before {
  position: absolute;
  height: 0.62em;
  width: 0.62em;
  background-color: #ffffff;
  border-radius: 50%;
  box-shadow: 0.18em 0.18em 0 0.5em #000000;
}
.eye {
  top: 4.37em;
  left: 3.75em;
}
.eye:before {
  content: "";
  left: 6.87em;
}
.eye:after {
  position: absolute;
  content: "";
  height: 1.56em;
  width: 1.56em;
  background-color: #d0865d;
  border-radius: 50%;
  top: 1.25em;
  left: -1.87em;
  box-shadow: 10em 0 #d0865d;
}
.details {
  background-color: #a85d46;
  height: 0.62em;
  width: 3.75em;
  position: absolute;
  transform: translateX(-50%);
  left: 50%;
  top: 5.62em;
  border-radius: 0.62em;
}
.details:before {
  position: absolute;
  content: "";
  background-color: #a85d46;
  height: 1.56em;
  width: 0.43em;
  top: 8.75em;
  left: -1.56em;
  border-radius: 0.31em;
  box-shadow: 1.56em 1.56em #a85d46, 1.56em -1.56em #a85d46, 3.12em 0 #a85d46,
    4.68em 1.56em #a85d46, 4.68em -1.56em #a85d46, 6.25em 0 #a85d46;
}
.mouth {
  position: absolute;
  background-color: #a8193f;
  height: 5em;
  width: 7.5em;
  top: 3.12em;
  left: 3.9em;
  top: 6.87em;
  border-radius: 0.93em;
  overflow: hidden;
}
.mouth:before {
  position: absolute;
  content: "";
  height: 2.5em;
  width: 100%;
  background-color: #d9394e;
  border-radius: 2.5em 2.5em 0 0;
  bottom: 0;
}
.teeth {
  position: absolute;
  height: 2em;
  width: 120%;
  background: linear-gradient(
      -45deg,
      #ffffff 1.25em,
      #ffffff 1.25em,
      #ffffff 1.25em,
      transparent 0
    ),
    linear-gradient(45deg, #ffffff 1.25em, transparent 0);
  background-position: left top;
  background-repeat: repeat-x;
  background-size: 2em 2em;
  left: -0.31em;
  bottom: 0;
}
.teeth:after {
  content: "";
  position: absolute;
  height: 2em;
  width: 120%;
  background: linear-gradient(-45deg, transparent 1.25em, #ffffff 0),
    linear-gradient(45deg, transparent 1.25em, #ffffff 0);
  background-repeat: repeat-x;
  background-position: left bottom;
  background-size: 1.75em 2em;
  top: -3.12em;
  left: -0.31em;
}
.hand-l {
  position: absolute;
  height: 9.37em;
  width: 3.75em;
  background-color: #b66750;
  transform: rotate(-60deg);
  transform-origin: 50% 100%;
  border-radius: 1.87em;
  left: 0.62em;
  z-index: -1;
  animation: wave 3s infinite;
}
@keyframes wave {
  50% {
    transform: rotate(-120deg);
  }
}
.hand-l:before {
  position: absolute;
  content: "";
  height: 1.25em;
  width: 1.25em;
  background-color: #b66750;
  border-radius: 50%;
  bottom: 6.25em;
  left: 3.43em;
}
.hand-r {
  height: 9.37em;
  width: 3.75em;
  background-color: #b66750;
  position: absolute;
  border-radius: 1.25em;
  right: -2.81em;
  top: 8.75em;
  transform-origin: 0 50%;
  transform: rotate(-40deg);
}
.leg {
  position: absolute;
  height: 4.37em;
  width: 3.75em;
  background-color: #b66750;
  bottom: -4.37em;
  left: 2.18em;
  border-radius: 0 0 2.5em 2.5em;
  box-shadow: 7.5em 0 #b66750;
}
