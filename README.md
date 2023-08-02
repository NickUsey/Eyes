# Eyes

<html>

<head>
    <link rel="stylesheet" type="text/css" href="./style.css">
</head>

<body>
    <div class="eyes">
        <div class="eye">
            <div class="ball"></div>
        </div>
        <div class="eye">
            <div class="ball"></div>
        </div>
    </div>
    
  <style>
        body {
          margin: 0;
          padding: 0;
          background: #14495e;
        }
        
        .eyes {
          position: absolute;
          top: 50%;
          transform: translateY(-50%);
          width: 100%;
          text-align: center;
        }
        .eye {
          width: 240px;
          height: 120px;
          background: #fff;
          display: inline-block;
          margin: 40px;
          border-radius: 50%;
          position: relative;
          overflow: hidden;
        }
        .ball {
          width: 80px;
          height: 80px;
          background: #000;
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
          border-radius: 50%;
        }
    </style>
</body>
<script>
    const balls = document.getElementsByClassName('ball');
document.onmousemove = (event) => {
  const x = (event.clientX * 100) / window.innerWidth + '%';
  const y = (event.clientY * 100) / window.innerHeight + '%';
for (let i = 0; i < 2; i++) {
    balls[i].style.left = x;
    balls[i].style.top = y;
    balls[i].transform = 'translate(-' + x + ',-' + y + ')';
  }
};
</script>

</html>
