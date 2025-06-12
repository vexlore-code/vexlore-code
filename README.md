<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vexlore - Animated Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css" />
  <style>
    body {
      margin: 0;
      font-family: 'Fira Code', monospace;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow-x: hidden;
    }

    .container {
      text-align: center;
      padding: 2rem;
      animation: fadeIn 2s ease;
    }

    .wave {
      animation: waveAnim 2s infinite;
      display: inline-block;
      transform-origin: 70% 70%;
    }

    .highlight {
      color: #00adb5;
    }

    .typing {
      border-right: 2px solid #fff;
      font-size: 1.2rem;
      width: 22ch;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 4s steps(22), blink .75s step-end infinite;
      margin: 1rem auto;
    }

    .terminal {
      text-align: left;
      background-color: #111;
      padding: 1rem 1.5rem;
      margin: 2rem auto;
      max-width: 600px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0, 173, 181, 0.5);
    }

    .terminal .cmd {
      color: #00adb5;
    }

    .btn {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.75rem 1.5rem;
      background-color: #00adb5;
      color: #fff;
      text-decoration: none;
      border-radius: 8px;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 5px 15px rgba(0, 173, 181, 0.4);
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 22ch }
    }

    @keyframes blink {
      50% { border-color: transparent }
    }

    @keyframes waveAnim {
      0% { transform: rotate(0.0deg) }
      10% { transform: rotate(14deg) }
      20% { transform: rotate(-8deg) }
      30% { transform: rotate(14deg) }
      40% { transform: rotate(-4deg) }
      50% { transform: rotate(10deg) }
      60% { transform: rotate(0.0deg) }
      100% { transform: rotate(0.0deg) }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1><span class="wave">👋</span> I'm <span class="highlight">Jubayer Hasan Munna</span></h1>
    <h2 class="typing">Flutter Developer | C++ Craftsman | Linux Lover</h2>

    <div class="terminal">
      <pre>
$ <span class="cmd">whoami</span>
vexlore-code

$ <span class="cmd">skills --list</span>
C++, Flutter, Dart, Linux, Git, Python, Blender

$ <span class="cmd">contact --email</span>
jubiofficial.dev@gmail.com
      </pre>
    </div>

    <a href="https://github.com/vexlore-code" class="btn">Visit My GitHub</a>
  </div>

  <script>
    // Example subtle animation script (optional)
    document.querySelector('.btn').addEventListener('mouseenter', () => {
      document.body.style.background = 'linear-gradient(135deg, #1a2a3a, #2d4e5f, #3f6a84)';
    });
    document.querySelector('.btn').addEventListener('mouseleave', () => {
      document.body.style.background = 'linear-gradient(135deg, #0f2027, #203a43, #2c5364)';
    });
  </script>
</body>
</html>
