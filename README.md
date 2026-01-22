# 2nd
<!DOCTYPE html>
<html>
<head>
  <title>Catch the Box</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #111;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-family: Arial;
    }
    #box {
      width: 60px;
      height: 60px;
      background: red;
      position: absolute;
      cursor: pointer;
    }
    #score {
      position: fixed;
      top: 10px;
      left: 10px;
      font-size: 20px;
    }
  </style>
</head>
<body>

<div id="score">Score: 0</div>
<div id="box"></div>

<script>
  const box = document.getElementById("box");
  const scoreText = document.getElementById("score");
  let score = 0;

  function moveBox() {
    const x = Math.random() * (window.innerWidth - 60);
    const y = Math.random() * (window.innerHeight - 60);
    box.style.left = x + "px";
    box.style.top = y + "px";
  }

  box.onclick = () => {
    score++;
    scoreText.innerText = "Score: " + score;
    moveBox();
  };

  moveBox();
</script>

</body>
</html>
