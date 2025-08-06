# Academy-Showdown-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Login | Academy Showdown</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #e6f2ff, #cce0ff);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-box {
      background-color: white;
      padding: 40px 30px;
      border-radius: 12px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.2);
      text-align: center;
      width: 100%;
      max-width: 350px;
    }

    .login-box h2 {
      margin-bottom: 25px;
      color: #0077cc;
    }

    .login-box input[type="text"],
    .login-box input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }

    .login-box button {
      width: 100%;
      padding: 12px;
      background-color: #0077cc;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 10px;
    }

    .login-box button:hover {
      background-color: #005fa3;
    }

    .status-message {
      margin-top: 15px;
      font-size: 14px;
      color: red;
    }

    .footer {
      margin-top: 20px;
      font-size: 13px;
      color: #888;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>🔐 Academy Showdown</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Username" required />
      <input type="password" id="password" placeholder="Password" required />
      <button type="submit">Login</button>
      <div id="status" class="status-message"></div>
    </form>
    <div class="footer">Founded by Abhishek 🇮🇳</div>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function(e) {
      e.preventDefault();

      const username = document.getElementById("username").value.trim();
      const password = document.getElementById("password").value.trim();
      const status = document.getElementById("status");

      // Example credentials — change later for real login
      const validUsername = "admin";
      const validPassword = "1234";

      if (username === validUsername && password === validPassword) {
        status.style.color = "green";
        status.textContent = "Login successful! Redirecting...";
        setTimeout(() => {
          window.location.href = "index.html"; // Change to your homepage
        }, 1000);
      } else {
        status.style.color = "red";
        status.textContent = "Invalid username or password.";
      }
    });
  </script>
</body>
</html>
