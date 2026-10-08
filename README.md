[style.css](https://github.com/user-attachments/files/33225598/style.css)

/* ── VARIÁVEIS ── */
  :root{
    --g-dark:#073d00;      /* verde escuro — header, footer */
    --g-mid:#1a7a00;       /* verde médio — botões, destaques */
    --g-brand:#3ec400;     /* verde Monster — logo, títulos */
    --g-light:#eaf6e2;     /* verde claríssimo — fundo de seções alt */
    --white:#ffffff;
    --text-dark:#061e00;
    --text-muted:#4a6640;
    --border:#c8e6b0;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  section[id]{scroll-margin-top:76px}
  html,body{background:var(--white);color:var(--text-dark);font-family:'Arial Black',Arial,sans-serif;scroll-behavior:smooth;overflow-x:hidden}
  /* ── HEADER ── */
  .hdr{
    position:sticky;top:0;z-index:200;
    display:flex;align-items:center;justify-content:space-between;
    padding:14px 48px;background:#000;
  }
  .hdr-logo{display:flex;align-items:center;gap:12px}
  .hdr-logo-img{height:46px;width:auto;display:block}
  .hdr-m{font-size:36px;font-weight:900;color:var(--g-brand);line-height:1;letter-spacing:-2px}
  .hdr-txt{font-size:10px;letter-spacing:5px;color:#a8d090;text-transform:uppercase}
  .hdr-nav{display:flex;gap:28px}
  .hdr-nav a{color:#c8e6b0;text-decoration:none;font-size:11px;letter-spacing:3px;text-transform:uppercase;font-weight:700;transition:color .2s}
  .hdr-nav a:hover{color:var(--g-brand)}
  .hdr-cta{
    background:var(--g-brand);color:var(--g-dark);border:none;padding:10px 22px;
    font-size:11px;font-weight:900;letter-spacing:2px;text-transform:uppercase;
    cursor:pointer;clip-path:polygon(6px 0%,100% 0%,calc(100% - 6px) 100%,0% 100%);
    transition:background .2s;
  }
  .hdr-cta:hover{background:#5ee000}
  /* ── HERO ── */
  .hero{
    text-align:center;padding:60px 24px;
    background:#000;
    min-height:92vh;display:flex;flex-direction:column;align-items:center;justify-content:center;
  }
  .hero-eye{font-size:10px;letter-spacing:7px;color:#a8d090;text-transform:uppercase;font-weight:700;margin-bottom:20px}
  .hero-h1{
    font-size:clamp(52px,10vw,108px);font-weight:900;
    color:var(--white);line-height:.88;letter-spacing:-3px;text-transform:uppercase;
  }
  .hero-h1 .wht{color:var(--g-brand)}
  .hero-sub{font-size:12px;color:#a8d090;letter-spacing:4px;text-transform:uppercase;margin-top:24px}
  /* ── CAROUSEL ── */
  .car-section{padding:56px 0 16px;background:var(--white);overflow:hidden}
  .car-title{display:table;margin:0 auto 8px;font-size:9px;letter-spacing:5px;color:var(--g-mid);text-transform:uppercase;font-weight:700;border:2px solid var(--g-brand);padding:6px 16px}
  .car-wrap{width:100%;height:520px;display:flex;align-items:center;justify-content:center;position:relative}
  .car-stage{position:relative;width:100%;height:100%;display:flex;align-items:center;justify-content:center}
  .can-item{
    position:absolute;text-align:center;background:transparent;
    transition:transform 1.1s cubic-bezier(.25,.46,.45,.94),
               opacity 1.1s ease;
    cursor:pointer;user-select:none;will-change:transform,opacity;
  }
  .can-item img{display:block;height:400px;width:auto;margin:0 auto;pointer-events:none;background:transparent;}
  .can-item.pos0 img{filter:none;}
  .can-label{
    margin-top:10px;font-size:9px;letter-spacing:3px;text-transform:uppercase;
    font-weight:700;opacity:0;transition:opacity .4s;color:var(--g-mid);
  }
  .can-item.pos0 .can-label{opacity:1}
  .car-dots{display:flex;justify-content:center;gap:7px;padding:20px 0 28px}
  .dot{width:22px;height:3px;background:var(--border);cursor:pointer;transition:background .3s;clip-path:polygon(3px 0%,100% 0%,calc(100% - 3px) 100%,0% 100%)}
  .dot.on{background:var(--g-mid)}
  /* ── DIVISOR ── */
  .div{height:3px;background:var(--g-brand);margin:0}
  /* ── STATS ── */
  /* ── ESPORTES ── */
  .sports{padding:80px 48px;background:var(--white);text-align:center}
  .s-tag{display:inline-block;font-size:9px;letter-spacing:5px;color:var(--g-mid);text-transform:uppercase;font-weight:700;border:2px solid var(--g-brand);padding:6px 16px;margin-bottom:22px}
  .s-title{font-size:clamp(34px,5.5vw,64px);font-weight:900;text-transform:uppercase;line-height:.92;margin-bottom:10px;color:var(--g-dark)}
  .s-title .g{color:var(--g-mid)}
  .s-sub{color:var(--text-muted);font-size:12px;letter-spacing:3px;margin-bottom:50px}
  .s-slider{position:relative}
  .s-viewport{overflow:hidden}
  .s-grid{display:flex;gap:4px;transition:transform .85s cubic-bezier(.25,.46,.45,.94);will-change:transform}
  .s-grid .s-card{flex:0 0 calc((100% - 8px)/3)}
  .s-nav{
    position:absolute;top:50%;transform:translateY(-50%);z-index:5;
    width:46px;height:46px;border-radius:50%;border:2px solid var(--g-brand);
    background:rgba(0,0,0,.65);color:var(--g-brand);font-size:20px;line-height:1;
    cursor:pointer;transition:background .25s,color .25s,opacity .25s;
  }
  .s-nav:hover{background:var(--g-brand);color:#000}
  .s-nav[disabled]{opacity:.25;cursor:default;pointer-events:none}
  .s-nav.prev{left:-14px}
  .s-nav.next{right:-14px}
  .s-card{
    position:relative;overflow:hidden;cursor:pointer;
    aspect-ratio:3/4;display:flex;flex-direction:column;justify-content:flex-end;
    transition:transform .3s;
  }
  .s-card:hover{transform:scale(1.01)}
  .s-bg{position:absolute;inset:0}
  .s-bg img{width:100%;height:100%;object-fit:cover;opacity:.92;transition:transform .55s ease,opacity .4s}
  .s-card:hover .s-bg img{transform:scale(1.05);opacity:1}
  /* ── CTA STRIP ── */
  .cta-strip{
    display:flex;align-items:center;justify-content:space-between;
    padding:52px 48px;background:#000;
  }
  .cta-strip h3{font-size:clamp(22px,3vw,40px);font-weight:900;text-transform:uppercase;color:var(--white)}
  .cta-strip h3 span{color:var(--g-brand)}
  .cta-big{
    background:var(--white);color:var(--g-dark);border:none;padding:16px 40px;
    font-size:13px;font-weight:900;letter-spacing:2px;text-transform:uppercase;
    cursor:pointer;clip-path:polygon(8px 0%,100% 0%,calc(100% - 8px) 100%,0% 100%);
    transition:background .2s,color .2s;white-space:nowrap;
  }
  .cta-big:hover{background:var(--g-brand);color:var(--g-dark)}
  /* ── FOOTER ── */
  .ftr{background:#000;border-top:4px solid var(--g-brand);padding:36px 48px;display:flex;align-items:center;justify-content:space-between}
  .ftr-logo{font-size:26px;font-weight:900;color:var(--g-brand);letter-spacing:-1px}
  .ftr-logo-img{height:40px;width:auto;display:block}
  .ftr-copy{font-size:9px;color:#a8d090;letter-spacing:2px;text-align:center}
  .ftr-links{display:flex;gap:20px}
  .ftr-links a{color:#a8d090;font-size:9px;letter-spacing:2px;text-decoration:none;text-transform:uppercase;transition:color .2s}
  .ftr-links a:hover{color:var(--g-brand)}
  /* ── ATLETAS ── */
  .athletes{background:#0b0d0b;padding:64px 48px}
  .ath-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;max-width:1280px;margin:0 auto}
  .ath-card{
    display:flex;align-items:stretch;background:#151815;overflow:hidden;cursor:pointer;
    transition:transform .3s,box-shadow .35s ease;
  }
  .ath-card:hover{transform:translateY(-3px);box-shadow:0 10px 30px rgba(62,196,0,.15)}
  .ath-photo{
    flex:0 0 44%;min-height:150px;background:#000 url(../img/logo-monster.jpg) center/62% no-repeat;
  }
  .ath-info{flex:1;padding:20px 18px;display:flex;flex-direction:column;justify-content:center;gap:9px}
  .ath-tag{font-size:9px;letter-spacing:3px;color:var(--g-brand);text-transform:uppercase;font-weight:900}
  .ath-name{font-size:16px;font-weight:900;color:var(--white)}
  .ath-country{display:flex;align-items:center;gap:8px;font-size:11px;color:#9aa39a}
  .ath-flag{font-size:14px;line-height:1}
  .ath-flag-img{height:12px;width:auto;display:block;border-radius:1px}
  .ath-feature{max-width:1280px;margin:26px auto 0}
  .ath-feature img{width:100%;height:auto;display:block}
  .ath-feature-caption{padding:18px 4px 0;font-size:14px;color:#c9d2c9;letter-spacing:.4px;line-height:1.6}
  .ath-feature-caption strong{color:var(--white);font-weight:900}
  .ath-feature-caption .g{color:var(--g-brand);font-weight:900}
  /* ── EVENTOS ── */
  .events{background:#161816;padding:80px 48px}
  .ev-card{
    max-width:1280px;margin:0 auto;background:#151815;overflow:hidden;cursor:pointer;
    transition:transform .3s,box-shadow .35s ease;
  }
  .ev-card:hover{transform:translateY(-3px);box-shadow:0 10px 30px rgba(62,196,0,.15)}
  .ev-media{overflow:hidden}
  .ev-card img{width:100%;height:auto;display:block;transition:transform .55s ease}
  .ev-card:hover img{transform:scale(1.04)}
  .ev-content{padding:28px 32px 32px}
  .ev-tag{display:inline-block;font-size:9px;letter-spacing:5px;color:var(--g-brand);text-transform:uppercase;font-weight:900;border:2px solid var(--g-brand);padding:6px 16px;margin-bottom:16px}
  .ev-title{font-size:clamp(38px,5vw,64px);font-weight:900;text-transform:uppercase;line-height:.95;letter-spacing:-2px;color:var(--white)}
  .ev-title .g{color:var(--g-brand)}
  .ev-date{margin-top:12px;font-size:13px;letter-spacing:2px;font-weight:700;text-transform:uppercase;color:var(--g-brand)}
  /* ── PROMO HAMILTON + LATAS ── */
  .promo{background:var(--white);padding:70px 0 0;overflow:hidden}
  .promo-stage{position:relative;max-width:1000px;height:560px;margin:0 auto}
  .promo-man{
    position:absolute;left:50%;bottom:65px;transform:translateX(-50%);height:470px;width:auto;z-index:5;
    opacity:0;transition:opacity .7s ease .05s;
  }
  .promo-can{
    position:absolute;left:50%;height:310px;width:auto;z-index:1;
    transform-origin:50% 100%;
    transform:translate(-50%,50px) rotate(0deg) scale(.7);opacity:0;
    transition:transform .95s cubic-bezier(.25,.46,.45,.94),opacity .6s ease;
  }
  .promo-can.c1{bottom:255px;transition-delay:.15s}
  .promo-can.c2{bottom:265px;transition-delay:.25s}
  .promo-can.c3{bottom:275px;transition-delay:.35s}
  .promo-can.c4{bottom:265px;transition-delay:.45s}
  .promo-can.c5{bottom:255px;transition-delay:.55s}
  .promo-stage.in .promo-man{opacity:1}
  .promo-stage.in .c1{transform:translate(calc(-50% - 128px),0) rotate(-32deg);opacity:1}
  .promo-stage.in .c2{transform:translate(calc(-50% - 72px),0) rotate(-16deg);opacity:1}
  .promo-stage.in .c3{transform:translate(-50%,0) rotate(0deg);opacity:1}
  .promo-stage.in .c4{transform:translate(calc(-50% + 72px),0) rotate(16deg);opacity:1}
  .promo-stage.in .c5{transform:translate(calc(-50% + 128px),0) rotate(32deg);opacity:1}
  .promo-fade{
    position:absolute;left:0;right:0;bottom:0;height:240px;z-index:9;pointer-events:none;
    background:linear-gradient(to top,
      #fff 0%,#fff 38%,
      rgba(255,255,255,.92) 50%,
      rgba(255,255,255,.72) 63%,
      rgba(255,255,255,.45) 77%,
      rgba(255,255,255,.18) 90%,
      rgba(255,255,255,0) 100%);
  }
  /* ==================== EXPERIENCIA PREMIUM (add-on) ==================== */
  /* estados iniciais aplicados SO quando o motor de animacao esta ativo   */
  html.anim-ready .hdr-logo,
  html.anim-ready .hero-eye,
  html.anim-ready .hero-sub,
  html.anim-ready .s-tag,
  html.anim-ready .s-sub,
  html.anim-ready .cta-big,
  html.anim-ready .ftr-logo,
  html.anim-ready .ftr-copy,
  html.anim-ready .ftr-links,
  html.anim-ready .ath-feature,
  html.anim-ready .ev-card,
  html.anim-ready .car-title{opacity:0;transform:translate3d(0,26px,0)}
  html.anim-ready .hdr-nav a{opacity:0;transform:translate3d(0,-10px,0)}
  html.anim-ready .s-card{opacity:0;transform:translate3d(0,42px,0) rotate(-1deg) scale(.97)}
  html.anim-ready .ath-card{opacity:0;transform:translate3d(0,30px,0) scale(.985)}
  html.anim-ready .hero-h1,
  html.anim-ready .s-title,
  html.anim-ready .cta-strip h3{opacity:0}
  html.anim-ready .car-stage{opacity:0;transform:scale(.96)}
  html.anim-ready .div{transform:scaleX(0);transform-origin:left center}
  .char{display:inline-block;will-change:transform,opacity}
  /* HERO cinematografico */
  .hero{position:relative;overflow:hidden;isolation:isolate}
  .hero-eye,.hero-h1,.hero-sub{position:relative;z-index:2}
  .hero-h1{text-shadow:0 0 30px rgba(62,196,0,.12)}
  .hero-glow{position:absolute;z-index:1;left:50%;top:40%;width:120vw;height:120vw;max-width:1050px;max-height:1050px;transform:translate3d(-50%,-50%,0);pointer-events:none;background:radial-gradient(circle,rgba(62,196,0,.30) 0%,rgba(62,196,0,.10) 33%,transparent 62%);filter:blur(4px);animation:heroGlow 5.5s ease-in-out infinite;will-change:transform}
  .hero-particles{position:absolute;inset:0;z-index:1;pointer-events:none}
  .hero-slides{position:absolute;inset:0;z-index:0;overflow:hidden;background:#000}
  .hero-slide{position:absolute;inset:0;opacity:0;transition:opacity 1.6s ease;will-change:opacity}
  .hero-slide img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;display:block}
  .hero-slide.on{opacity:1}
  .hero-slides-ov{position:absolute;inset:0;background:radial-gradient(ellipse at 50% 42%,rgba(0,0,0,.56) 0%,rgba(0,0,0,.85) 100%)}
  @keyframes heroGlow{0%,100%{transform:translate3d(-50%,-50%,0) scale(1)}50%{transform:translate3d(-50%,-50%,0) scale(1.09)}}
  /* GLOW pulsante + hover premium nos botoes */
  .hdr-cta{transition:background .2s,transform .25s cubic-bezier(.2,.7,.3,1),box-shadow .25s ease;animation:softPulse 4s ease-in-out infinite}
  .cta-big{transition:background .2s,color .2s,transform .25s cubic-bezier(.2,.7,.3,1),box-shadow .25s ease;animation:softPulse 4s ease-in-out infinite}
  @keyframes softPulse{0%,100%{box-shadow:0 0 0 rgba(62,196,0,0)}50%{box-shadow:0 0 22px rgba(62,196,0,.35)}}
  .hdr-cta:hover,.cta-big:hover{transform:translate3d(0,-2px,0) scale(1.05);box-shadow:0 0 26px rgba(62,196,0,.6),0 8px 24px rgba(0,0,0,.35)}
  /* CARDS: glow + brilho que segue o cursor */
  .s-card{transition:transform .3s,box-shadow .35s ease;will-change:transform}
  .s-card:hover{box-shadow:0 0 26px rgba(62,196,0,.35),0 18px 40px rgba(0,0,0,.28)}
  .s-card::before{content:"";position:absolute;inset:0;z-index:1;pointer-events:none;opacity:0;transition:opacity .35s ease;background:radial-gradient(200px circle at var(--mx,50%) var(--my,50%),rgba(62,196,0,.22),transparent 60%)}
  .s-card:hover::before{opacity:1}
  /* RIPPLE */
  .btn-ripple{position:relative;overflow:hidden}
  .btn-ripple .ripple{position:absolute;border-radius:50%;background:rgba(255,255,255,.45);transform:translate(-50%,-50%) scale(0);pointer-events:none;animation:rippleGo .6s ease-out forwards}
  @keyframes rippleGo{to{transform:translate(-50%,-50%) scale(1);opacity:0}}
  @media (prefers-reduced-motion: reduce){
    .hero-glow,.hdr-cta,.cta-big{animation:none !important}
  }

  [hero-slideshow.js](https://github.com/user-attachments/files/33225606/hero-slideshow.js)
[produtos.js](https://github.com/user-attachments/files/33225607/produtos.js)[animacoes.js](https://github.com/user-attachments/files/33225610/animacoes.js)
[slider-esportes.js](https://github.com/user-attachments/files/33225609/slider-esportes.js)
[promo-latas.js](https://github.com/user-attachments/files/33225608/promo-latas.js)

[gsap.min.js](https://github.com/user-attachments/files/33225620/gsap.min.js)
[lenis.min.js](https://github.com/user-attachments/files/33225621/lenis.min.js)[split-type.min.js](https://github.com/user-attachments/files/33225623/split-type.min.js)
[ScrollTrigger.min.js](https://github.com/user-attachments/files/33225622/ScrollTrigger.min.js)

<img width="231" height="600" alt="promo-lata-05" src="https://github.com/user-attachments/assets/04d89f0a-27e0-4ebc-aa7c-d979f3e0b5e7" />
<img width="249" height="600" alt="promo-lata-04" src="https://github.com/user-attachments/assets/de1cca13-97e1-4916-9a26-db5b74168ecc" />
<img width="247" height="600" alt="promo-lata-03" src="https://github.com/user-attachments/assets/7183b255-d15b-4e2c-8a24-901a66201833" />
<img width="236" height="600" alt="promo-lata-02" src="https://github.com/user-attachments/assets/fd9960d7-17cb-49f2-ae65-25b3d20fbeb7" />
<img width="247" height="600" alt="promo-lata-01" src="https://github.com/user-attachments/assets/c59a259c-7e21-4572-a7e8-41d1932c855b" />
<img width="938" height="900" alt="promo-atleta" src="https://github.com/user-attachments/assets/76fe6fce-26f3-49b5-acf5-3bef86cdeb82" />
<img width="3840" height="2160" alt="logo-monster" src="https://github.com/user-attachments/assets/16eaa0ee-750d-461a-bc64-2a3eb2bb602e" />
<img width="395" height="564" alt="lata-zero-ultra" src="https://github.com/user-attachments/assets/d03b52cd-c61b-4462-b803-97023f835f19" />
<img width="395" height="564" alt="lata-ultra-watermelon" src="https://github.com/user-attachments/assets/ae50db54-34b3-4267-8799-6669e2cee10f" />
<img width="395" height="564" alt="lata-ultra-violet" src="https://github.com/user-attachments/assets/ca30b567-9521-4319-8718-0d2f1db20840" />
<img width="395" height="564" alt="lata-ultra-fiesta-mango" src="https://github.com/user-attachments/assets/18025f64-1066-498e-91d7-d8b3a3a94583" />
<img width="395" height="564" alt="lata-rio-punch" src="https://github.com/user-attachments/assets/b4c14d29-f0fa-4834-95b4-ed437729ac54" />
<img width="395" height="564" alt="lata-monster-original" src="https://github.com/user-attachments/assets/5b879814-1002-45df-b658-f0e6a580186e" />
<img width="395" height="564" alt="lata-mango-loco" src="https://github.com/user-attachments/assets/1e7f9633-bde5-4418-a752-14b07e802b86" />
<img width="395" height="564" alt="lata-absolutely-zero" src="https://github.com/user-attachments/assets/d3f2d6b9-19ea-40be-9280-2a5aaf748928" />
<img width="1920" height="1080" alt="hero-04" src="https://github.com/user-attachments/assets/d1e23a1e-7c68-4a3a-abc2-38b6cfc38e1a" />
<img width="1177" height="662" alt="hero-03" src="https://github.com/user-attachments/assets/3083b4e4-e553-49d3-b9d7-90f0c536ac39" />
<img width="1352" height="900" alt="hero-02" src="https://github.com/user-attachments/assets/f7587d62-9f56-4d1c-83e9-d10793779fb3" />
<img width="1260" height="840" alt="hero-01" src="https://github.com/user-attachments/assets/e548a7cc-55a3-412f-90fc-7f157a29951b" />
<img width="1024" height="683" alt="evento-01" src="https://github.com/user-attachments/assets/4d71320b-6a52-4f9b-aa60-ce45d6807162" />
<img width="600" height="800" alt="esporte-08" src="https://github.com/user-attachments/assets/f95a4a7e-8db5-4d51-8d4d-47c9a9638055" />
<img width="600" height="800" alt="esporte-07" src="https://github.com/user-attachments/assets/983bca7f-6438-4f91-afd7-3069687db14f" />
<img width="600" height="800" alt="esporte-06" src="https://github.com/user-attachments/assets/486bf511-804e-452f-a78e-0975e09c6d51" />
<img width="600" height="800" alt="esporte-05" src="https://github.com/user-attachments/assets/5aacdfc1-2d90-44f4-a227-f2e868e6aea2" />
<img width="600" height="800" alt="esporte-04" src="https://github.com/user-attachments/assets/37c6e53c-1bf4-423e-b7fe-3717a0c82159" />
<img width="600" height="800" alt="esporte-03" src="https://github.com/user-attachments/assets/b92c3f2f-54d3-4f8f-ba9a-02449728509d" />
<img width="600" height="800" alt="esporte-02" src="https://github.com/user-attachments/assets/bde1c3bf-6939-4746-a33f-13bf2e3e2941" />
<img width="600" height="800" alt="esporte-01" src="https://github.com/user-attachments/assets/27754c84-b6f3-4aef-acfc-55d6685868de" />
<img width="36" height="24" alt="bandeira-09" src="https://github.com/user-attachments/assets/47ee399d-937f-4958-b74a-9a935f7e15dd" />
<img width="36" height="24" alt="bandeira-07" src="https://github.com/user-attachments/assets/b4a60d96-6862-49cc-bce2-762bc973b4eb" />
<img width="36" height="24" alt="bandeira-06" src="https://github.com/user-attachments/assets/1c77c3b5-9cda-427e-9698-0fec37b1062c" />
<img width="36" height="24" alt="bandeira-04" src="https://github.com/user-attachments/assets/98ba8fea-54d1-486a-8054-1dca580bb5c7" />
<img width="36" height="24" alt="bandeira-03" src="https://github.com/user-attachments/assets/10e6afb0-a6a3-44e3-ae66-6a44f2c96269" />
<img width="36" height="24" alt="bandeira-02" src="https://github.com/user-attachments/assets/f0bc1f06-dc5c-4c0c-999b-691526988397" />
<img width="36" height="24" alt="bandeira-01" src="https://github.com/user-attachments/assets/c0d231e3-65bc-4212-9aec-78d2b8657097" />
<img width="984" height="655" alt="atleta-destaque" src="https://github.com/user-attachments/assets/bc1fed30-648d-42f6-8dcf-0af2a2309632" />
<img width="900" height="506" alt="atleta-10" src="https://github.com/user-attachments/assets/1f4d1fc6-7677-436b-b7c7-375a2a7317ca" />
<img width="900" height="599" alt="atleta-09" src="https://github.com/user-attachments/assets/6bd3f6b1-ee90-45a7-ae3f-ce6ee84d02c1" />
<img width="858" height="726" alt="atleta-08" src="https://github.com/user-attachments/assets/0e835115-0034-42f9-878a-ce7ed77b5c3a" />
<img width="481" height="481" alt="atleta-07" src="https://github.com/user-attachments/assets/2b98d0e6-2357-44e1-b6b3-7f88ed827330" />
<img width="768" height="512" alt="atleta-06" src="https://github.com/user-attachments/assets/799e2d89-c143-48cc-8639-201f8376b626" />
<img width="900" height="600" alt="atleta-05" src="https://github.com/user-attachments/assets/78e9a871-1e5b-4f8a-a686-f17c94386357" />
<img width="900" height="599" alt="atleta-04" src="https://github.com/user-attachments/assets/7f5ef810-ffe1-418e-830f-bb42b04f7d20" />
<img width="640" height="960" alt="atleta-03" src="https://github.com/user-attachments/assets/e3b01507-4afd-48d7-b872-e18b3cf77f41" />
<img width="640" height="640" alt="atleta-02" src="https://github.com/user-attachments/assets/03596b10-aa87-4cbf-98e5-e7959501151c" />

