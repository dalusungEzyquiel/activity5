<!DOCTYPE html>
<html lang="en">
<head>
<title>Rectangle and Square</title>
<style>
  * { box-sizing: border-box; }

  body {
    margin: 0;
    min-height: 100vh;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background: #ffffff;
    font-family: "Segoe UI", system-ui, sans-serif;
  }

  button {
    border: none;
    color: #fff;
    font-size: 0.9rem;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.25s ease, transform 0.25s ease;
  }

  /* Rectangle: tilts and turns orange only while the cursor is on it */
  .rectangle {
    width: 160px;
    height: 56px;
    border-radius: 4px;
    background: #14b8a6;
  }
  .rectangle:hover {
    background: #f97316;
    transform: rotate(-10deg);
  }

  /* Square: always bobs up and down, turns purple only while the cursor is on it */
  .square {
    width: 64px;
    height: 64px;
    border-radius: 6px;
    background: #ef1c36;
    animation: bob 1.2s ease-in-out infinite;
  }
  .square:hover {
    background: #8b5cf6;
  }
  @keyframes bob {
    0%, 100% { transform: translateY(0); }
    50%      { transform: translateY(-10px); }
  }

  footer {
    position: fixed;
    bottom: 12px;
    width: 100%;
    text-align: center;
    font-size: 0.8rem;
    color: #555;
  }
</style>
</head>
<body>
  <button class="rectangle">Rectangle</button>
  <button class="square">Square</button>
  <footer>Credits by Ezyquiel Dalusung</footer>
</body>
</html>