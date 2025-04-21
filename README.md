<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Undangan Nongki Rock</title>
  <link href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Rock Salt', cursive;
      background-color: #1f1f1f;
      color: #fff;
      text-align: center;
      padding: 50px 0;
      background-image: url('https://www.transparenttextures.com/patterns/dark-wood.png');
      background-size: cover;
    }

    .container {
      max-width: 800px;
      margin: auto;
      padding: 30px;
      background-color: rgba(0, 0, 0, 0.7);
      border-radius: 10px;
      border: 2px solid #ff4500;
    }

    .header {
      background-color: #ff4500;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(255, 69, 0, 0.7);
    }

    .header h1 {
      font-size: 3em;
      color: white;
      letter-spacing: 5px;
      text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.8);
    }

    .menu {
      display: flex;
      justify-content: center;
      margin-top: 30px;
    }

    .menu a {
      padding: 12px 25px;
      margin: 0 20px;
      background-color: #ff4500;
      color: white;
      text-decoration: none;
      font-size: 1.3em;
      border-radius: 5px;
      border: 2px solid #ff0000;
      box-shadow: 0 4px 8px rgba(255, 0, 0, 0.7);
      transition: background 0.3s ease;
    }

    .menu a:hover {
      background-color: #ff0000;
      transform: scale(1.1);
    }

    .tab-content {
      margin-top: 30px;
      display: none;
    }

    .tab-content.active {
      display: block;
    }

    .tab-content h2 {
      font-size: 2em;
      margin-bottom: 20px;
      color: #ff4500;
      text-shadow: 1px 1px 5px black;
    }

    .tab-content p {
      font-size: 1.3em;
      margin-bottom: 30px;
      line-height: 1.8;
    }

    .galeri-foto {
      width: 100%;
      max-width: 500px;
      border-radius: 10px;
      border: 4px solid #ff4500;
      margin-bottom: 25px;
      box-shadow: 0 4px 10px rgba(255, 69, 0, 0.6);
    }

    footer {
      margin-top: 60px;
      font-size: 1.1em;
      color: white;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <h1>Undangan Nongki</h1>
      <p>cus lah ke bengs, ngopi</p>
    </div>

    <!-- Navigasi -->
    <div class="menu">
      <a href="#" class="tab-link" data-tab="event-details">Acara</a>
      <a href="#" class="tab-link" data-tab="gallery">Galeri</a>
      <a href="#" class="tab-link" data-tab="rsvp">RSVP</a>
    </div>

    <!-- Halaman Acara -->
    <div id="event-details" class="tab-content active">
      <h2>Tempat & Waktu</h2>
      <p>Sekarang<br>Pukul 24 jam WIB<br>Di belakang, Jalan masjid 1</p>
    </div>

    <!-- Galeri -->
    <div id="gallery" class="tab-content">
      <h2>Galeri Foto</h2>
      <p>bengkel</p>
      <img src="https://i.imgur.com/9PjflUS.jpg" alt="Foto Galeri" class="galeri-foto">
    </div>

    <!-- RSVP -->
    <div id="rsvp" class="tab-content">
      <h2>RSVP</h2>
      <p>Konfirmasi kehadiran kamu di bawah ini:</p>
      <a href="https://wa.me/628558156566" class="btn">Klik untuk mengirim RSVP via WhatsApp</a>
    </div>
  </div>

  <footer>
    <p>&copy; Nongki Gauls cunay| by QIIHY </p>
  </footer>

  <script>
    const links = document.querySelectorAll('.tab-link');
    const tabContents = document.querySelectorAll('.tab-content');

    links.forEach(link => {
      link.addEventListener('click', function(e) {
        e.preventDefault();
        const tabName = this.getAttribute('data-tab');

        tabContents.forEach(tab => tab.classList.remove('active'));
        links.forEach(link => link.classList.remove('active'));

        document.getElementById(tabName).classList.add('active');
        this.classList.add('active');
      });
    });
  </script>
</body>
</html>
