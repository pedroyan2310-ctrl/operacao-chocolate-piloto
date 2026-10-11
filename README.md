
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>O Caso da Mancha de Chocolate — Operação Chocolate</title>
<meta name="description" content="Episódio piloto de uma série escolar de comédia e mistério: O Caso da Mancha de Chocolate. Baixe o projeto para assistir.">[operacao-chocolate-piloto_1.zip](https://github.com/user-attachments/files/33308298/operacao-chocolate-piloto_1.zip)
<!doctype html>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
<style>
  :root{
    --bg:#07070b; --bg2:#0d0d14; --card:#13131c; --card-border:#24243482;
    --cream:#f6f1e6; --muted:#9a97ac;
    --gold:#ffd36f; --pink:#ff7b87; --blue:#71c8ee; --purple:#8377d9; --green:#79cda5;
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    margin:0; background:var(--bg); color:var(--cream);
    font-family:"Trebuchet MS",ui-rounded,system-ui,sans-serif;
    overflow-x:hidden;
  }
  a{color:inherit}
  .wrap{max-width:1040px;margin:0 auto;padding:0 24px}

  .blob{position:fixed;border-radius:50%;filter:blur(60px);opacity:.18;z-index:0;pointer-events:none}
  .blob.b1{width:380px;height:380px;background:var(--gold);top:-120px;left:-100px;animation:drift 22s ease-in-out infinite}
  .blob.b2{width:320px;height:320px;background:var(--pink);bottom:10%;right:-120px;animation:drift 26s ease-in-out infinite reverse}
  .blob.b3{width:260px;height:260px;background:var(--blue);top:45%;left:48%;animation:drift 19s ease-in-out infinite}
  @keyframes drift{0%,100%{transform:translate(0,0) scale(1)}50%{transform:translate(30px,-40px) scale(1.08)}}

  header.hero{position:relative;z-index:1;min-height:92vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:40px 20px}
  .badge{display:inline-block;border:1px solid #585567;border-radius:999px;padding:8px 16px;font-size:12px;letter-spacing:.14em;color:var(--muted);margin-bottom:26px;text-transform:uppercase}
  h1.title{margin:0;font-size:clamp(34px,8vw,78px);line-height:1.04;letter-spacing:.02em;color:#fff}
  h1.title .line{display:block}
  h1.title .letter{display:inline-block;opacity:0;will-change:transform,opacity;
    animation:letterIn .6s cubic-bezier(.2,.85,.25,1.15) forwards;
    animation-delay:calc(var(--i,0) * 45ms)}
  @keyframes letterIn{0%{opacity:0;transform:translateY(22px) rotate(6deg) scale(.85)}70%{opacity:1;transform:translateY(-3px) rotate(-1deg) scale(1.05)}100%{opacity:1;transform:translateY(0) rotate(0) scale(1)}}
  .accent{background:linear-gradient(90deg,var(--gold),var(--pink));-webkit-background-clip:text;background-clip:text;color:transparent}
  .subtitle{margin:22px 0 0;font-size:clamp(14px,2.2vw,19px);color:var(--muted);min-height:1.6em}
  .subtitle .cursor{display:inline-block;width:2px;background:var(--gold);margin-left:2px;animation:blink 1s step-end infinite}
  @keyframes blink{50%{opacity:0}}

  .cta{display:flex;gap:16px;flex-wrap:wrap;justify-content:center;margin-top:38px}
  .btn{display:inline-flex;align-items:center;gap:10px;padding:14px 26px;border-radius:14px;font-weight:800;font-size:15px;text-decoration:none;border:1px solid transparent;transition:transform .18s ease,box-shadow .18s ease}
  .btn:hover{transform:translateY(-3px)}
  .btn.primary{background:linear-gradient(90deg,var(--gold),#ffb57e);color:#1b1407;box-shadow:0 10px 30px #ffd36f33}
  .btn.primary:hover{box-shadow:0 14px 36px #ffd36f55}
  .btn.ghost{background:#ffffff0a;border-color:#595567;color:var(--cream)}
  .btn.ghost:hover{background:#ffffff14}
  .scroll-hint{margin-top:70px;color:var(--muted);font-size:12px;letter-spacing:.2em;text-transform:uppercase;opacity:.7}
  .scroll-hint span{display:block;margin-top:8px;animation:bounce 1.8s ease-in-out infinite}
  @keyframes bounce{0%,100%{transform:translateY(0)}50%{transform:translateY(6px)}}

  section{position:relative;z-index:1;padding:90px 0}
  .section-head{text-align:center;max-width:640px;margin:0 auto 46px}
  .eyebrow{color:var(--gold);font-weight:800;letter-spacing:.14em;text-transform:uppercase;font-size:12px}
  h2{font-size:clamp(26px,4vw,38px);margin:10px 0 0;color:#fff}
  p.lead{color:var(--muted);font-size:16px;line-height:1.7}

  .about-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:40px}
  .stat{background:var(--card);border:1px solid var(--card-border);border-radius:18px;padding:24px;text-align:center}
  .stat b{display:block;font-size:26px;color:var(--gold);margin-bottom:6px}
  .stat span{color:var(--muted);font-size:13px}

  .cast-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:16px;margin-top:10px}
  .card{background:var(--card);border:1px solid var(--card-border);border-radius:18px;padding:20px;transition:transform .25s ease,border-color .25s ease}
  .card:hover{transform:translateY(-6px);border-color:#59566f}
  .card .dot{width:12px;height:12px;border-radius:50%;margin-bottom:12px}
  .card h3{margin:0 0 8px;font-size:17px;color:#fff}
  .card p{margin:0;color:var(--muted);font-size:13.5px;line-height:1.55}

  .how{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;margin-top:10px}
  .how .card p{font-size:14px}

  .team{display:flex;flex-wrap:wrap;gap:12px;justify-content:center;margin-top:28px}
  .pill{background:#ffffff0c;border:1px solid #595567;border-radius:999px;padding:9px 18px;font-size:13.5px;font-weight:700}

  .final-cta{text-align:center;background:var(--bg2);border-top:1px solid var(--card-border);border-bottom:1px solid var(--card-border)}
  .final-cta h2{margin-bottom:14px}

  footer{text-align:center;color:var(--muted);font-size:12.5px;padding:46px 20px 60px;line-height:1.8}
  footer a{color:var(--blue);text-decoration:underline}

  .reveal{opacity:0;transform:translateY(22px);transition:opacity .7s ease,transform .7s ease}
  .reveal.in{opacity:1;transform:translateY(0)}
  @media(max-width:640px){.about-grid{grid-template-columns:1fr}}
</style>
</head>
<body>
  <div class="blob b1"></div><div class="blob b2"></div><div class="blob b3"></div>

  <header class="hero">
    <span class="badge">Episódio Piloto · Animação 2D Original</span>
    <h1 class="title" id="titleEl" aria-label="O Caso da Mancha de Chocolate">
      <span class="line" data-line="O CASO DA"></span>
      <span class="line" data-line="MANCHA DE"></span>
      <span class="line accent-line" data-line="CHOCOLATE"></span>
    </h1>
    <p class="subtitle" id="typeSubtitle"><span id="typeText"></span><span class="cursor">&nbsp;</span></p>
    <div class="cta">
      <a class="btn primary" id="downloadBtn" href="#" target="_blank" rel="noopener">⬇ Baixar e assistir</a>
    </div>
    <div class="scroll-hint">Role para saber mais<span>↓</span></div>
  </header>

  <section id="sobre">
    <div class="wrap">
      <div class="section-head reveal" data-anim="animate__fadeInUp">
        <span class="eyebrow">Sobre a animação</span>
        <h2>Um mistério pequeno que vira caso gigante</h2>
        <p class="lead">Na Escola Vira-Volta, cinco amigos transformam pequenos problemas do cotidiano em
          investigações gigantescas. Cada um imagina a solução de um jeito diferente — e por alguns
          instantes, a sala comum vira o cenário exagerado da teoria que estão contando. No fim, a
          resposta costuma ser mais humana (e mais engraçada) do que qualquer teoria.</p>
      </div>
      <div class="about-grid">
        <div class="stat reveal" data-anim="animate__zoomIn"><b>~11 min</b><span>duração de referência</span></div>
        <div class="stat reveal" data-anim="animate__zoomIn"><b>2D</b><span>animação vetorial original</span></div>
        <div class="stat reveal" data-anim="animate__zoomIn"><b>7</b><span>personagens principais</span></div>
      </div>
    </div>
  </section>

  <section id="personagens" style="background:var(--bg2)">
    <div class="wrap">
      <div class="section-head reveal" data-anim="animate__fadeInUp">
        <span class="eyebrow">Quem investiga o caso</span>
        <h2>Personagens</h2>
      </div>
      <div class="cast-grid">
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:var(--gold)"></div><h3>Kauan</h3><p>Observador e organizado. Desenha mapas de pistas e tenta manter o grupo no caminho.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:var(--green)"></div><h3>Logan</h3><p>Brincalhão, inventivo e querido pelos amigos. Esconde um problema que vira o centro do caso.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:var(--purple)"></div><h3>Gabi</h3><p>Atenta e gentil, sem deixar de ser direta. Percebe quando alguém está escondendo algo.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:var(--blue)"></div><h3>Ravi</h3><p>Fã de filmes de espionagem. Constrói aparelhos com material escolar — nem sempre como planejado.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:var(--pink)"></div><h3>Duda</h3><p>Corajosa e competitiva. Corre para a ação antes de terminar de ouvir o plano.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:#e8c27a"></div><h3>Paçoca</h3><p>Cachorro companheiro do grupo. Curioso, expressivo, e com um faro excelente.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><div class="dot" style="background:#9fb3ff"></div><h3>Professora Cida</h3><p>Firme e acolhedora. Não resolve o mistério pelos alunos, mas ajuda a turma a conversar.</p></div>
      </div>
    </div>
  </section>

  <section id="como-foi-feito">
    <div class="wrap">
      <div class="section-head reveal" data-anim="animate__fadeInUp">
        <span class="eyebrow">Por trás das cenas</span>
        <h2>Como a animação foi feita</h2>
        <p class="lead">Tudo construído do zero com código: personagens vetoriais articulados, cenários com
          profundidade e falas sincronizadas com atuação dos personagens.</p>
      </div>
      <div class="how">
        <div class="card reveal" data-anim="animate__fadeInUp"><h3>🎨 Personagens originais</h3><p>Cada personagem é um SVG articulado por partes, com expressões, piscadas e gestos próprios.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><h3>🎬 24 quadros por segundo</h3><p>Poses claras, antecipação e transições pensadas para parecer fluido mesmo em HTML/CSS/JS.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><h3>🗣️ Atuação e falas</h3><p>Cada fala tem reação corporal e expressão — não é só uma boca mexendo.</p></div>
        <div class="card reveal" data-anim="animate__fadeInUp"><h3>💻 Só web</h3><p>Roda direto no navegador: HTML, CSS e JavaScript puro, sem precisar instalar nada.</p></div>
      </div>
    </div>
  </section>

  <section class="final-cta">
    <div class="wrap reveal" data-anim="animate__fadeIn">
      <span class="eyebrow">Pronto para o caso?</span>
      <h2>Baixe e leve o projeto com você</h2>
      <div class="cta">
        <a class="btn primary" id="downloadBtn2" href="#" target="_blank" rel="noopener">⬇ Baixar e assistir</a> [operacao-chocolate-piloto_1.zip](https://github.com/user-attachments/files/33308298/operacao-chocolate-piloto_1.zip)
<!doctype html>
      </div>
      <p class="lead" style="margin-top:18px;font-size:13px">O download inclui o player completo, a trilha de créditos e todas as imagens. Depois de baixar, extraia o .zip e abra o arquivo <code>assistir.html</code> no Chrome ou Edge para assistir — pode usar Tela cheia para exibir na TV.</p>
    </div>
  </section>

  <div class="team wrap reveal" data-anim="animate__fadeIn" style="padding:0 0 10px">
    <span class="eyebrow" style="display:block;width:100%;text-align:center;margin-bottom:14px">Criado por</span>
  </div>
  <div class="team wrap" style="padding-bottom:50px">
    <span class="pill">Pedro Yan</span>
    <span class="pill">Walace (Judas)</span>
    <span class="pill">Alana</span>
    <span class="pill">Bianca</span>
  </div>

  <footer>
    Projeto escolar original · o roteiro completo vem dentro do download ·
    trilha de aplausos: Starlite (domínio público, Wikimedia Commons)
    <br>Feito com HTML, CSS e JavaScript.
  </footer>

  <!-- Anime.js: efeito extra opcional. A página funciona perfeitamente mesmo se isso falhar ao
       carregar (sem internet, bloqueador de anúncio) — toda animação essencial abaixo é CSS/JS puro. -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js" defer></script>
  <script>
    var REPO_ZIP_URL = "https://github.com/pedroyan2310-ctrl/operacao-chocolate-piloto/raw/main/operacao-chocolate-piloto.zip";
    document.getElementById('downloadBtn').href = REPO_ZIP_URL;
    document.getElementById('downloadBtn2').href = REPO_ZIP_URL;

    try {
      var titleEl = document.getElementById('titleEl');
      var letterCount = 0;
      titleEl.querySelectorAll('.line').forEach(function(lineEl){
        var text = lineEl.getAttribute('data-line');
        var isAccent = lineEl.classList.contains('accent-line');
        lineEl.innerHTML = Array.from(text).map(function(ch){
          var safe = ch === ' ' ? '&nbsp;' : ch;
          var span = '<span class="letter' + (isAccent ? ' accent' : '') + '" style="--i:' + letterCount + '">' + safe + '</span>';
          letterCount++;
          return span;
        }).join('');
      });
    } catch (e) { console.warn('Animação das letras falhou, texto segue visível normalmente.', e); }

    try {
      var fullText = "Episódio piloto · comédia e mistério escolar";
      var typeEl = document.getElementById('typeText');
      var i = 0;
      function typeStep(){
        if(i <= fullText.length){
          typeEl.textContent = fullText.slice(0, i);
          i++;
          setTimeout(typeStep, 38);
        }
      }
      setTimeout(typeStep, 1300);
    } catch (e) { console.warn('Typewriter falhou.', e); }

    try {
      var revealEls = document.querySelectorAll('.reveal');
      if ('IntersectionObserver' in window) {
        var io = new IntersectionObserver(function(entries){
          entries.forEach(function(entry){
            if(entry.isIntersecting){
              entry.target.classList.add('in');
              var anim = entry.target.getAttribute('data-anim') || 'animate__fadeInUp';
              entry.target.classList.add('animate__animated', anim);
              io.unobserve(entry.target);
            }
          });
        }, {threshold:0.18});
        revealEls.forEach(function(el){ io.observe(el); });
      } else {
        revealEls.forEach(function(el){ el.classList.add('in'); });
      }
    } catch (e) { console.warn('Revelação das seções falhou, conteúdo segue visível.', e); }

    window.addEventListener('load', function(){
      try {
        if (typeof anime === 'function') {
          anime({
            targets: '.btn.primary',
            boxShadow: [
              '0 10px 30px rgba(255,211,111,0.2)',
              '0 14px 40px rgba(255,211,111,0.55)',
              '0 10px 30px rgba(255,211,111,0.2)'
            ],
            duration: 2600,
            easing: 'easeInOutSine',
            loop: true
          });
        }
      } catch (e) { console.warn('Brilho extra do botão indisponível (sem internet/CDN), tudo bem.', e); }
    });
  </script>
</body>
</html>
