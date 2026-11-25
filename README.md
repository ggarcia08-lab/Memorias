# Memorias
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Resgate Cronológico do Garcia</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;400;500&display=swap');

    :root {
      --bg-deep: #020617;
      --bg-blue: #0f172a;
      --accent: #38bdf8;
      --accent-soft: #7dd3fc;
      --text: #e0f2fe;
      --text-muted: #94a3b8;
      --glow: 0 0 20px rgba(56, 189, 248, 0.4);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg-deep);
      color: var(--text);
      line-height: 1.7;
      overflow-x: hidden;
      min-height: 100vh;
    }

    /* Fundo com estrelas e nebula */
    .stars {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
      background: 
        radial-gradient(ellipse at 20% 30%, rgba(56, 189, 248, 0.08) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 70%, rgba(14, 165, 233, 0.06) 0%, transparent 50%),
        radial-gradient(circle at 50% 50%, #0f172a 0%, #020617 100%);
    }

    .star {
      position: absolute;
      background: white;
      border-radius: 50%;
      animation: twinkle 3s infinite ease-in-out;
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.3; transform: scale(1); }
      50% { opacity: 1; transform: scale(1.2); }
    }

    /* Buraco negro decorativo */
    .black-hole {
      position: absolute;
      border-radius: 50%;
      background: radial-gradient(circle at 40% 40%, #1e293b 0%, #0f172a 40%, #000 70%);
      box-shadow: 
        0 0 40px 10px rgba(56, 189, 248, 0.15),
        inset 0 0 30px rgba(0,0,0,0.9);
      pointer-events: none;
      z-index: 0;
    }

    .container {
      position: relative;
      z-index: 1;
      max-width: 900px;
      margin: 0 auto;
      padding: 40px 20px 80px;
    }

    /* Header / Título */
    .header {
      display: flex;
      align-items: center;
      gap: 30px;
      margin-bottom: 50px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .title-box {
      flex: 1;
      min-width: 280px;
    }

    h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(1.8rem, 5vw, 2.6rem);
      background: linear-gradient(90deg, #7dd3fc, #38bdf8, #0ea5e9);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: var(--glow);
      letter-spacing: 1px;
      margin-bottom: 8px;
    }

    .subtitle {
      color: var(--text-muted);
      font-size: 0.95rem;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .photo-placeholder {
      width: 180px;
      height: 180px;
      border-radius: 16px;
      background: linear-gradient(145deg, #1e293b, #0f172a);
      border: 2px solid rgba(56, 189, 248, 0.3);
      box-shadow: var(--glow);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text-muted);
      font-size: 0.85rem;
      text-align: center;
      overflow: hidden;
      position: relative;
      transition: all 0.3s ease;
    }

    .photo-placeholder:hover {
      border-color: var(--accent);
      transform: scale(1.03);
    }

    .photo-placeholder img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .photo-placeholder span {
      padding: 10px;
    }

    /* Seções */
    section {
      background: rgba(15, 23, 42, 0.7);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(56, 189, 248, 0.15);
      border-radius: 20px;
      padding: 35px 30px;
      margin-bottom: 40px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.3);
      position: relative;
      overflow: hidden;
    }

    section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, transparent, var(--accent), transparent);
    }

    h2 {
      font-family: 'Orbitron', sans-serif;
      font-size: 1.5rem;
      color: var(--accent-soft);
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    h2::before {
      content: '✦';
      color: var(--accent);
      font-size: 1.2rem;
    }

    p {
      margin-bottom: 18px;
      color: #cbd5e1;
      font-size: 1.05rem;
      text-align: justify;
    }

    .photo-area {
      margin: 30px 0;
      display: flex;
      justify-content: center;
    }

    .photo-area .photo-placeholder {
      width: 100%;
      max-width: 420px;
      height: 260px;
      border-radius: 12px;
    }

    .final-text {
      text-align: center;
      font-style: italic;
      color: var(--accent-soft);
      font-size: 1.15rem;
      margin-top: 25px;
      padding: 20px;
      border-left: 3px solid var(--accent);
      background: rgba(56, 189, 248, 0.05);
    }

    /* Página / Divisor */
    .page-break {
      height: 60px;
      position: relative;
      margin: 20px 0;
    }

    .page-break::after {
      content: '';
      position: absolute;
      top: 50%;
      left: 10%;
      right: 10%;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(56,189,248,0.4), transparent);
    }

    footer {
      text-align: center;
      margin-top: 60px;
      color: var(--text-muted);
      font-size: 0.9rem;
      letter-spacing: 1px;
    }

    /* Responsivo */
    @media (max-width: 600px) {
      .header {
        flex-direction: column-reverse;
        text-align: center;
      }
      .photo-placeholder {
        width: 150px;
        height: 150px;
      }
      section {
        padding: 25px 18px;
      }
    }
  </style>
</head>
<body>
  <div class="stars" id="stars"></div>

  <!-- Buracos negros decorativos -->
  <div class="black-hole" style="width: 180px; height: 180px; top: 8%; right: -40px; opacity: 0.7;"></div>
  <div class="black-hole" style="width: 120px; height: 120px; bottom: 15%; left: -30px; opacity: 0.5;"></div>

  <div class="container">
    <!-- CABEÇALHO -->
    <header class="header">
      <div class="title-box">
        <h1>Resgate cronológico do Garcia!</h1>
        <div class="subtitle">Uma jornada através do tempo e do espaço</div>
      </div>
      <div class="photo-placeholder">
        <span>Adicionar<br>foto aqui</span>
        <!-- Substitua por: <img src="sua-foto.jpg" alt="Garcia"> -->
      </div>
    </header>

    <!-- PÁGINA 1 - Escola Municipal Paulo Freire -->
    <section>
      <h2>Início da jornada – Escola Municipal Paulo Freire</h2>
      <p>
        Minha história começa na Escola Municipal Paulo Freire. Tive professoras que, embora tenham sido muito marcantes, 
        infelizmente não recordo mais os nomes. No entanto, a que mais permanece em minha memória é uma mulher alta, 
        de cabelos cacheados e pele escura. Recentemente, reencontrei-a próximo à escola. Mesmo após tantos anos, 
        ela continua com uma altura superior à minha.
      </p>

      <div class="photo-area">
        <div class="photo-placeholder">
          <span>Adicionar foto<br>desta fase</span>
        </div>
      </div>
    </section>

    <div class="page-break"></div>

    <!-- PÁGINA 2 - Benedicto João Cordeiro -->
    <section>
      <h2>Minha jornada no Benedicto João Cordeiro</h2>
      <p>
        No 6º ano do Benedicto, eu era bastante solitário e me isolava por algum motivo. Por conta disso, 
        comecei a ser ironizado pelos demais alunos. Após algum tempo, uma menina notou essa situação e 
        decidiu agir de forma diferente: aproximou-se de mim e iniciou uma conversa. A partir daquele momento, 
        nasceu uma amizade que me ajudou profundamente a voltar a ser quem eu realmente era — extrovertido e brincalhão. 
        Depois disso, passei a criar mais amizades, embora sempre com um grupo pequeno da sala.
      </p>
      <p>
        Até que chegou a pandemia. A partir de então, eu só ficava em casa jogando no computador. 
        Em consequência disso, vieram as “gordurinhas”. Acredito que, naquele período, cheguei a pesar cerca de 80 kg.
      </p>
      <p>
        Após a pandemia, vivi tanto experiências boas quanto ruins. Fiz amizades inesperadas, e uma delas se destaca 
        especialmente na minha visão: o Gordão. Vou contar como nossa amizade começou.
      </p>
      <p>
        No passado, eu tinha uma amizade em que, ao descobrir certas atitudes dessa pessoa, percebi que não se tratava 
        de uma amizade verdadeira. Determinado a cortar relações, pensei em frases e gestos para expressar minha 
        frustração. Enviei uma mensagem curta e direta — “não quero mais ser seu amigo” — e a bloqueei em tudo. 
        Assim, minha vida seguiu sem essa pessoa.
      </p>
      <p>
        Alguns dias depois, três meninos mais velhos vieram me ameaçar e me acusar de coisas horrorosas dentro da sala 
        de aula. Sem compreender o motivo, fiquei desesperado com as ameaças. Depois que a poeira baixou, fiz o que 
        qualquer menino novo não deveria ter vergonha de fazer: peguei o telefone e liguei para alguém que me protegia — 
        meu pai. Após a ligação, ele logo estava na escola para resolver a situação.
      </p>
      <p>
        Descobri que a pessoa que eu considerava amiga havia criado uma conta no Instagram para me difamar, citando 
        meu nome. Após os acontecimentos — nos quais meu irmão também me ajudou e me protegeu —, descobri que uma 
        das pessoas que queria brigar comigo era exatamente o Gustavo Henrique, vulgo Gordão. Foi assim que nasceu 
        uma amizade que já se prolonga por mais de seis anos.
      </p>

      <div class="photo-area">
        <div class="photo-placeholder">
          <span>Adicionar foto<br>(Benedicto / amizades)</span>
        </div>
      </div>

      <!-- Campo extra de fotos um pouco distante -->
      <div class="photo-area" style="margin-top: 50px;">
        <div class="photo-placeholder">
          <span>Mais fotos<br>desta fase</span>
        </div>
      </div>
    </section>

    <div class="page-break"></div>

    <!-- PÁGINA 3 - Ensino Médio -->
    <section>
      <h2>Ensino Médio – 3º Ano H</h2>
      <p>
        Admito que este está sendo o melhor ano da minha vida escolar. Ao longo dos anos passados, fui ficando 
        cada vez mais extrovertido e fazendo cada vez mais amizades — desta vez, inclusive de outras turmas! 
        Não consigo nem contar nos dedos quantas pessoas considero meus amigos. Todo esse mérito eu atribuo a 
        dois amigos especiais: o Gordão e o Tonhão. Com o Tonho fiz amizade há um ano, mas parece uma amizade 
        de muitos anos. Esses dois me ajudaram a ser quem eu sou de verdade: uma pessoa que gosta de brincar 
        com os outros, porém de uma forma que faça a outra parte rir também.
      </p>

      <div class="photo-area">
        <div class="photo-placeholder">
          <span>Adicionar foto<br>3º Ano H</span>
        </div>
      </div>

      <div class="final-text">
        A última coisa que quero dizer é que vou sentir falta disso: das brincadeiras no colégio e das experiências 
        únicas que o último ano do Ensino Médio me proporcionou. Isso ficará no meu coração para sempre.
      </div>
    </section>

    <footer>
      ✦ Resgate Cronológico do Garcia ✦<br>
      Uma viagem pelo espaço-tempo das memórias
    </footer>
  </div>

  <script>
    // Gera estrelas dinamicamente
    const starsContainer = document.getElementById('stars');
    for (let i = 0; i < 120; i++) {
      const star = document.createElement('div');
      star.className = 'star';
      const size = Math.random() * 2.5 + 0.5;
      star.style.width = size + 'px';
      star.style.height = size + 'px';
      star.style.left = Math.random() * 100 + '%';
      star.style.top = Math.random() * 100 + '%';
      star.style.animationDelay = Math.random() * 4 + 's';
      star.style.animationDuration = (Math.random() * 3 + 2) + 's';
      starsContainer.appendChild(star);
    }
  </script>
</body>
</html>
