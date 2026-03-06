<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>POKI GLOBAL | BRENNO CEO</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700;800;900&display=swap" rel="stylesheet">
    <style>
        :root { --p-purple: #6a42f4; --p-dark: #4c2fb3; --p-yellow: #ffde00; --p-bg: #5b39d1; --p-cyan: #00f2ff; --card-radius: 20px; --shadow: 0 8px 0 rgba(0,0,0,0.2); }
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Montserrat', sans-serif; }
        body { background: var(--p-dark); padding-top: 160px; color: white; overflow-x: hidden; }
        header { position: fixed; top: 0; width: 100%; height: 95px; background: var(--p-purple); z-index: 10000; display: flex; align-items: center; justify-content: space-between; padding: 0 40px; border-bottom: 6px solid rgba(0,0,0,0.1); }
        .logo { font-size: 55px; font-weight: 900; color: var(--p-yellow); letter-spacing: -5px; text-transform: lowercase; }
        .search-input { width: 100%; max-width: 600px; height: 55px; border-radius: 30px; border: none; padding-left: 30px; font-size: 18px; font-weight: 800; }
        .xp-engine { position: fixed; top: 95px; width: 100%; height: 6px; background: rgba(0,0,0,0.3); z-index: 9999; }
        #xp-bar { width: 30%; height: 100%; background: var(--p-cyan); box-shadow: 0 0 15px var(--p-cyan); }
        .content-engine { display: flex; max-width: 1800px; margin: 0 auto; padding: 20px; gap: 20px; }
        .poki-grid { flex: 1; display: grid; grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); grid-auto-rows: 150px; gap: 15px; }
        .game-card { background: white; border-radius: var(--card-radius); cursor: pointer; position: relative; overflow: hidden; box-shadow: var(--shadow); transition: 0.3s; }
        .game-card:hover { transform: scale(1.05); }
        .game-card img { width: 100%; height: 100%; object-fit: cover; }
        .game-card .info { position: absolute; bottom: 0; width: 100%; height: 30px; background: white; color: #333; display: flex; align-items: center; justify-content: center; font-size: 10px; font-weight: 900; }
        #poki-theatre { position: fixed; inset: 0; background: #000; z-index: 200000; display: none; flex-direction: column; }
        .nav-theatre { height: 70px; background: var(--p-purple); display: flex; align-items: center; justify-content: space-between; padding: 0 30px; }
        .back-button { background: var(--p-yellow); border: none; padding: 10px 30px; border-radius: 15px; font-weight: 900; cursor: pointer; }
        iframe { flex: 1; border: none; background: white; }
    </style>
</head>
<body>
<header><div class="logo">poki</div><input type="text" class="search-input" placeholder="Buscar jogos..."><div style="background:white; color:#333; padding:10px 20px; border-radius:30px; font-weight:900;">⭐ LVL 1</div></header>
<div class="xp-engine"><div id="xp-bar"></div></div>
<div class="content-engine"><div class="poki-grid" id="grid"></div></div>
<div id="poki-theatre"><div class="nav-theatre"><h2>JOGANDO AGORA</h2><button class="back-button" onclick="closeGame()">VOLTAR</button></div><iframe id="game-frame"></iframe></div>
<script>
    const games = [
        {n:"2048", u:"https://play2048.co/", i:"https://play2048.co/meta/apple-touch-icon.png"},
        {n:"Snake", u:"https://n-p-n.github.io/snake/", i:"https://n-p-n.github.io/snake/apple-touch-icon.png"},
        {n:"Hextris", u:"https://hextris.io/", i:"https://hextris.io/images/touch-icon-114x114.png"},
        {n:"Flappy", u:"https://wayou.github.io/FlappyBird/", i:"https://wayou.github.io/FlappyBird/style/img/apple-touch-icon.png"}
    ];
    const grid = document.getElementById('grid');
    for(let i=0; i<100; i++) {
        const g = games[i % games.length];
        const card = document.createElement('div');
        card.className = 'game-card';
        card.innerHTML = `<img src="${g.i}"><div class="info">${g.n}</div>`;
        card.onclick = () => { document.getElementById('poki-theatre').style.display='flex'; document.getElementById('game-frame').src=g.u; };
        grid.appendChild(card);
    }
    function closeGame() { document.getElementById('poki-theatre').style.display='none'; document.getElementById('game-frame').src=''; }
</script>
</body>
</html>
