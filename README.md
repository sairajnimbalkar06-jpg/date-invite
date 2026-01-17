# date-invite
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Sairaj's Special Invite 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      text-align: center;
      width: 320px;
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 10px;
    }

    p {
      color: #555;
      margin-bottom: 20px;
    }

    button {
      padding: 12px 24px;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.2s;
    }

    .yes-btn {
      background-color: #ff4d6d;
      color: white;
      margin-right: 10px;
    }

    .no-btn {
      background-color: #ccc;
      color: black;
      position: absolute;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <div class="card" id="slide1">
    <h1>Will you go on a date with me? 💕</h1>
    <p>— From Sairaj 💌</p>
    <button class="yes-btn" onclick="showCongrats()">Yes 😍</button>
    <button class="no-btn" id="noBtn">No 😅</button>
  </div>

  <div class="card hidden" id="slide2">
    <h1>Congratulations! 🎉</h1>
    <p>You’ll be updated soon 💖</p>
    <p>— Sairaj</p>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const slide1 = document.getElementById("slide1");
    const slide2 = document.getElementById("slide2");

    noBtn.addEventListener("mouseover", moveNoButton);
    noBtn.addEventListener("click", moveNoButton);

    function moveNoButton() {
      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;

      const randomX = Math.random() * maxX;
      const randomY = Math.random() * maxY;

      noBtn.style.left = randomX + "px";
      noBtn.style.top = randomY + "px";
    }

    function showCongrats() {
      slide1.classList.add("hidden");
      slide2.classList.remove("hidden");
    }
  </script>

</body>

</html>
