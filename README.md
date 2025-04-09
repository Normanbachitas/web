# web
parecido a un virus famoso
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Mini Prank con Música</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background-color: black;
      color: white;
      font-family: sans-serif;
      text-align: center;
      padding-top: 2rem;
    }
    .emoji {
      position: absolute;
      animation: move 5s infinite linear;
      color: yellow;
    }
    @keyframes move {
      0%   { transform: translate(0, 0); }
      25%  { transform: translate(100vw, 0); }
      50%  { transform: translate(100vw, 100vh); }
      75%  { transform: translate(0, 100vh); }
      100% { transform: translate(0, 0); }
    }
    button {
      padding: 1rem 2rem;
      font-size: 1.2rem;
      border: none;
      background: #0f0;
      color: #000;
      border-radius: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>¿Te atreves? 😈</h1>
  <button onclick="startPrank()">Iniciar Prank</button>

  <audio id="prank-audio" loop>
    <source src="https://rr3---sn-n4v7snly.googlevideo.com/videoplayback?expire=1744177950&ei=vrb1Z8PdGJezlu8P4MjEmQo&ip=201.141.97.87&id=o-ANRp5Mm0X3pK0o0OTRblvZ6i2yUFo8Jtc3rVj5BGpvFm&itag=251&source=youtube&requiressl=yes&xpc=EgVo2aDSNQ%3D%3D&gcr=mx&bui=AccgBcOoUJ6rctRpRub2XiDmG1xLnpzhXjKyVBc2fgsXf2eenXwXz-SYfwnqs3gjL_KKVpX81a5hGD3r&vprv=1&svpuc=1&mime=audio%2Fwebm&ns=LxdhfNCaRES0QVvtkGZkKdkQ&rqh=1&gir=yes&clen=3018387&dur=198.761&lmt=1714681316163288&keepalive=yes&lmw=1&c=TVHTML5&sefc=1&txp=4502434&n=zLCtiUhMnBO_Dw&sparams=expire%2Cei%2Cip%2Cid%2Citag%2Csource%2Crequiressl%2Cxpc%2Cgcr%2Cbui%2Cvprv%2Csvpuc%2Cmime%2Cns%2Crqh%2Cgir%2Cclen%2Cdur%2Clmt&sig=AJfQdSswRgIhANgmR9HJoCc9e9EE7zYXYIZFKfglphMnBawZ9UUsnqzfAiEAvB0erqUIIclPFoTGWDI6C6tXxUXjp1BRGlISbM4wuoM%3D&rm=sn-j5cax8pnpvohm-hxmr7k,sn-9gvld7l&rrc=79,104&fexp=24350590,24350737,24350827,24350961,24351147,24351149,24351173,24351283,24351398,24351523,24351528,24351545,24351606&req_id=14f3dcca1e41a3ee&cmsv=e&rms=rdu,au&redirect_counter=2&cms_redirect=yes&ipbypass=yes&met=1744156378,&mh=VT&mip=187.190.242.110&mm=29&mn=sn-n4v7snly&ms=rdu&mt=1744155895&mv=m&mvi=3&pl=24&lsparams=ipbypass,met,mh,mip,mm,mn,ms,mv,mvi,pl,rms&lsig=ACuhMU0wRAIgfqk3aYh2FUjXey8PF1XaADFPUu4FdI4vDyOZX1xsPQoCIEFuuHFA2j0jpBrc9_vY0evjcW90TKC1n-38ehBZoNQ8" type="audio/mpeg">
    Tu navegador no soporta audio.
  </audio>

  <script>
    function randomPosition() {
      return {
        top: Math.random() * window.innerHeight,
        left: Math.random() * window.innerWidth
      };
    }

    function spawnEmoji() {
      const emoji = document.createElement('div');
      emoji.classList.add('emoji');
      emoji.textContent = ['😄', '😜', '👻', '😂', '🤪'][Math.floor(Math.random() * 5)];
      const pos = randomPosition();
      emoji.style.top = pos.top + 'px';
      emoji.style.left = pos.left + 'px';
      emoji.style.fontSize = (1 + Math.random() * 4) + 'rem';
      document.body.appendChild(emoji);
    }

    function startPrank() {
      const audio = document.getElementById('prank-audio');
      audio.play();
      setInterval(spawnEmoji, 200);
      document.querySelector('button').remove(); // Quita el botón después de iniciar
    }
  </script>
</body>
</html>
