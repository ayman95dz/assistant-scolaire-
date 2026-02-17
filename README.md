
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Assistant Scolaire Ultimate+</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    transition: 0.4s;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}

/* MENU */
.menu-btn {
    position: fixed;
    top: 15px;
    left: 15px;
    font-size: 30px;
    cursor: pointer;
    z-index: 1001;
}

.overlay {
    position: fixed;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.4);
    display: none;
    z-index: 1000;
}

.overlay.active { display: block; }

.sidebar {
    position: fixed;
    top: 0;
    left: -280px;
    width: 260px;
    height: 100%;
    background: rgba(0,0,0,0.9);
    color: white;
    padding: 20px;
    transition: 0.4s;
    z-index: 1002;
    overflow-y: auto;
}

.sidebar.active { left: 0; }

.sidebar select, .sidebar button {
    width: 100%;
    padding: 8px;
    margin-bottom: 10px;
}

.container {
    padding: 80px 20px 20px 20px;
    background: rgba(0,0,0,0.5);
    min-height: 100vh;
    color: white;
}

input, select, button {
    padding: 10px;
    margin: 5px;
}

li {
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
    background: rgba(255,255,255,0.2);
}

/* THEMES CLASSIQUES (25 déjà existants simplifiés ici) */
.clair { background:#f4f4f4; color:black;}
.sombre { background:#121212; color:white;}
.neon { background:black; color:#00ffcc;}
.galactique { background:radial-gradient(circle,#000428,#004e92); color:white;}
.sunset { background:linear-gradient(to right,#ff512f,#dd2476); color:white;}
.ocean { background:linear-gradient(to right,#2E3192,#1BFFFF);}
.foret { background:linear-gradient(to right,#134E5E,#71B280);}
.feu { background:linear-gradient(to right,#ff0000,#ff9900);}
.violet { background:linear-gradient(to right,#41295a,#2F0743);}
.pastel { background:#ffe0f0; color:#333;}

/* THEMES IMAGES ANIMAUX */
.lion { background-image:url('https://images.unsplash.com/photo-1546182990-dffeafbe841d'); }
.loup { background-image:url('https://images.unsplash.com/photo-1508672019048-805c876b67e2'); }
.tigre { background-image:url('https://images.unsplash.com/photo-1549366021-9f761d040a94'); }
.aigle { background-image:url('https://images.unsplash.com/photo-1501706362039-c6e80948a97a'); }
.cheval { background-image:url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee'); }

/* THEMES IMAGES NATURE */
.foretNature { background-image:url('https://images.unsplash.com/photo-1501785888041-af3ef285b470'); }
.montagne { background-image:url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b'); }
.plage { background-image:url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e'); }
.cascade { background-image:url('https://images.unsplash.com/photo-1501785888041-af3ef285b470'); }
.ciel { background-image:url('https://images.unsplash.com/photo-1444703686981-a3abbc4d4fe3'); }

</style>
</head>

<body class="clair">

<div class="menu-btn" onclick="toggleMenu()">☰</div>
<div class="overlay" id="overlay" onclick="toggleMenu()"></div>

<div class="sidebar" id="sidebar">
    <h3>🎨 Thèmes</h3>
    <select onchange="changerTheme(this.value)">
        <option value="clair">Clair</option>
        <option value="sombre">Sombre</option>
        <option value="neon">Néon</option>
        <option value="galactique">Galactique</option>
        <option value="sunset">Sunset</option>
        <option value="ocean">Océan</option>
        <option value="foret">Forêt</option>
        <option value="feu">Feu</option>
        <option value="violet">Violet</option>
        <option value="pastel">Pastel</option>

        <option disabled>──────────</option>
        <option value="lion">🦁 Lion</option>
        <option value="loup">🐺 Loup</option>
        <option value="tigre">🐯 Tigre</option>
        <option value="aigle">🦅 Aigle</option>
        <option value="cheval">🐎 Cheval</option>

        <option disabled>──────────</option>
        <option value="foretNature">🌲 Forêt Nature</option>
        <option value="montagne">🏔️ Montagne</option>
        <option value="plage">🏖️ Plage</option>
        <option value="cascade">💧 Cascade</option>
        <option value="ciel">🌌 Ciel étoilé</option>
    </select>
</div>

<div class="container">
    <h1>📚 Mon Assistant Scolaire</h1>
    <p>Organise tes devoirs et tes rappels facilement.</p>

    <input type="text" placeholder="Nom du devoir">
    <input type="date">
    <button>Ajouter</button>

    <ul>
        <li>Exemple : Contrôle de math - 20/06</li>
    </ul>
</div>

<script>
function toggleMenu() {
    document.getElementById("sidebar").classList.toggle("active");
    document.getElementById("overlay").classList.toggle("active");
}

function changerTheme(theme) {
    document.body.className = theme;
}
</script>

</body>
</html>
