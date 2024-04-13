<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Heart Effect</title>
<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
  }

  .heart {
    width: 100px;
    height: 90px;
    position: relative;
    animation: beat 1s infinite alternate;
  }

  .heart::before,
  .heart::after {
    content: '';
    width: 50px;
    height: 80px;
    background-color: red;
    border-radius: 50px 50px 0 0;
    position: absolute;
    top: -45px;
    left: 50px;
    transform: rotate(-45deg);
    transform-origin: 0 100%;
  }

  .heart::after {
    left: 0;
    transform: rotate(45deg);
    transform-origin: 100% 100%;
  }

  @keyframes beat {
    0% {
      transform: scale(1) rotate(0);
    }
    100% {
      transform: scale(1.1) rotate(0);
    }
  }

  .message {
    font-size: 24px;
    text-align: center;
    margin-top: 20px;
  }
</style>
</head>
<body>
<div class="heart"></div>
<div class="message">Happy 4th Monthsary Babe, I love you</div>
</body>
</html>
