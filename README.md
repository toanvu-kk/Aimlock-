# Aimlock-
Crt
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Menu Free Fire - 8 Chức Năng</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #1c1c1c;
      color: #fff;
      text-align: center;
      padding-top: 80px;
    }
    .box {
      background-color: #2b2b2b;
      border-radius: 10px;
      padding: 25px;
      width: 350px;
      margin: auto;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }
    input[type="text"], input[type="password"] {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 6px;
    }
    button {
      background-color: #00cc66;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 10px;
      font-weight: bold;
    }
    .menu-item {
      background-color: #383838;
      padding: 12px;
      border-radius: 6px;
      margin: 10px 0;
      cursor: pointer;
      transition: 0.3s;
    }
    .menu-item:hover {
      background-color: #00cc66;
    }
    .status {
      font-weight: bold;
      color: #00ff99;
    }
  </style>
</head>
<body>

<div class="box" id="loginBox">
  <h2>ĐĂNG NHẬP MENU</h2>
  <input type="text" id="username" placeholder="Tài khoản">
  <input type="password" id="password" placeholder="Mật khẩu">
  <br>
  <button onclick="login()">Đăng nhập</button>
</div>

<div class="box" id="menuBox" style="display:none;">
  <h2>🎮 MENU FREE FIRE</h2>
  <div class="menu-item" onclick="toggle(this)">🔫 Headshot</div>
  <div class="menu-item" onclick="toggle(this)">🎯 Aimlock</div>
  <div class="menu-item" onclick="toggle(this)">🛡️ Anti Lag</div>
  <div class="menu-item" onclick="toggle(this)">📶 Tăng FPS</div>
  <div class="menu-item" onclick="toggle(this)">🎚️ Fix Rung Tâm</div>
  <div class="menu-item" onclick="toggle(this)">🎮 Mode PC Panel</div>
  <div class="menu-item" onclick="toggle(this)">🎯 Tăng FOV</div>
  <div class="menu-item" onclick="toggle(this)">⚙️ Reset Config</div>
  <br>
  <p class="status">Tất cả chức năng có thể bật/tắt</p>
  <button onclick="logout()">Đăng xuất</button>
</div>

<script>
  function login() {
    const u = document.getElementById('username').value;
    const p = document.getElementById('password').value;
    if (u === "admin" && p === "123456") {
      document.getElementById('loginBox').style.display = "none";
      document.getElementById('menuBox').style.display = "block";
    } else {
      alert("Sai tài khoản hoặc mật khẩu!");
    }
  }

  function logout() {
    document.getElementById('menuBox').style.display = "none";
    document.getElementById('loginBox').style.display = "block";
  }

  function toggle(element) {
    if (element.style.backgroundColor === "rgb(0, 204, 102)") {
      element.style.backgroundColor = "#383838";
      element.innerHTML = element.innerHTML.replace("✅ ", "");
    } else {
      element.style.backgroundColor = "#00cc66";
      element.innerHTML = "✅ " + element.innerHTML;
    }
  }
</script>

</body>
</html>
