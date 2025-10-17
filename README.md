[index.html](https://github.com/user-attachments/files/22973876/index.html)[musica.mp3](https://github.com/user-attachments/files/22973877/musica.mp3)

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Contrato de Namoro - Rayanne Diana</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Georgia', serif;
      background: #fdf9f3;
      padding: 20px;
      min-height: 100vh;
      overflow-y: auto;
      position: relative;
      color: #444;
    }

    .contract {
      background: #fffaf0;
      width: 100%;
      max-width: 600px;
      padding: 25px;
      border: 2px solid #e0d0b0;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      line-height: 1.6;
      color: #444;
      margin: 0 auto;
      position: relative;
    }

    h1 {
      text-align: center;
      font-size: 24px;
      margin-bottom: 10px;
      color: #5a4a3a;
    }

    @media (min-width: 768px) {
      h1 {
        font-size: 28px;
      }
    }

    .heart {
      text-align: center;
      font-size: 26px;
      margin: 10px 0;
      color: #e74c3c;
    }

    @media (min-width: 768px) {
      .heart {
        font-size: 30px;
      }
    }

    .field {
      display: inline-block;
      min-width: 100px;
      border-bottom: 1px dashed #999;
      padding: 2px 0;
      margin: 0 5px;
      outline: none;
      background: transparent;
      border: none;
      font-family: inherit;
      font-size: inherit;
      color: inherit;
    }

    @media (max-width: 480px) {
      .field {
        min-width: 80px;
        font-size: 14px;
      }
    }

    .field:focus {
      outline: none;
      border-bottom: 1px solid #e74c3c;
    }

    .section {
      margin: 15px 0;
    }

    ul {
      padding-left: 20px;
      margin: 10px 0;
    }

    .penalty {
      background: #fff8e1;
      padding: 10px;
      border-left: 4px solid #ff9800;
      margin: 15px 0;
      font-weight: bold;
      border-radius: 0 4px 4px 0;
    }

    @media (max-width: 480px) {
      .penalty {
        padding: 8px;
        font-size: 14px;
      }
    }

    .signatures {
      margin-top: 25px;
      text-align: center;
    }

    .signature-line {
      width: 45%;
      display: inline-block;
      border-bottom: 1px solid #888;
      padding: 5px;
      margin: 8px;
      cursor: pointer;
      transition: border-color 0.3s;
      font-size: 16px;
    }

    @media (max-width: 480px) {
      .signature-line {
        width: 90%;
        font-size: 14px;
        margin: 5px 0;
      }
    }

    .signature-line:hover {
      border-bottom: 1px solid #e74c3c;
    }

    .footer {
      font-size: 12px;
      text-align: center;
      margin-top: 20px;
      color: #888;
    }

    .checkboxes {
      margin-top: 8px;
    }

    .checkboxes label {
      margin-right: 15px;
      cursor: pointer;
      font-size: 14px;
    }

    @media (min-width: 768px) {
      .checkboxes label {
        margin-right: 20px;
        font-size: 16px;
      }
    }

    input[type="radio"] {
      margin-right: 5px;
    }

    .confirm-button {
      display: block;
      width: 80%;
      margin: 25px auto;
      padding: 10px;
      background: #e74c3c;
      color: white;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    @media (min-width: 768px) {
      .confirm-button {
        padding: 12px;
        font-size: 18px;
      }
    }

    .confirm-button:hover {
      background: #c0392b;
      transform: scale(1.05);
    }

    .confirm-button:active {
      transform: scale(0.98);
    }

    .surprise {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: black;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 100;
      opacity: 0;
      pointer-events: none;
      transition: opacity 1s ease-in-out;
      overflow: hidden;
      padding: 20px;
      box-sizing: border-box;
    }

    .surprise.active {
      opacity: 1;
      pointer-events: all;
    }

    .star-bg {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 20% 30%, rgba(200, 0, 0, 0.2) 0%, rgba(0,0,0,1) 70%);
      z-index: -1;
    }

    .particle {
      position: absolute;
      background: white;
      border-radius: 50%;
      pointer-events: none;
    }

    .lyric {
      font-size: 20px;
      color: white;
      text-shadow: 0 0 10px rgba(255,255,255,0.8);
      opacity: 0;
      transition: opacity 1s ease, transform 0.5s ease;
      text-align: center;
      margin: 8px 0;
      font-weight: bold;
    }

    @media (min-width: 768px) {
      .lyric {
        font-size: 28px;
        margin: 10px 0;
      }
    }

    .lyric.visible {
      opacity: 1;
      transform: scale(1.1);
    }

    .lyric.highlight {
      color: yellow;
      text-shadow: 0 0 15px rgba(255,215,0,0.8);
      animation: pulse 1s infinite alternate;
    }

    @keyframes pulse {
      from { transform: scale(1); }
      to { transform: scale(1.05); }
    }

    .watermark {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 12px;
      color: white;
      opacity: 0.7;
      font-family: monospace;
      letter-spacing: 1px;
    }

    @media (max-width: 480px) {
      .watermark {
        font-size: 10px;
        top: 10px;
        right: 10px;
      }
    }

    .heart-float {
      position: absolute;
      font-size: 24px;
      animation: float 3s ease-in-out infinite;
      z-index: 999;
    }

    @media (min-width: 768px) {
      .heart-float {
        font-size: 30px;
      }
    }

    .heart-purple {
      color: #9b59b6;
    }

    .heart-red {
      color: #e74c3c;
    }

    @keyframes float {
      0% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-10px) rotate(10deg); }
      100% { transform: translateY(0px) rotate(0deg); }
    }

    #playButton {
      background: #e74c3c;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 18px;
      border-radius: 30px;
      margin-top: 20px;
      cursor: pointer;
      display: none;
    }

    #playButton.show {
      display: block;
    }
  </style>
</head>
<body>

  <div class="contract" id="contrato">
    <h1>Contrato de Namoro</h1>
    <div class="heart">♡</div>

    <div class="section">
      Data do início: 
      <input type="text" class="field" id="data-inicio" placeholder="__/__/____" maxlength="10" style="width: 60px;">
      <br><br>
      Data da assinatura: 
      <input type="text" class="field" id="data-assinatura" placeholder="__/__/____" maxlength="10" style="width: 60px;">
    </div>

    <div class="section">
      Eu 
      <input type="text" class="field" id="nome1" placeholder="seu nome" style="min-width: 150px;">
      , declaro que com esse contrato, nosso amor acaba de se iniciar.
    </div>

    <div class="section">
      <strong>Benefícios de assinar comigo:</strong>
      <ul>
        <li>Beijinhos pra sempre.</li>
        <li>Companhia pra todos os lugares (obrigatório).</li>
        <li>Construir nosso futuro juntinhos.</li>
      </ul>

      <strong>Concorda com todas as MINHAS exigências?</strong><br>
      <div class="checkboxes">
        <label><input type="radio" name="concorda" value="sim"> Sim.</label>
        <label><input type="radio" name="concorda" value="obvio"> Óbvio.</label>
      </div>
    </div>

    <div class="section">
      Eu 
      <input type="text" class="field" id="nome2" placeholder="nome da pessoa amada" style="min-width: 150px;">
      , assino esse contrato por livre e espontânea pressão.
    </div>

    <div class="penalty">
      <strong>QUEBRA DE CONTRATO ❌</strong><br>
      Nesse caso, a multa será de R$ 100.000,00 ao réquerente, fora os milhares de chocolatinhos.
    </div>

    <div class="signatures">
      <strong>ASSINATURAS:</strong><br><br>
      <div class="signature-line" contenteditable="true" id="assinatura1" placeholder="Sua assinatura"></div>
      <div class="signature-line" contenteditable="false" style="background: #fffbe6; border: 1px solid #e74c3c; font-weight: bold;">Rayanne Diana</div>
    </div>

    <div class="footer">
      Renovação: todo ano, no dia do nosso aniversário de namoro.<br>
      ❤️ Válido enquanto houver amor, risadas e paciência mútua.
    </div>

    <button class="confirm-button" id="confirmar">VOCÊ CONFIRMA ISSO? 😍</button>
  </div>

  <div class="surprise" id="surprise">
    <div class="star-bg" id="starBg"></div>
    <div class="watermark">JHF_MP3</div>
    
    <div class="lyric" id="lyric1">Eu não consigo parar</div>
    <div class="lyric highlight" id="lyric2">DE AMAR</div>
    <div class="lyric" id="lyric3">VOCÊ</div>
    <div class="lyric" id="lyric4">Por mais que eu</div>
    <div class="lyric highlight" id="lyric5">TENTE</div>
    <div class="lyric" id="lyric6">Não</div>
    <div class="lyric highlight" id="lyric7">CONSIGO</div>
    <div class="lyric" id="lyric8">Não posso deixar de</div>
    <div class="lyric highlight" id="lyric9">TE QUERER</div>
    <div class="lyric" id="lyric10">Eu sei que morreria</div>
    <div class="lyric highlight" id="lyric11">SEM VOCÊ</div>

    <button id="playButton">▶️ TOCAR MÚSICA</button>
  </div>

  <!-- ÁUDIO: coloque seu arquivo como "musica.mp3" na mesma pasta -->
  <audio id="music" src="musica.mp3" preload="auto"></audio>

  <script>
    const confirmButton = document.getElementById('confirmar');
    const surprise = document.getElementById('surprise');
    const starBg = document.getElementById('starBg');
    const music = document.getElementById('music');
    const playButton = document.getElementById('playButton');

    function createParticles() {
      for (let i = 0; i < 100; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.width = Math.random() * 2 + 'px';
        particle.style.height = particle.style.width;
        particle.style.left = Math.random() * 100 + 'vw';
        particle.style.top = Math.random() * 100 + 'vh';
        particle.style.opacity = Math.random() * 0.5 + 0.5;
        starBg.appendChild(particle);
        setInterval(() => {
          particle.style.left = Math.random() * 100 + 'vw';
          particle.style.top = Math.random() * 100 + 'vh';
        }, 5000 + Math.random() * 5000);
      }
    }

    function playMusic() {
      music.play()
        .then(() => {
          playButton.classList.remove('show');
        })
        .catch(e => {
          playButton.classList.add('show');
        });
    }

    playButton.addEventListener('click', playMusic);

    confirmButton.addEventListener('click', function() {
      surprise.classList.add('active');
      playMusic();
      createParticles();
      
      // Cria corações flutuantes
      for (let i = 0; i < 20; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart-float ' + (Math.random() > 0.5 ? 'heart-purple' : 'heart-red');
        heart.textContent = '❤️';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.top = Math.random() * 100 + 'vh';
        heart.style.animationDuration = (2 + Math.random() * 3) + 's';
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 10000);
      }

      // ⏱️ Sincronização ajustada para áudio de ~29s que começa com a música
      const lyrics = [
        { id: 'lyric1', delay: 1000 },   // 1s
        { id: 'lyric2', delay: 3000 },   // 3s
        { id: 'lyric3', delay: 4000 },   // 4s
        { id: 'lyric4', delay: 6000 },   // 6s
        { id: 'lyric5', delay: 8000 },   // 8s
        { id: 'lyric6', delay: 10000 },  // 10s
        { id: 'lyric7', delay: 11000 },  // 11s
        { id: 'lyric8', delay: 13000 },  // 13s
        { id: 'lyric9', delay: 15000 },  // 15s
        { id: 'lyric10', delay: 18000 }, // 18s
        { id: 'lyric11', delay: 20000 }  // 20s
      ];

      lyrics.forEach(line => {
        setTimeout(() => {
          document.getElementById(line.id).classList.add('visible');
        }, line.delay);
      });
    });

    // Formatação de data
    document.querySelectorAll('input[type="text"]').forEach(input => {
      if (input.placeholder.includes('__')) {
        input.addEventListener('input', function() {
          let value = this.value.replace(/\D/g, '');
          if (value.length >= 2) value = value.substring(0,2) + '/' + value.substring(2);
          if (value.length >= 5) value = value.substring(0,5) + '/' + value.substring(5,9);
          this.value = value;
        });
      }
    });
  </script>

</body>
</html>
