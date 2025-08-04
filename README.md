# Untuk-pacarku
Selamat 7 bulan hubungan ini ya sayang
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy 7 Months of Dating</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #ffccd5, #ffe6eb);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #d6336c;
      text-align: center;
      overflow: hidden;
    }

    .container {
      position: relative;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
      z-index: 1;
    }

    h1 {
      font-size: 2.8em;
      margin-bottom: 10px;
      animation: fadeIn 2s ease-in-out;
    }

    p {
      font-size: 1.2em;
      max-width: 600px;
      margin: 10px auto 20px;
      animation: fadeIn 3s ease-in-out;
    }

    video {
      width: 90%;
      max-width: 600px;
      border-radius: 15px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.2);
      margin-top: 20px;
      outline: none;
    }

    .hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      overflow: hidden;
      pointer-events: none;
      z-index: 0;
    }

    .heart {
      position: absolute;
      color: #ff6b81;
      animation: float 6s linear forwards;
      will-change: transform, opacity;
      user-select: none;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) scale(0.5);
        opacity: 0;
      }
      20% {
        opacity: 1;
      }
      80% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2);
        opacity: 0;
      }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Selamat 7 Bulan hubungan ini, Cintaku 💖</h1>
    <p>
      Terima kasih telah menjadi bagian dari hidupku. Setiap detik bersamamu adalah berkah tak ternilai.<br>
      Semoga kita terus tumbuh bersama dalam cinta. I love you so much ❤️
    </p>
    <video id="Video" autoplay muted playsinline controls>
      <source src="Video.mp4" type="video/mp4"/>
      Maaf, browser Anda tidak mendukung pemutaran video.
    </video>
  </div>
  <div class="hearts"></div>
  <script>
    const heartsContainer = document.querySelector('.hearts');
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (Math.random() * 20 + 20) + "px";
      heart.style.top = "100vh";
      heart.innerHTML = Math.random() > 0.5 ? "❤️" : "🫶";
      heartsContainer.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 500);
  </script>
</body>
</html>
