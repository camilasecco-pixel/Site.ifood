# Site.ifood
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>iFood | Peça o que você ama</title>
  <style>
    :root { --red: #ea1d2c; --dark: #252525; --light: #fff5f5; }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body { font-family: Arial, Helvetica, sans-serif; color: var(--dark); line-height: 1.6; }
    a { color: inherit; text-decoration: none; }
    header { background: white; position: sticky; top: 0; z-index: 10; box-shadow: 0 2px 12px #00000012; }
    nav { max-width: 1120px; margin: auto; padding: 15px 22px; display: flex; justify-content: space-between; align-items: center; gap: 18px; }
    .logo { color: var(--red); font-size: 30px; font-weight: 900; letter-spacing: -1.5px; }
    nav ul { display: flex; list-style: none; gap: 25px; flex-wrap: wrap; }
    nav a:hover { color: var(--red); }
    .hero { background: var(--light); padding: 42px 20px 55px; text-align: center; }
    .carousel { max-width: 1100px; margin: auto; position: relative; }
    .slide { display: none; position: relative; min-height: 330px; border-radius: 22px; overflow: hidden; background-size: cover; background-position: center; color: white; align-items: center; justify-content: center; padding: 40px 22px; }
    .slide.active { display: flex; }
    .slide::before { content: ""; position: absolute; inset: 0; background: linear-gradient(90deg, #000a, #0003); }
    .slide-content { position: relative; max-width: 650px; }
    .slide h1 { font-size: clamp(32px, 5vw, 54px); line-height: 1.1; margin-bottom: 14px; }
    .slide p { font-size: 18px; }
    .carousel-btn { position: absolute; top: 50%; transform: translateY(-50%); border: 0; background: white; color: var(--red); border-radius: 50%; width: 42px; height: 42px; font-size: 24px; cursor: pointer; z-index: 2; }
    .prev { left: 12px; } .next { right: 12px; }
    .dots { display: flex; justify-content: center; gap: 9px; margin-top: 16px; }
    .dot { border: 0; width: 10px; height: 10px; border-radius: 50%; background: #d5a3a6; cursor: pointer; }
    .dot.active { background: var(--red); }
    section { padding: 65px 22px; }
    .container { max-width: 1100px; margin: auto; }
    .section-title { text-align: center; font-size: 32px; margin-bottom: 30px; }
    .section-title span { color: var(--red); }
    .two-col { display: grid; grid-template-columns: 1fr 1fr; align-items: center; gap: 38px; }
    .two-col img { width: 100%; min-height: 280px; max-height: 390px; object-fit: cover; border-radius: 18px; }
    .two-col h2 { font-size: 32px; line-height: 1.2; margin-bottom: 16px; }
    .two-col p { margin-bottom: 18px; color: #555; }
    .btn { display: inline-block; border: 0; border-radius: 9px; background: var(--red); color: white; font-weight: bold; padding: 12px 20px; cursor: pointer; }
    .btn:hover { background: #c91523; }
    .services { background: #fafafa; }
    .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
    .card { background: white; border: 1px solid #eee; border-radius: 16px; padding: 24px; box-shadow: 0 5px 18px #00000008; }
    .card .emoji { font-size: 35px; }
    .card h3 { margin: 10px 0 7px; }
    .card p { color: #666; }
    .contact { background: var(--light); }
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 35px; }
    form { display: grid; gap: 13px; }
    input, textarea { width: 100%; border: 1px solid #ddd; border-radius: 8px; padding: 13px; font: inherit; background: white; }
    textarea { min-height: 120px; resize: vertical; }
    .info p { margin: 12px 0; }
    iframe { width: 100%; height: 260px; border: 0; border-radius: 14px; margin-top: 12px; }
    footer { background: #242424; color: white; padding: 25px 20px; text-align: center; }
    footer strong { color: #ff5360; }
    @media (max-width: 760px) {
      nav { flex-direction: column; }
      nav ul { justify-content: center; gap: 14px; }
      .two-col, .contact-grid { grid-template-columns: 1fr; }
      .cards { grid-template-columns: repeat(2, 1fr); }
      .slide { min-height: 280px; }
    }
    @media (max-width: 480px) { .cards { grid-template-columns: 1fr; } section { padding: 45px 18px; } }
  </style>
</head>
<body>
  <header>
    <nav>
      <a class="logo" href="#home" aria-label="iFood início">iFood</a>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#servicos">Serviços</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="carousel" aria-label="Destaques">
        <article class="slide active" style="background-image:url('https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?auto=format&fit=crop&w=1600&q=85')">
          <div class="slide-content"><h1>Seu prato favorito, a poucos cliques</h1><p>Peça suas comidas preferidas sem sair de casa.</p></div>
        </article>
        <article class="slide" style="background-image:url('https://images.unsplash.com/photo-1546069901-ba9599a7e63c?auto=format&fit=crop&w=1600&q=85')">
          <div class="slide-content"><h1>Mais sabor para o seu dia</h1><p>Encontre opções para todos os gostos e momentos.</p></div>
        </article>
        <article class="slide" style="background-image:url('https://images.unsplash.com/photo-1555939594-58d7cb561ad1?auto=format&fit=crop&w=1600&q=85')">
          <div class="slide-content"><h1>Escolha. Peça. Aproveite.</h1><p>Uma forma prática de descobrir novos sabores.</p></div>
        </article>
        <button class="carousel-btn prev" type="button" aria-label="Imagem anterior">&#8249;</button>
        <button class="carousel-btn next" type="button" aria-label="Próxima imagem">&#8250;</button>
      </div>
      <div class="dots" aria-label="Escolher destaque">
        <button class="dot active" aria-label="Destaque 1"></button>
        <button class="dot" aria-label="Destaque 2"></button>
        <button class="dot" aria-label="Destaque 3"></button>
      </div>
    </section>

    <section id="sobre">
      <div class="container two-col">
        <div>
          <h2>Sobre o <span style="color:#ea1d2c">iFood</span></h2>
          <p>O iFood é uma plataforma digital que conecta clientes, restaurantes, mercados e entregadores. Pelo aplicativo, as pessoas podem descobrir opções, fazer pedidos e acompanhar a entrega.</p>
          <p>Este site é um projeto escolar demonstrativo, criado para apresentar os serviços e a identidade visual da marca.</p>
          <a class="btn" href="#servicos">Conheça os serviços</a>
        </div>
        <img src="https://images.unsplash.com/photo-1526367790999-0150786686a2?auto=format&fit=crop&w=1200&q=85" alt="Entregador levando um pedido">
      </div>
    </section>

    <section class="services" id="servicos">
      <div class="container">
        <h2 class="section-title">O que você encontra no <span>iFood?</span></h2>
        <div class="cards">
          <article class="card"><div class="emoji">🍔</div><h3>Restaurantes</h3><p>Peça hambúrgueres, pizzas, comida caseira e muito mais.</p></article>
          <article class="card"><div class="emoji">🛒</div><h3>Mercado</h3><p>Encontre produtos para completar as compras do dia a dia.</p></article>
          <article class="card"><div class="emoji">🍰</div><h3>Doces e sobremesas</h3><p>Descubra bolos, sorvetes e outras opções doces.</p></article>
          <article class="card"><div class="emoji">🥗</div><h3>Opções variadas</h3><p>Explore pratos e alternativas para diferentes preferências.</p></article>
          <article class="card"><div class="emoji">🛵</div><h3>Entrega</h3><p>Acompanhe as informações do pedido pelo aplicativo.</p></article>
          <article class="card"><div class="emoji">💳</div><h3>Pagamento</h3><p>Confira no app as formas de pagamento disponíveis para seu pedido.</p></article>
        </div>
      </div>
    </section>

    <section>
      <div class="container two-col">
        <img src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?auto=format&fit=crop&w=1200&q=85" alt="Pessoa usando cartão para fazer um pagamento">
        <div>
          <h2>Praticidade para a sua rotina</h2>
          <p>Com poucos passos, você pode pesquisar estabelecimentos, comparar opções e escolher o que combina com o seu momento.</p>
          <p>Consulte disponibilidade, taxas e prazos diretamente no aplicativo oficial, pois eles podem variar conforme o endereço e o estabelecimento.</p>
          <a class="btn" href="https://www.ifood.com.br/" target="_blank" rel="noopener noreferrer">Acessar o iFood</a>
        </div>
      </div>
    </section>

    <section class="contact" id="contato">
      <div class="container">
        <h2 class="section-title">Entre em <span>contato</span></h2>
        <div class="contact-grid">
          <div>
            <h3>Envie uma mensagem</h3>
            <form id="contactForm">
              <input type="text" name="nome" placeholder="Seu nome" aria-label="Seu nome" required>
              <input type="email" name="email" placeholder="Seu e-mail" aria-label="Seu e-mail" required>
              <input type="tel" name="telefone" placeholder="Seu telefone" aria-label="Seu telefone">
              <textarea name="mensagem" placeholder="Digite sua mensagem" aria-label="Digite sua mensagem" required></textarea>
              <button class="btn" type="submit">Enviar mensagem</button>
              <p id="formMessage" aria-live="polite"></p>
            </form>
          </div>
          <div class="info">
            <h3>Informações</h3>
            <p><strong>Site oficial:</strong> <a href="https://www.ifood.com.br/" target="_blank" rel="noopener noreferrer">www.ifood.com.br</a></p>
            <p><strong>Atendimento:</strong> acesse a Central de Ajuda pelo aplicativo ou site oficial.</p>
            <p><strong>Endereço no mapa:</strong> região da sede do iFood em Osasco – SP. Confirme os dados atuais nos canais oficiais.</p>
            <iframe title="Mapa da região de Osasco, São Paulo" loading="lazy" src="https://www.google.com/maps?q=iFood%20Osasco%20SP&output=embed" referrerpolicy="no-referrer-when-downgrade" allowfullscreen></iframe>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer><p>Projeto escolar demonstrativo — <strong>iFood</strong>. Este não é um site oficial da empresa.</p></footer>

  <script>
    const slides = Array.from(document.querySelectorAll('.slide'));
    const dots = Array.from(document.querySelectorAll('.dot'));
    let current = 0;
    function showSlide(index) {
      current = (index + slides.length) % slides.length;
      slides.forEach((slide, i) => slide.classList.toggle('active', i === current));
      dots.forEach((dot, i) => dot.classList.toggle('active', i === current));
    }
    document.querySelector('.prev').addEventListener('click', () => showSlide(current - 1));
    document.querySelector('.next').addEventListener('click', () => showSlide(current + 1));
    dots.forEach((dot, i) => dot.addEventListener('click', () => showSlide(i)));
    setInterval(() => showSlide(current + 1), 5000);

    document.getElementById('contactForm').addEventListener('submit', function(event) {
      event.preventDefault();
      document.getElementById('formMessage').textContent = 'Mensagem demonstrativa! Este formulário não envia dados de verdade.';
      this.reset();
    });
  </script>
</body>
</html>
