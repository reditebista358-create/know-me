<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Redite's Cute Site</title>

<style>
  body {
    background-color: #fce4ec;
    font-family: "Courier New", monospace;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    text-align: center;
  }

  h1 {
    font-size: 2em;
    margin-top: 50px;
    animation: pop 1s ease-in-out infinite alternate;
    color: #ff4081;
    text-shadow: 2px 2px white;
  }

  @keyframes pop {
    0% { transform: scale(1); }
    100% { transform: scale(1.2); }
  }

  .socials {
    position: fixed;
    bottom: 15px;
    left: 0;
    right: 0;
    display: flex;
    justify-content: center;
    gap: 15px;
  }

  .socials a img {
    width: 40px;
    height: 40px;
    transition: transform 0.3s;
  }

  .socials a img:hover {
    transform: scale(1.2);
  }

  .hello-kitty {
    position: absolute;
    width: 60px;
    height: 60px;
    pointer-events: none;
    animation: fadeOut 3s forwards;
  }

  @keyframes fadeOut {
    0% { opacity: 1; transform: scale(1); }
    100% { opacity: 0; transform: scale(0.5); }
  }

  p {
    margin-top: 10px;
    color: #880e4f;
    font-size: 1em;
    padding: 0 10px;
  }
</style>
</head>

<body>
  <h1>Welcome!</h1>
  <p>Hello, my name is Redite and these are my socials:</p>

  <!-- Social Links -->
  <div class="socials">
    <a href="https://www.facebook.com/reditebista1" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733547.png"></a>
    <a href="https://www.instagram.com/reditebista11/" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733558.png"></a>
    <a href="https://www.tiktok.com/@reditebista" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/3046/3046121.png"></a>
    <a href="https://www.youtube.com/@reditebista4788" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/1384/1384060.png"></a>
  </div>

<script>
  const kittyImgs = [
    "<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/8c7317c8-4e89-41e9-bd26-486172a5b129" />
",
    "<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/13017a41-a91c-40b8-b28b-6f0ded7a8bb7" />
",
    "<img width="278" height="181" alt="image" src="https://github.com/user-attachments/assets/4405acfa-b59e-4fbc-87aa-9a69823e6596" />
"
  ];

  function spawnKitty() {
    const img = document.createElement("img");
    img.src = kittyImgs[Math.floor(Math.random() * kittyImgs.length)];
    img.className = "hello-kitty";
    img.style.top = Math.random() * window.innerHeight + "px";
    img.style.left = Math.random() * window.innerWidth + "px";
    document.body.appendChild(img);

    setTimeout(() => {
      img.remove();
    }, 3000);
  }

  setInterval(spawnKitty, 2000);
</script>
</body>
</html>
