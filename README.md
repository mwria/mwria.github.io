<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
<title>Aniversário da Mabi!!!!!!!!!!</title>
<style>
/* RESET E ESTILOS GLOBAIS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: radial-gradient(circle at 10% 20%, #0a0a0a, #000000);
    font-family: 'Segoe UI', 'Poppins', system-ui, sans-serif;
    overflow-x: hidden;
    color: #f0f0f0;
}

/* MENU */
.menu {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 30px 20px;
    background: rgba(0,0,0,0.85);
    backdrop-filter: blur(8px);
    position: sticky;
    top: 0;
    z-index: 100;
    border-bottom: 1px solid rgba(255,105,180,0.4);
}

button {
    padding: 12px 28px;
    border: none;
    border-radius: 60px;
    background: linear-gradient(135deg, #ff1493, #ff69b4);
    color: white;
    font-size: 1.1rem;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 5px 18px rgba(255,20,147,0.4);
    transition: all 0.25s ease;
}

button:hover {
    transform: translateY(-4px) scale(1.02);
}

/* BIG HUG - zoom grande (3.5x) */
.chan {
    position: fixed;
    width: 140px;
    pointer-events: none;
    z-index: 999;
    animation: zoomBIG 1.2s ease-out forwards;
}

@keyframes zoomBIG {
    0% { transform: scale(0) rotate(0deg); opacity: 0; }
    20% { opacity: 1; }
    100% { transform: scale(3.5) rotate(12deg); opacity: 1; }
}

/* SEÇÕES */
.section {
    padding: 50px 30px;
    max-width: 1400px;
    margin: 0 auto;
}

h1 {
    text-align: center;
    font-size: 3.2rem;
    background: linear-gradient(135deg, #fff, #ffb6d9);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    margin-bottom: 15px;
}

.subtitle {
    text-align: center;
    color: #ffbfdf;
    font-size: 1.2rem;
    margin-bottom: 45px;
}

/* GALERIA NÓS */
.gallery {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 18px;
}

.gallery img, .gallery .bi-card {
    width: 100%;
    height: 260px;
    object-fit: cover;
    border-radius: 28px;
    transition: all 0.35s ease;
    box-shadow: 0 8px 18px rgba(0,0,0,0.5);
    border: 1px solid rgba(255,192,203,0.3);
    cursor: pointer;
}

.gallery img:hover, .gallery .bi-card:hover {
    transform: scale(1.05) translateY(-6px);
    box-shadow: 0 0 28px #ff69b4;
}

/* OVERLAY BISSEXUAL – fundo com 30% opacidade via pseudo-elemento, fotos 100% */
.bi-overlay {
    position: fixed;
    inset: 0;
    z-index: 10000;
    display: none;
    justify-content: center;
    align-items: center;
}

.bi-overlay.active {
    display: flex;
}

/* Pseudo-elemento para o fundo da bandeira com opacidade 30% */
.bi-overlay::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(to bottom, #d60270 0%, #d60270 33%, #9b4f96 33%, #9b4f96 66%, #0038a8 66%, #0038a8 100%);
    opacity: 0.3;
    z-index: -1;
}

/* Container das fotos extras – 100% opacas */
.bi-photos {
    position: relative;
    z-index: 10001;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    background: transparent;
    padding: 30px;
    border-radius: 50px;
    width: 90%;
    max-width: 1000px;
    margin: auto;
    overflow: visible;
}

.bi-photos img {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 25px;
    box-shadow: 0 0 20px rgba(255,20,147,0.8);
    transition: 0.2s;
    border: 2px solid #ff99cc;
    opacity: 1 !important;
    background: white;
}

.bi-photos img:hover {
    transform: scale(1.03);
}

.close-bi {
    position: fixed;
    top: 25px;
    right: 30px;
    z-index: 10002;
    background: #ff1493;
    border: none;
    font-size: 2rem;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 0 15px white;
    color: white;
}

/* BINDER */
#binderSection {
    background: #ffe6f2;
    color: #1e1e1e;
    border-radius: 50px 50px 30px 30px;
    margin: 40px 20px;
    padding: 30px 20px;
}

#binderSection h1 {
    color: #ff1493;
    text-shadow: none;
}

.binder-stats {
    text-align: center;
    font-size: 1.8rem;
    font-weight: bold;
    background: #fff0f7;
    display: inline-block;
    padding: 10px 25px;
    border-radius: 40px;
    margin: 15px auto;
    box-shadow: inset 0 0 5px #ff99cc, 0 5px 10px rgba(0,0,0,0.1);
}

#cardDisplay {
    text-align: center;
    margin: 30px auto;
    background: #fff0f7;
    padding: 25px;
    border-radius: 45px;
    width: fit-content;
    max-width: 95%;
}

#cardDisplay img {
    max-width: 260px;
    border-radius: 30px;
    box-shadow: 0 0 25px #ff66b2;
    border: 3px solid white;
    aspect-ratio: 2 / 3;
    object-fit: cover;
}

.card-buttons {
    display: flex;
    gap: 20px;
    justify-content: center;
    margin-top: 20px;
}

.card-buttons button {
    font-size: 2rem;
    width: 70px;
    height: 70px;
    border-radius: 50%;
    padding: 0;
}

.binder-page {
    background: #fff9fc;
    border-radius: 40px;
    padding: 25px;
    margin-top: 35px;
}

#binder {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
    margin-top: 25px;
}

.binder-card {
    background: white;
    border-radius: 25px;
    padding: 12px;
    box-shadow: 0 5px 12px rgba(0,0,0,0.1);
    transition: 0.2s;
}

.binder-card img {
    width: 100%;
    aspect-ratio: 2 / 3;
    object-fit: cover;
    border-radius: 18px;
}

.binder-card:hover {
    transform: scale(1.02);
    box-shadow: 0 0 18px hotpink;
}

/* BILLBOARD */
#chartsSection {
    background: #efefef;
    padding: 80px 30px;
    color: black;
}

.billboard-title {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 40px;
    margin-bottom: 60px;
}

.billboard-title h1 {
    font-size: 75px;
    color: #3f47b8;
    font-weight: 900;
    background: none;
    -webkit-background-clip: unset;
    color: #3f47b8;
}

.line {
    flex: 1;
    height: 10px;
    background: #3f47b8;
}

.charts-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 35px;
}

.chart-card {
    background: #f8f8f8;
    border: 2px solid #ddd;
    padding: 25px;
    box-shadow: 12px 12px 0 rgba(0,0,0,0.08);
    transition: 0.3s;
}

.chart-card:hover {
    transform: translateY(-8px);
}

.top-info {
    display: flex;
    gap: 25px;
    align-items: flex-start;
}

.top-info img {
    width: 170px;
    height: 170px;
    object-fit: cover;
}

.rank-number {
    font-size: 70px;
    font-weight: 900;
}

.trend {
    font-size: 28px;
    font-weight: 900;
    padding: 8px 16px;
    border-radius: 999px;
}

.up { background: #d8ffd8; color: #119911; }
.down { background: #ffd8d8; color: #cc2222; }
.same { background: #dfe1ff; color: #3f47b8; }

.chart-text h2 {
    font-size: 42px;
}
.chart-text p {
    font-size: 28px;
    color: #444;
}

.stats {
    margin-top: 40px;
    display: grid;
    grid-template-columns: repeat(3,1fr);
    text-align: center;
    border-top: 2px solid #ddd;
    padding-top: 25px;
}
.stats div { border-right: 1px solid #ddd; }
.stats div:last-child { border-right: none; }
.stats span { color: #4b53c5; font-weight: 900; font-size: 18px; }
.stats strong { font-size: 55px; }

/* TIMELINE */
#timelineSection {
    background: #111;
    padding: 80px 20px;
}
.timeline-title {
    text-align: center;
    font-size: 55px;
    color: white;
    text-shadow: 0 0 20px hotpink;
}
.timeline-sub {
    text-align: center;
    color: #ffb6d9;
    margin-bottom: 60px;
    font-size: 22px;
}
.timeline {
    max-width: 900px;
    margin: auto;
    position: relative;
}
.timeline::before {
    content: "";
    position: absolute;
    left: 50%;
    top: 0;
    width: 6px;
    height: 100%;
    background: hotpink;
    transform: translateX(-50%);
    border-radius: 20px;
}
.timeline-item {
    width: 45%;
    background: #1b1b1b;
    padding: 25px;
    border-radius: 25px;
    margin-bottom: 50px;
    position: relative;
    opacity: 0;
    transform: translateY(80px);
    transition: 1s;
    box-shadow: 0 0 20px rgba(255,105,180,0.3);
}
.timeline-item.show {
    opacity: 1;
    transform: translateY(0);
}
.timeline-item.left {
    left: 0;
}
.timeline-item.right {
    left: 55%;
}
.timeline-year {
    font-size: 55px;
    font-weight: bold;
    color: hotpink;
}
.timeline-text {
    margin-top: 10px;
    font-size: 22px;
    line-height: 1.5;
}

/* PLAYLIST */
#playlistSection {
    background: #ffd9ec;
    color: black;
    padding: 80px 20px;
}
.playlist-title {
    text-align: center;
    font-size: 60px;
    color: #ff1493;
}
.playlist-sub {
    text-align: center;
    font-size: 22px;
    margin-bottom: 40px;
}
.spotify-box {
    max-width: 900px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 30px;
    box-shadow: 0 0 30px rgba(0,0,0,0.15);
}

/* ===== POP-UP DE ANIVERSÁRIO ===== */
.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.85);
    z-index: 20000;
    justify-content: center;
    align-items: center;
    backdrop-filter: blur(8px);
}
.modal.active {
    display: flex;
}
.modal-content {
    background: linear-gradient(145deg, #1e1a2e, #0f0c1a);
    max-width: 550px;
    width: 90%;
    padding: 40px 30px;
    border-radius: 50px;
    text-align: center;
    border: 2px solid #ff69b4;
    box-shadow: 0 0 50px rgba(255,105,180,0.6);
    animation: fadeInUp 0.5s ease;
}
.modal-content p {
    font-size: 1.4rem;
    line-height: 1.5;
    color: #ffe0f0;
    margin: 20px 0;
}
.modal-content button {
    background: #ff1493;
    border: none;
    padding: 12px 30px;
    font-size: 1.2rem;
    margin-top: 15px;
    border-radius: 40px;
    cursor: pointer;
}
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* RESPONSIVO */
@media (max-width: 1100px) {
    .charts-grid { grid-template-columns: 1fr; }
}
@media (max-width: 900px) {
    .gallery { grid-template-columns: repeat(2, 1fr); }
    #binder { grid-template-columns: repeat(2, 1fr); }
    .bi-photos { grid-template-columns: repeat(2, 1fr); gap: 15px; padding: 20px; width: 95%; }
    .billboard-title h1 { font-size: 45px; }
    .top-info { flex-direction: column; }
    .top-info img { width: 100%; height: auto; }
    .rank-number { font-size: 50px; }
    .timeline::before { left: 20px; }
    .timeline-item { width: calc(100% - 60px); left: 40px !important; }
    .modal-content p { font-size: 1.1rem; }
}
</style>
</head>
<body>

<!-- POP-UP DE ANIVERSÁRIO (aparece ao carregar) -->
<div id="birthdayModal" class="modal">
    <div class="modal-content">
        <p>💖 AMIGA, obrigada por tudo que você já fez e continua fazendo por mim. 💖</p>
        <p>Uma vez você me disse que deve ser divertido ter uma irmã, saiba que o que a gente tem é mil vezes mais forte e divertido que a maioria das relações.</p>
        <p>Eu amo você e amo seu aniversário por poder comemorar a maravilha do alinhamento milenar que a gente tem.</p>
        <p>Fiz esse site pra você se divertir um pouco. </p>
        <button onclick="closeModal()"></button>
    </div>
</div>

<div class="menu">
    <button onclick="startBigHug()">BIG HUG </button>
    <button onclick="scrollToNos()">US </button>
    <button onclick="scrollToBinder()">BINDER</button>
    <button onclick="scrollToCharts()">CHARTS</button>
    <button onclick="scrollToTimeline()">TIMELINE</button>
    <button onclick="scrollToPlaylist()">PLAYLIST</button>
</div>

<!-- NÓS -->
<section class="section" id="nosSection">
    <h1>✦ NÓS ✦</h1>
    <p class="subtitle">everywhere all around the world ♡</p>
    <div class="gallery" id="gallery"></div>
</section>

<!-- BINDER -->
<section class="section" id="binderSection">
    <h1>PHOTOCARDS</h1>
    <div style="text-align:center;">
        <button onclick="drawCard()"> ABRIR PACOTE</button>
        <button onclick="resetBinder()" style="background:#c73b6b; margin-left:15px;">🗑️ RESETAR</button>
    </div>
    <div id="cardDisplay"></div>
    <div class="binder-stats" id="binderStats">0 / 0 photocards</div>
    <div class="binder-page">
        <h2 style="text-align:center;">💗 MINHA COLEÇÃO 💗</h2>
        <div id="binder"></div>
    </div>
</section>

<!-- NAMORADOS DA MABI CHARTS -->
<section id="chartsSection">
    <div class="billboard-title"><div class="line"></div><h1>Namorados da Mabi™</h1><div class="line"></div></div>
    <div class="charts-grid" id="chartsGrid"></div>
</section>

<!-- TIMELINE -->
<section id="timelineSection">
    <h1 class="timeline-title">COISAS QUE DURARAM MENOS QUE NOSSA AMIZADE</h1>
    <p class="timeline-sub">13 anos insuperáveis infelizmente</p>
    <div class="timeline" id="timeline"></div>
</section>

<!-- PLAYLIST -->
<section id="playlistSection">
    <h1 class="playlist-title">PLAYLIST DA NOSSA AMIZADE</h1>
    <p class="playlist-sub">trilha sonora oficial do caos</p>
    <div class="spotify-box">
        <iframe style="border-radius:20px" src="https://open.spotify.com/embed/playlist/5Sk3nemYaY0ElR5M7R5kNO" width="100%" height="500" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </div>
</section>

<!-- OVERLAY BISSEXUAL -->
<div id="biOverlay" class="bi-overlay">
    <button class="close-bi" onclick="closeBiOverlay()">✖</button>
    <div class="bi-photos" id="biPhotos"></div>
</div>

<script>
// ==================== POP-UP ====================
function closeModal() {
    document.getElementById("birthdayModal").classList.remove("active");
}
window.addEventListener("load", () => {
    document.getElementById("birthdayModal").classList.add("active");
});

// ==================== GALERIA "NÓS" ====================
const galleryImages = [
  "https://i.ibb.co/VYsPJnc1/8aa304d5e88fb71859ed5b168c8d3605.jpg",
  "https://i.ibb.co/XxNfH4b9/8d19ca3dc311addf37e1e506e6680483.jpg",
  "https://i.ibb.co/ynzGTrt6/7e2bb6b938636b036c2bfbf12d3d44ff.jpg",
  "https://i.ibb.co/nsVJ6p6w/3fa01f52623857fab86a2684929a4e0c.jpg",
  "https://i.ibb.co/mV2b2hnd/e01fb1efe9d1038b128709968e92a7e5.jpg",
  "https://i.ibb.co/3mc6hb6B/5d674b324fb74ab3670af1f156f29025.jpg",
  "https://i.ibb.co/C5YkW2V0/23f5c825f9bf0a6c08b6957793226d02.jpg",
  "https://i.ibb.co/Gv48ZdWg/86ca2d3c9c427940a3db6a65c97bcec8.jpg",
  "https://i.ibb.co/4nKstCX6/40e01b84b05436504bda30c7f8b17862.jpg",
  "https://i.ibb.co/Y4LQLQRt/f27f3cd49ae19eaff495d0924280795e.jpg",
  "https://i.ibb.co/pvPZqh17/8a63de03598873a5e7d58e9e0b91be56.jpg",
  "https://i.ibb.co/VYTN2VsD/8f65e79ff12d76fe9a90081d90c7d811-1.jpg",
  "https://i.ibb.co/jZhzZmVN/872eeeb57f97aed9e02ddc682a832653.jpg",
  "https://i.ibb.co/TBksSQk6/1eaca39efef28551fec4ada622b2a9c3.jpg",
  "https://i.ibb.co/mCDWshVk/ecb29da94673f747d814337a0b393067.jpg",
  "https://i.ibb.co/pr07jy4J/e0d1362c76fb001195fdac2807b4e617.jpg",
  "https://i.ibb.co/jkZyCP5B/595c1922667b0def4fff8d7739fe07f6.jpg",
  "https://i.ibb.co/b5xT4Rxh/d629357bf9144eee684d241f593f28f7.jpg",
  "https://i.ibb.co/hqZfmZ4/170c10a2268e52e810cd6b07f58c71c4.jpg",
  "https://i.ibb.co/5x6P6ckm/6fd7ac9905d3806a35e630e324ae68bb.jpg",
  "https://i.ibb.co/03CHbhZ/de413a0bcbbf2da102413b1aa4de9419.jpg",
  "https://i.ibb.co/Vcyjgdfq/0ad288c6398762c6a0e40e3bfd6b8567.jpg",
  "https://i.ibb.co/Gfj3T7Fq/3cecd6e3f7705fc1eec5ebb3cb16ea90.jpg",
  "https://i.ibb.co/3m4nDcfj/671c99a94b4088ab82078e035262561e.jpg",
  "https://i.ibb.co/SX1Mkn4m/577d454dff08245f6eee09a6747f6b0c.jpg",
  "https://i.ibb.co/zHL4qXXH/f620252cb99226134c2f950e909a9790.jpg",
  "https://i.ibb.co/RV4Xm41/1e32435a4fa6c90d0232db89c4b5afda.jpg",
  "https://i.ibb.co/zTTD7WmW/b29c2c54c6b02ca9cddb80c7c9fb05b9.jpg",
  "https://i.ibb.co/nq6yybsd/ba30d5757099ba5d7be25ffdc2ba8722.jpg",
  "https://i.ibb.co/mFGDXN8T/0e2a2eee4705fb91a79b9ef44f4a96cf.jpg",
  "https://i.ibb.co/yFcwFqv8/4b85f51b8a5baeaad1f2ae4d5fc67606.jpg",
  "https://i.ibb.co/9kwzMBzT/31e3001fc8d1f44992f5fcefc2adc1f9.jpg",
  "https://i.ibb.co/M527SrdS/42a5960b1610481c90c15071d5afd7c8.jpg",
  "https://i.ibb.co/qYMdyffz/76df5f7db3cff6a78c4081c6b811f2c2.jpg",
  "https://i.ibb.co/6JZYZ8wV/df66298ebdda2e95e45813f313a0073d.jpg",
  "https://i.ibb.co/DPQmpBVh/73530bb53824f23df9566765739bd2cf.jpg",
  "https://i.ibb.co/dJ44pxz3/b19089975b186e9483dce91e505ed858.jpg",
  "https://i.ibb.co/FkGs5VYD/3fb488a76ef1176c94897f38a2c4d1e5.jpg",
  "https://i.ibb.co/zh5pSMys/786ab4c06fdc5102097294abe6610094.jpg",
  "https://i.ibb.co/Rnn3Jj6/1d92a44486e310597d7f83077901f969.jpg",
  "https://i.ibb.co/m57txdmL/b1953c0e724e39eecb9a1239b1a16e9f.jpg",
  "https://i.ibb.co/Z6fRcqpv/4f48681db301865c1dc102445971693f.jpg",
  "https://i.ibb.co/TqbxyHkf/84381b379ff86b36098897298e24b447.jpg",
  "https://i.ibb.co/mFVcfJXM/d8e6056e0455db9e1b77b9f53de50c84.jpg",
  "https://i.ibb.co/Vpq9TB8f/ccf87d65dcf9810031584244fcd35579.jpg",
  "https://i.ibb.co/9RGnq05/49bb28745d946d2e896e43590c9bd1a3.jpg",
  "https://i.ibb.co/3YVwD1Wz/469b9d6b85c8694fb79931a162df83cb.jpg",
  "https://i.ibb.co/zMrKZ80/249f51579b4d8162a1be437093272ed5.jpg",
  "https://i.ibb.co/3yftZwf0/a438a07df79412d63e7068ed54f0f8b8.jpg",
  "https://i.ibb.co/kgx4SHw2/9d4721edd76486b4a3ab4f1a0b56f9f2.jpg",
  "https://i.ibb.co/BHTBrv3p/b9522262811bd17553e96d5aae2c2a5c.jpg",
  "https://i.ibb.co/F49q1yjr/c05807b3c6664a81f7ef63246ad2a86e.jpg",
  "https://i.ibb.co/xSKB3wQW/2e76445c3af20fd646c6c06c1c902912-1.jpg",
  "https://i.ibb.co/S4r9QvzF/b95fb43d9498df67f39cee853ef1bf52.jpg",
  "https://i.ibb.co/mFtk3GHb/e3f20375c86b96dc25f30abdb75833ce-1.jpg",
  "https://i.ibb.co/bj3YJLcN/afc5db8aa1148a2428309ff725652b13.jpg",
  "https://i.ibb.co/TMy1qkLB/3bae59972b98d3fc8d05da36f76aacde-1.jpg",
  "https://i.ibb.co/G4FBfTb0/cb308cded403903aafbc33f498403958-1.jpg",
  "https://i.ibb.co/spwGpPRt/d384d0ac0af4600b3069ee78e688a379.jpg",
  "https://i.ibb.co/XrbTVfQK/1f50bfcd1c566b82d712b06e47fa3f3e-1.jpg",
  "https://i.ibb.co/GQrTXKgL/088fe361b3db47127c8ee0c1b7d90d9e-2.jpg",
  "https://i.ibb.co/4nKstCX6/40e01b84b05436504bda30c7f8b17862.jpg",
  "https://i.ibb.co/dsszhDb2/8b4a78d5a0deef2a672ea0985e182489.jpg",
  "https://i.ibb.co/WCWFzYS/e1940b4272e943e3f16b87f67f70b4ba.jpg",
  "https://i.ibb.co/Fq7ZQsFg/18eaa78167d02e2aa41e44862b13ccd6.jpg",
  "https://i.ibb.co/ynZNB8yB/9bf61043c9405ace4434c6ce362fe595.jpg",
  "https://i.ibb.co/Y7FsPMfx/0f4362c2d681575f38c6079831e683aa.jpg",
  "https://i.ibb.co/NdbCLzZv/6c0529d9735696cb30483b283c304911.jpg",
  "https://i.ibb.co/Dfqn84PG/89f6ca2a75fe54371a4aa217ff387215.jpg",
  "https://i.ibb.co/6RTbPM4h/d8b3f4a09a5a958eec604023d798d83b.jpg",
  "https://i.ibb.co/5x6P6ckm/6fd7ac9905d3806a35e630e324ae68bb.jpg",
  "https://i.ibb.co/YT2kKZK2/6f417ef71b30daa38bb57aeca7b527e8.jpg",
  "https://i.ibb.co/TxndbmMR/d48bdfde5dd79f1d1b5688bd60649133.jpg",
  "https://i.ibb.co/Wp4X3mhk/d95d923c5c2118fdb6470304559c1439.jpg",
  "https://i.ibb.co/67qbb4Tv/badad3b1cfc5c1cb557462727c895998.jpg",
  "https://i.ibb.co/RdRhs6C/7f21771b36d7ad306bff1d08825ee361.jpg",
  "https://i.ibb.co/cKFVw3dz/dfd3d9e75c24eff1b8c4f269a596dfd1.jpg",
  "https://i.ibb.co/QFXBn8gQ/383de92cb7e194537059e24981d4d3c5.jpg",
  "https://i.ibb.co/FLM1Yjdv/06da83267fc44a8b9a0bfebcd2a9d0b8.jpg",
  "https://i.ibb.co/k2TH96kw/3cf656dc5b0f2092d88d2425368b18a0.jpg"
];

const galleryDiv = document.getElementById("gallery");
galleryImages.forEach(link => {
    const img = document.createElement("img");
    img.src = link;
    galleryDiv.appendChild(img);
});

// Bandeira bi clicável
const biCard = document.createElement("div");
biCard.className = "bi-card";
biCard.style.cursor = "pointer";
biCard.innerHTML = `<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Bisexual_Pride_Flag.svg" style="width:100%; height:260px; object-fit:cover;">`;
biCard.onclick = openBiOverlay;
galleryDiv.appendChild(biCard);

// ==================== BINDER ====================
const binderCards = [
  "https://i.ibb.co/Bb5zyCM/aa0d0adae895b028f5c03b338d9bb47c.jpg",
  "https://i.ibb.co/PZG81jB3/4a31c3a1567f09a2a172cb310f74c98b.jpg",
  "https://i.ibb.co/LFq8pP5/85515793c03020019fefd376ae6c85b8.jpg",
  "https://i.ibb.co/qFJ7WvVL/37ea9202ac3081edeaf70af0bd5141f2.jpg",
  "https://i.ibb.co/hRY3z8T7/be0559cbb313ec9cd32fe63a45318602.jpg",
  "https://i.ibb.co/67bkn528/9e0e3b3b5d0800bd7b5c741d150676ac.jpg",
  "https://i.ibb.co/2mV2Mk6/24b91d6a994c17f91c531259333d65ab.jpg",
  "https://i.ibb.co/d03LcgZM/ca0d33c6adbd013216460643c0210fa9.jpg",
  "https://i.ibb.co/N6fyTdWQ/dc77d7ff279f0665e1164b97577ee358.jpg",
  "https://i.ibb.co/Xx5xHHGW/a31147cccf725f63d8a56b6de0a3acba.jpg",
  "https://i.ibb.co/qF3fw8zH/15b35e38e6eed15cc984b15eeb3c7bce.jpg",
  "https://i.ibb.co/DfTXH5pL/84846bf4bc3a650e0a4313dbfc6b4fec.jpg",
  "https://i.ibb.co/DP83P5BB/d4875bd2f5eea3dbcca710ce369d88b7.jpg",
  "https://i.ibb.co/Z1mhLqdB/b2818f180fce9f4de7c9b56576b3b412.jpg",
  "https://i.ibb.co/bMmrh9nn/bc0143ee458e386e95630aad5383e517.jpg",
  "https://i.ibb.co/MyC78qKT/81c7ddfe422f267b479c181f72865816.jpg",
  "https://i.ibb.co/JWk1zCfk/08d44e68d8415f79ca13079b13d9605d.jpg",
  "https://i.ibb.co/jvS05YQG/50eee8977ca9ec43128b957624333434.jpg",
  "https://i.ibb.co/tw815B8F/ead2a671e066fd59ef15abe7d6733075.jpg",
  "https://i.ibb.co/bjKytTJ6/7880ab22b0bc4353911b954e51a8f9fe.jpg",
  "https://i.ibb.co/svR29GW5/30b4a25bba7c0c3439ab7d56ba860aa7.jpg",
  "https://i.ibb.co/KxYDp3VK/049fc42a70f9d8b08259f89b4f799093.jpg",
  "https://i.ibb.co/WNFkx4BS/4bbc9ab622fbde11df7d174790e2ef70.jpg",
  "https://i.ibb.co/ZRWjX9DD/e7e2bd7fdb1b51352897ff1b3370ac5d.jpg",
  "https://i.ibb.co/Qjq2kpXk/0b630450a8fc01a898059b78346035d7.jpg",
  "https://i.ibb.co/3yPLXvGR/d27fbe1083e3925a12857e5d4a650af3.jpg",
  "https://i.ibb.co/Cs7n6P0n/be44f50a27c54dd32a6ac1f3d7eed60b.jpg",
  "https://i.ibb.co/4n9JjXzT/2c021ec31ead5ed2439ef1285c760938.jpg",
  "https://i.ibb.co/HDxKVJqZ/ba2b1c4a40abc551d8d952b45c1f73d9.jpg",
  "https://i.ibb.co/QjpWNVkf/01b803ca9fc195cd062af907e165bee8.jpg",
  "https://i.ibb.co/MyKjHZw8/c032e64f1dddd3577400d1b77e43db9e.jpg",
  "https://i.ibb.co/MySc2VHk/20981addfb5aaf90801b30edda77d5af.jpg",
  "https://i.ibb.co/27gYZwKf/f6e876e079711f77e790113f78fd7871.jpg",
  "https://i.ibb.co/fzbjnhRK/f5dd7ef8a4c2e8f53ce56f3c7e59b1f1.jpg",
  "https://i.ibb.co/SwgscGQJ/22c88043a6e0a831dbdf47f08817d334.jpg",
  "https://i.ibb.co/6RMQP34j/0b3790045ecfe471f81d1889bc14b469.jpg",
  "https://i.ibb.co/Bb5zyCM/aa0d0adae895b028f5c03b338d9bb47c.jpg",
  "https://i.ibb.co/PZG81jB3/4a31c3a1567f09a2a172cb310f74c98b.jpg",
  "https://i.ibb.co/LFq8pP5/85515793c03020019fefd376ae6c85b8.jpg",
  "https://i.ibb.co/qFJ7WvVL/37ea9202ac3081edeaf70af0bd5141f2.jpg",
  "https://i.ibb.co/67bkn528/9e0e3b3b5d0800bd7b5c741d150676ac.jpg",
  "https://i.ibb.co/2mV2Mk6/24b91d6a994c17f91c531259333d65ab.jpg",
  "https://i.ibb.co/d03LcgZM/ca0d33c6adbd013216460643c0210fa9.jpg",
  "https://i.ibb.co/N6fyTdWQ/dc77d7ff279f0665e1164b97577ee358.jpg",
  "https://i.ibb.co/Xx5xHHGW/a31147cccf725f63d8a56b6de0a3acba.jpg",
  "https://i.ibb.co/qF3fw8zH/15b35e38e6eed15cc984b15eeb3c7bce.jpg",
  "https://i.ibb.co/DfTXH5pL/84846bf4bc3a650e0a4313dbfc6b4fec.jpg",
  "https://i.ibb.co/DP83P5BB/d4875bd2f5eea3dbcca710ce369d88b7.jpg",
  "https://i.ibb.co/Z1mhLqdB/b2818f180fce9f4de7c9b56576b3b412.jpg",
  "https://i.ibb.co/bMmrh9nn/bc0143ee458e386e95630aad5383e517.jpg",
  "https://i.ibb.co/MyC78qKT/81c7ddfe422f267b479c181f72865816.jpg",
  "https://i.ibb.co/JWk1zCfk/08d44e68d8415f79ca13079b13d9605d.jpg",
  "https://i.ibb.co/jvS05YQG/50eee8977ca9ec43128b957624333434.jpg",
  "https://i.ibb.co/tw815B8F/ead2a671e066fd59ef15abe7d6733075.jpg",
  "https://i.ibb.co/bjKytTJ6/7880ab22b0bc4353911b954e51a8f9fe.jpg",
  "https://i.ibb.co/svR29GW5/30b4a25bba7c0c3439ab7d56ba860aa7.jpg",
  "https://i.ibb.co/KxYDp3VK/049fc42a70f9d8b08259f89b4f799093.jpg",
  "https://i.ibb.co/WNFkx4BS/4bbc9ab622fbde11df7d174790e2ef70.jpg",
  "https://i.ibb.co/ZRWjX9DD/e7e2bd7fdb1b51352897ff1b3370ac5d.jpg",
  "https://i.ibb.co/Qjq2kpXk/0b630450a8fc01a898059b78346035d7.jpg",
  "https://i.ibb.co/3yPLXvGR/d27fbe1083e3925a12857e5d4a650af3.jpg",
  "https://i.ibb.co/Cs7n6P0n/be44f50a27c54dd32a6ac1f3d7eed60b.jpg",
  "https://i.ibb.co/4n9JjXzT/2c021ec31ead5ed2439ef1285c760938.jpg",
  "https://i.ibb.co/HDxKVJqZ/ba2b1c4a40abc551d8d952b45c1f73d9.jpg",
  "https://i.ibb.co/SX97RpFg/06940cd301fb5e3aac9596af42d4bbfe.jpg",
  "https://i.ibb.co/zVFYM9cb/bbb4118d2dc5e9a0a45df37758139e5a.jpg",
  "https://i.ibb.co/rKNx3dpJ/14257235304b35954836e10bcf572e12.jpg",
  "https://i.ibb.co/xqcVsTdB/ef9a88eccbe4c277976e028fc2bba8ca.jpg",
  "https://i.ibb.co/RG7FPz1q/171a7915d11038274b3661e741155a6a.jpg",
  "https://i.ibb.co/tMcMn5Fg/fa2c20f57a34b2061123b799823e3840.jpg",
  "https://i.ibb.co/zhTcZfdP/cecc0003b6cd90dd74a12fcb29638f7f.jpg",
  "https://i.ibb.co/tTyxvm06/daf6a48266f5b84b891f4942a09448b1.jpg",
  "https://i.ibb.co/Zpkr6S6V/3ff4233ab7a3465dd9b55dc52233f8f3.jpg",
  "https://i.ibb.co/pvcJfNB5/590dd2310a66b1f6d677e9afa4dffe94.jpg",
  "https://i.ibb.co/PvQNhYFh/7088925aeed152766784f61a31bd7511.jpg",
  "https://i.ibb.co/1fnYZY1f/e19eb5b56d473cd98d05f12876b92e1c.jpg",
  "https://i.ibb.co/tPYFMJxb/bd44cec259bdb2fd0eaa6a5bde5eed46.jpg",
  "https://i.ibb.co/PzC838Jy/64a413a87c72d2a941bead88be22e88f.jpg",
  "https://i.ibb.co/zWGGxvCc/becb957fb3a84e6b04e71b30d6b1207e.jpg",
  "https://i.ibb.co/wFjKMtdk/cb175f75e4c0445346473cc7ee6d29ef.jpg",
  "https://i.ibb.co/XZTFnP1L/94a24b8c955da739585db131d0352520.jpg",
  "https://i.ibb.co/5hFkNqy2/5316aa51ae21a45ba2c182abddac3e43.jpg",
  "https://i.ibb.co/rf5QJnHN/06e6587fd9a6f02e1fbccd18bdeafe06.jpg",
  "https://i.ibb.co/ynHp0ngb/a691c04000b27c3c56fb8dad20f8a6de.jpg",
  "https://i.ibb.co/tgxV09n/026256eb44a597fa85da385282a88507.jpg",
  "https://i.ibb.co/MkG5jGqH/7707b13df5cd4f139d1773c22296450c.jpg",
  "https://i.ibb.co/JRtsnJCH/4d015a092a34df2b7ac2d041aa2d0c5d.jpg",
  "https://i.ibb.co/nNDpFq9c/1569fc12b5e96a2770b4597c9c747ee4.jpg",
  "https://i.ibb.co/sZsh7Vv/3bae81c9712003b45013c685fba01289.jpg",
  "https://i.ibb.co/Txjz9421/021f17bd2213d7a4879842a3b8488f14.jpg",
  "https://i.ibb.co/b543Lrzc/e4a280013b720105d3aa2bde4edef6c2.jpg",
  "https://i.ibb.co/dvzXpS4/4665c48cd70fc9e0a15ffd5d36630bb8.jpg",
  "https://i.ibb.co/dJW7LmQ8/c422383d6ac46b0cf2ce0b123c336fe4.jpg",
  "https://i.ibb.co/99C3JVCR/97f1cc38c0e9ab3f1eefa85ac3dc7e0b.jpg",
  "https://i.ibb.co/YBxXJZ24/724d8f72d428a6e43b8efbaeb9868f43.jpg",
  "https://i.ibb.co/9mnm48kC/4b07ba4546fd719f7f7477652b7bf18b.jpg"
];

function getSaved() { return JSON.parse(localStorage.getItem("kpop_binder_final")) || []; }
function saveColl(arr) { localStorage.setItem("kpop_binder_final", JSON.stringify(arr)); }

function loadBinder() {
    const div = document.getElementById("binder");
    const saved = getSaved();
    div.innerHTML = "";
    saved.forEach(url => {
        div.innerHTML += `<div class="binder-card"><img src="${url}" loading="lazy"></div>`;
    });
    document.getElementById("binderStats").innerText = `${saved.length} / ${binderCards.length} photocards`;
}

function drawCard() {
    const random = binderCards[Math.floor(Math.random() * binderCards.length)];
    const saved = getSaved();
    const repeated = saved.includes(random);
    document.getElementById("cardDisplay").innerHTML = `
        <img src="${random}">
        <div class="card-buttons">
            ${repeated ? `<button onclick="discardCard()">✖</button>` : `<button onclick="saveCard('${random}')">❤️</button><button onclick="discardCard()">✖</button>`}
        </div>
        ${repeated ? '<p style="color:#ff1493;">🌸 repetida! descarte se quiser 🌸</p>' : ''}
    `;
}
function saveCard(url) {
    let saved = getSaved();
    if (!saved.includes(url)) saved.push(url);
    saveColl(saved);
    loadBinder();
    discardCard();
}
function discardCard() { document.getElementById("cardDisplay").innerHTML = ""; }
function resetBinder() {
    if(confirm("Tem certeza? Todas as cartas serão apagadas.")) {
        localStorage.removeItem("kpop_binder_final");
        loadBinder();
        discardCard();
    }
}

// ==================== BIG HUG ====================
let hugInterval;
function createChan() {
    const img = document.createElement("img");
    img.src = "https://i.ibb.co/4ZCrvYQh/Picsart-26-05-06-22-32-08-703.png";
    img.classList.add("chan");
    img.style.left = Math.random() * window.innerWidth + "px";
    img.style.top = Math.random() * window.innerHeight + "px";
    document.body.appendChild(img);
}
function startBigHug() {
    if (hugInterval) clearInterval(hugInterval);
    hugInterval = setInterval(createChan, 250);
}

// ==================== BANDEIRA BI ====================
const biExtra = [
    "https://i.ibb.co/xSGVCqq5/f0e3ae2b2e2423dad6b32642a420f859.jpg",
    "https://i.ibb.co/fdhv750J/07bc841f02955b068681bb8e7c5fb04e.jpg",
    "https://i.ibb.co/xKX49vLS/175e6917b8113722d5dd6b95a949586d.jpg",
    "https://i.ibb.co/kVfQW8Rr/image.png",
    "https://i.ibb.co/4w1xxkyC/e6d75fbcc02c6eefd8d73c693bcbfbed.jpg",
    "https://i.ibb.co/RG7W160K/1fea8cac7455d647619df135499352c5.jpg",
    "https://i.ibb.co/S79sszW2/2347044a2a33a4e6d159b2a3ef9905d7.jpg",
    "https://i.ibb.co/ZRk0NKVC/96c75a278e9011b582b930437988701b.jpg",
    "https://i.ibb.co/qMG1pCmt/0419d5d95f8966702e68685fa2e07836.jpg"
];
function openBiOverlay() {
    const overlay = document.getElementById("biOverlay");
    const container = document.getElementById("biPhotos");
    container.innerHTML = "";
    biExtra.forEach(url => {
        const img = document.createElement("img");
        img.src = url;
        container.appendChild(img);
    });
    overlay.classList.add("active");
}
function closeBiOverlay() {
    document.getElementById("biOverlay").classList.remove("active");
}

// ==================== CHARTS ====================
const chartsData = [
    { rank:1, name:"Bang Chan", group:"Stray Kids", img:"https://i.ibb.co/Bb5zyCM/aa0d0adae895b028f5c03b338d9bb47c.jpg", last:1, peak:1, weeks:999, trend:"same", ch:"" },
    { rank:2, name:"Mark", group:"NCT", img:"https://i.ibb.co/SX97RpFg/06940cd301fb5e3aac9596af42d4bbfe.jpg", last:2, peak:2, weeks:87, trend:"same", ch:"" },
    { rank:3, name:"Changbin", group:"Stray Kids", img:"https://i.ibb.co/JWk1zCfk/08d44e68d8415f79ca13079b13d9605d.jpg", last:3, peak:2, weeks:66, trend:"same", ch:"" },
    { rank:4, name:"Han Jisung", group:"Stray Kids", img:"https://i.ibb.co/Qjq2kpXk/0b630450a8fc01a898059b78346035d7.jpg", last:5, peak:4, weeks:71, trend:"up", ch:"+1" },
    { rank:5, name:"Mingyu", group:"SEVENTEEN", img:"https://i.ibb.co/kVfQW8Rr/image.png", last:3, peak:1, weeks:55, trend:"down", ch:"-2" },
    { rank:6, name:"Eric", group:"THE BOYZ", img:"https://i.ibb.co/fdhv750J/07bc841f02955b068681bb8e7c5fb04e.jpg", last:22, peak:6, weeks:14, trend:"up", ch:"+16cm" },
    { rank:7, name:"Mingi", group:"ATEEZ", img:"https://i.ibb.co/RG7W160K/1fea8cac7455d647619df135499352c5.jpg", last:1, peak:1, weeks:39, trend:"down", ch:"-10" },
    { rank:8, name:"V", group:"BTS", img:"https://i.ibb.co/ZRk0NKVC/96c75a278e9011b582b930437988701b.jpg", last:8, peak:2, weeks:102, trend:"same", ch:"" }
];
const chartsGrid = document.getElementById("chartsGrid");
chartsData.forEach(c => {
    const card = document.createElement("div");
    card.className = "chart-card";
    card.innerHTML = `
        <div class="top-info">
            <img src="${c.img}">
            <div class="chart-text">
                <div class="rank-row">
                    <span class="rank-number">${c.rank}</span>
                    <span class="trend ${c.trend}">${c.trend === "up" ? "▲" : c.trend === "down" ? "▼" : "="} ${c.ch}</span>
                </div>
                <h2>${c.name}</h2>
                <p>${c.group}</p>
            </div>
        </div>
        <div class="stats">
            <div><span>LAST WEEK</span><strong>${c.last}</strong></div>
            <div><span>PEAK</span><strong>${c.peak}</strong></div>
            <div><span>WEEKS</span><strong>${c.weeks}</strong></div>
        </div>
    `;
    chartsGrid.appendChild(card);
});

// ==================== TIMELINE ====================
const timelineData = [
    { year: 1, text: "Governo do Jânio Quadros" },
    { year: 2, text: "namoro 'Jelena' (Justin Bieber + Selena Gomez)" },
    { year: 3, text: "relacionamento de Ian Somerhalder e Nina Dobrev" },
    { year: 4, text: "LOONA" },
    { year: 5, text: "sua faculdade" },
    { year: 6, text: "One Direction" },
    { year: 7, text: "Pretty Little Liars" },
    { year: 8, text: "Stray Kids (e contando ♡)" },
    { year: 9, text: "Depois das Onze" },
    { year: 10, text: "Friends" },
    { year: 11, text: "amizade Thabie" },
    { year: 12, text: "Ciclo do Zodíaco Chinês" },
    { year: 13, text: "Império Macedônico de Alexandre, o Grande" }
];
const timelineContainer = document.getElementById("timeline");
timelineData.forEach((item, idx) => {
    const side = idx % 2 === 0 ? "left" : "right";
    const div = document.createElement("div");
    div.className = `timeline-item ${side}`;
    div.innerHTML = `<div class="timeline-year">${item.year} ano</div><div class="timeline-text">${item.text}</div>`;
    timelineContainer.appendChild(div);
});
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add("show");
            observer.unobserve(entry.target);
        }
    });
}, { threshold: 0.2 });
document.querySelectorAll(".timeline-item").forEach(el => observer.observe(el));

// ==================== SCROLLS ====================
function scrollToNos() { document.getElementById("nosSection").scrollIntoView({ behavior:"smooth" }); }
function scrollToBinder() { document.getElementById("binderSection").scrollIntoView({ behavior:"smooth" }); }
function scrollToCharts() { document.getElementById("chartsSection").scrollIntoView({ behavior:"smooth" }); }
function scrollToTimeline() { document.getElementById("timelineSection").scrollIntoView({ behavior:"smooth" }); }
function scrollToPlaylist() { document.getElementById("playlistSection").scrollIntoView({ behavior:"smooth" }); }

loadBinder();
</script>
</body>
</html>
```
