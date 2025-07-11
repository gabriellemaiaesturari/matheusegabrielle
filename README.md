<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Casamento - Gabrielle & [Nome]</title>
  <style>
    body {
      margin: 0;
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #ffffff;
      color: #2f3e2e;
    }
    header {
      text-align: center;
      background-color: #f8f8f8;
      padding: 40px 20px;
    }
    header img {
      width: 100%;
      max-height: 500px;
      object-fit: cover;
    }
    h1 {
      font-size: 2.8rem;
      margin: 20px 0 5px;
      color: #556b2f;
    }
    h2 {
      font-size: 1.6rem;
      margin-bottom: 40px;
    }
    section {
      padding: 40px 20px;
      max-width: 800px;
      margin: auto;
    }
    .countdown {
      font-size: 2rem;
      font-weight: bold;
      text-align: center;
      margin-bottom: 40px;
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      background-color: #6b8e23;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background-color: #556b2f;
    }
  </style>
</head>
<body>
  <header>
    <img src="sua-foto-aqui.jpg" alt="Foto dos noivos">
    <h1>Gabrielle & [Nome]</h1>
    <h2>31 de Maio de 2026</h2>
  </header>

  <section>
    <div class="countdown" id="countdown"></div>
  </section>

  <section>
    <h2>Uma mensagem especial para você</h2>
    <p>
      Esse dia é a realização de um sonho, e ele só será completo com a presença de cada pessoa querida que fez parte da nossa história. Obrigado por caminhar ao nosso lado. Esperamos dividir esse momento com muito amor, fé e alegria!
    </p>
  </section>

  <section>
    <h2>Local da cerimônia</h2>
    <p><strong>Espaço Villa Verde</strong><br>
    Rua das Palmeiras, 123 - Bairro Jardim, São Paulo/SP</p>
    <iframe src="https://www.google.com/maps/embed?..." width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
  </section>

  <section>
    <h2>Confirmação de Presença</h2>
    <form>
      <label>Nome completo</label>
      <input type="text" name="nome" required>

      <label>Quantidade de adultos</label>
      <input type="number" name="adultos" min="1" required>

      <label>Crianças (nomes e idades)</label>
      <textarea name="criancas" placeholder="Ex: Ana - 5 anos, Pedro - 8 anos"></textarea>

      <button type="submit">Confirmar Presença</button>
    </form>
  </section>

  <section>
    <h2>Deixe uma mensagem para os noivos</h2>
    <form>
      <label>Seu nome</label>
      <input type="text" name="mensagem_nome">

      <label>Mensagem</label>
      <textarea name="mensagem" rows="4"></textarea>

      <button type="submit">Enviar mensagem</button>
    </form>
  </section>

  <section>
    <h2>Lista de Presentes</h2>
    <p>Você pode nos presentear de forma prática e simbólica através de nossa lista online:</p>
    <ul>
      <li><a href="#">Clique aqui para acessar nossa lista na Amazon</a></li>
      <li><a href="#">Pix para presente: pix@email.com</a></li>
    </ul>
  </section>

  <script>
    const countdown = document.getElementById("countdown");
    const targetDate = new Date("2026-05-31T00:00:00").getTime();

    const timer = setInterval(function () {
      const now = new Date().getTime();
      const distance = targetDate - now;

      if (distance < 0) {
        clearInterval(timer);
        countdown.innerHTML = "O grande dia chegou!";
        return;
      }

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      countdown.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s para o "Sim!"`;
    }, 1000);
  </script>
</body>
</html>
