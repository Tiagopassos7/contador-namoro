<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Contador de Namoro - Tiago & Ricaely</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      color: #fff;
      text-align: center;
      background: url('https://images.unsplash.com/photo-1526045612212-70caf35c14df?auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      backdrop-filter: brightness(0.6);
    }
    h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
    }
    p {
      font-size: 1.2rem;
      max-width: 800px;
      padding: 0 2rem;
    }
    .timer {
      font-size: 2rem;
      margin: 1rem 0;
      background: rgba(0, 0, 0, 0.5);
      padding: 1rem 2rem;
      border-radius: 1rem;
    }
  </style>
</head>
<body>
  <h1>Tiago ❤️ Ricaely</h1>
  <p>Desde 18 de Janeiro de 2025</p>
  <div class="timer" id="timer"></div>
  <p>
    Desde o instante em que nossos olhos se cruzaram, minha vida mudou para sempre. Não foi apenas o começo de uma história de amor, foi o despertar de algo verdadeiro, forte e cheio de propósito. Com você, Tiago, aprendi que o amor não se mede em palavras bonitas, mas em gestos simples, nos detalhes do dia a dia, no cuidado e no carinho que compartilhamos. <br><br>
    Ricaely, cada segundo ao seu lado me mostra que o amor é construção diária, é parceria, é escolher o outro mesmo nos dias difíceis. Nosso amor é uma jornada maravilhosa, cheia de descobertas, desafios superados e momentos inesquecíveis. A cada amanhecer, a certeza de que estamos juntos nessa vida me enche de alegria e gratidão. <br><br>
    Que o tempo continue sendo nosso aliado, que o amor continue sendo nosso guia. Que essa história siga sendo escrita com coragem, ternura e muito afeto. Porque, ao seu lado, descobri o que é amar de verdade. E se eu tivesse que escolher novamente, escolheria você, mil vezes mais.
  </p>

  <script>
    const startDate = new Date("2025-01-18T00:00:00").getTime();

    function updateTimer() {
      const now = new Date().getTime();
      let distance = now - startDate;

      const years = Math.floor(distance / (1000 * 60 * 60 * 24 * 365));
      const months = Math.floor((distance % (1000 * 60 * 60 * 24 * 365)) / (1000 * 60 * 60 * 24 * 30));
      const days = Math.floor((distance % (1000 * 60 * 60 * 24 * 30)) / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      document.getElementById("timer").innerHTML =
        `${years} anos, ${months} meses, ${days} dias, ${hours} horas, ${minutes} minutos, ${seconds} segundos`;
    }

    setInterval(updateTimer, 1000);
    updateTimer();
  </script>
</body>
</html>
