<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>PecesGuía | Guía de peces y acuarios</title>

    <meta name="description" content="Guía de peces de acuario con información sobre litros, temperatura, pH, alimentación y compatibilidad.">

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f2f8fa;
            color: #17324d;
        }

        header {
            background: #073b5c;
            color: white;
            padding: 20px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: bold;
        }

        .hero {
            background: linear-gradient(135deg, #087ea4, #073b5c);
            color: white;
            text-align: center;
            padding: 80px 20px;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }

        .search {
            max-width: 650px;
            margin: auto;
        }

        .search input {
            width: 100%;
            padding: 17px;
            border: none;
            border-radius: 10px;
            font-size: 17px;
        }

        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 32px;
        }

        .filters {
            background: white;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
        }

        .filter-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .filters label {
            font-weight: bold;
            display: block;
            margin-bottom: 7px;
        }

        .filters input,
        .filters select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccd9df;
            border-radius: 8px;
        }

        .fish-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .fish-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: 0.2s;
        }

        .fish-card:hover {
            transform: translateY(-5px);
        }

        .fish-image {
            height: 180px;
            background: linear-gradient(135deg, #56c6e9, #087ea4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 70px;
        }

        .fish-info {
            padding: 20px;
        }

        .fish-info h3 {
            font-size: 22px;
            margin-bottom: 5px;
        }

        .scientific {
            color: #71808a;
            font-style: italic;
            margin-bottom: 15px;
        }

        .details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 8px;
            font-size: 14px;
        }

        .detail {
            background: #eef7fa;
            padding: 9px;
            border-radius: 7px;
        }

        .guides {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .guide {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.07);
        }

        .guide h3 {
            margin-bottom: 10px;
        }

        .ad {
            margin: 40px 0;
            min-height: 100px;
            background: #e7eef1;
            border: 2px dashed #b7c5ca;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #71808a;
        }

        footer {
            background: #073b5c;
            color: white;
            text-align: center;
            padding: 30px;
            margin-top: 50px;
        }

        @media (max-width: 800px) {

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav a {
                margin: 0 7px;
                font-size: 14px;
            }

            .hero h1 {
                font-size: 36px;
            }

            .filter-grid,
            .fish-grid,
            .guides {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>

<header>

    <div class="logo">
        🐟 PecesGuía
    </div>

    <nav>
        <a href="#inicio">Inicio</a>
        <a href="#peces">Peces</a>
        <a href="#guias">Guías</a>
    </nav>

</header>


<section class="hero" id="inicio">

    <h1>🐠 PecesGuía</h1>

    <p>
        Todo lo que necesitas saber para cuidar tus peces y tu acuario.
    </p>

    <div class="search">

        <input
            type="text"
            id="searchInput"
            placeholder="🔎 Busca un pez... Ej: Betta"
        >

    </div>

</section>


<div class="container">

    <div class="ad">
        Espacio para publicidad
    </div>


    <section id="peces">

        <h2 class="section-title">
            🔎 Busca tu pez
        </h2>

        <div class="filters">

            <div class="filter-grid">

                <div>
                    <label>Litros máximos</label>

                    <input
                        type="number"
                        id="litros"
                        placeholder="Ej: 60"
                    >
                </div>

                <div>
                    <label>pH</label>

                    <select id="ph">

                        <option value="">Cualquier pH</option>
                        <option value="6">6 - 6.9</option>
                        <option value="7">7 - 7.9</option>
                        <option value="8">8 - 8.9</option>

                    </select>

                </div>

                <div>
                    <label>Temperatura máxima</label>

                    <input
                        type="number"
                        id="temperatura"
                        placeholder="Ej: 28"
                    >
                </div>

            </div>

        </div>


        <div class="fish-grid" id="fishGrid">


            <!-- BETTA -->

            <article
                class="fish-card"
                data-name="betta"
                data-litros="20"
                data-ph="7"
                data-temp="28"
            >

                <div class="fish-image">
                    🐟
                </div>

                <div class="fish-info">

                    <h3>Betta</h3>

                    <div class="scientific">
                        Betta splendens
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 20 L+
                        </div>

                        <div class="detail">
                            🌡️ 24-28 °C
                        </div>

                        <div class="detail">
                            🧪 pH 6.5-7.5
                        </div>

                        <div class="detail">
                            ⭐ Fácil
                        </div>

                    </div>

                </div>

            </article>


            <!-- NEON -->

            <article
                class="fish-card"
                data-name="neon tetra"
                data-litros="60"
                data-ph="7"
                data-temp="26"
            >

                <div class="fish-image">
                    🐠
                </div>

                <div class="fish-info">

                    <h3>Neón tetra</h3>

                    <div class="scientific">
                        Paracheirodon innesi
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 60 L+
                        </div>

                        <div class="detail">
                            🌡️ 20-26 °C
                        </div>

                        <div class="detail">
                            🧪 pH 6-7.5
                        </div>

                        <div class="detail">
                            ⭐ Fácil
                        </div>

                    </div>

                </div>

            </article>


            <!-- GUPPY -->

            <article
                class="fish-card"
                data-name="guppy"
                data-litros="50"
                data-ph="7"
                data-temp="28"
            >

                <div class="fish-image">
                    🐟
                </div>

                <div class="fish-info">

                    <h3>Guppy</h3>

                    <div class="scientific">
                        Poecilia reticulata
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 50 L+
                        </div>

                        <div class="detail">
                            🌡️ 22-28 °C
                        </div>

                        <div class="detail">
                            🧪 pH 6.8-8
                        </div>

                        <div class="detail">
                            ⭐ Fácil
                        </div>

                    </div>

                </div>

            </article>


            <!-- CORYDORAS -->

            <article
                class="fish-card"
                data-name="corydoras"
                data-litros="60"
                data-ph="7"
                data-temp="26"
            >

                <div class="fish-image">
                    🐟
                </div>

                <div class="fish-info">

                    <h3>Corydoras</h3>

                    <div class="scientific">
                        Corydoras paleatus
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 60 L+
                        </div>

                        <div class="detail">
                            🌡️ 18-26 °C
                        </div>

                        <div class="detail">
                            🧪 pH 6-7.5
                        </div>

                        <div class="detail">
                            ⭐ Fácil
                        </div>

                    </div>

                </div>

            </article>


            <!-- ESCALAR -->

            <article
                class="fish-card"
                data-name="escalar pez angel"
                data-litros="200"
                data-ph="7"
                data-temp="28"
            >

                <div class="fish-image">
                    🐠
                </div>

                <div class="fish-info">

                    <h3>Escalar</h3>

                    <div class="scientific">
                        Pterophyllum scalare
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 200 L+
                        </div>

                        <div class="detail">
                            🌡️ 24-28 °C
                        </div>

                        <div class="detail">
                            🧪 pH 6-7.5
                        </div>

                        <div class="detail">
                            ⭐ Media
                        </div>

                    </div>

                </div>

            </article>


            <!-- MOLLY -->

            <article
                class="fish-card"
                data-name="molly"
                data-litros="60"
                data-ph="8"
                data-temp="28"
            >

                <div class="fish-image">
                    🐟
                </div>

                <div class="fish-info">

                    <h3>Molly</h3>

                    <div class="scientific">
                        Poecilia sphenops
                    </div>

                    <div class="details">

                        <div class="detail">
                            💧 60 L+
                        </div>

                        <div class="detail">
                            🌡️ 24-28 °C
                        </div>

                        <div class="detail">
                            🧪 pH 7-8.5
                        </div>

                        <div class="detail">
                            ⭐ Fácil
                        </div>

                    </div>

                </div>

            </article>


        </div>

    </section>


    <div class="ad">
        Espacio para publicidad
    </div>


    <section id="guias">

        <h2 class="section-title">
            📚 Guías de acuario
        </h2>

        <div class="guides">

            <article class="guide">

                <h3>💧 Cómo ciclar un acuario</h3>

                <p>
                    Aprende qué es el ciclado y por qué es importante
                    antes de introducir peces.
                </p>

            </article>


            <article class="guide">

                <h3>🐟 Peces para principiantes</h3>

                <p>
                    Descubre algunas especies adecuadas para comenzar
                    en la acuariofilia.
                </p>

            </article>


            <article class="guide">

                <h3>🧪 Cómo controlar el agua</h3>

                <p>
                    Aprende a controlar parámetros como el pH,
                    amoníaco, nitritos y nitratos.
                </p>

            </article>

        </div>

    </section>


    <div class="ad">
        Espacio para publicidad
    </div>


    <section>

        <h2 class="section-title">
            🛒 Productos recomendados
        </h2>

        <div class="guide">

            <h3>Productos para tu acuario</h3>

            <p>
                Aquí podremos colocar enlaces de afiliados a filtros,
                calentadores, comida, iluminación y otros productos.
            </p>

        </div>

    </section>

</div>


<footer>

    <p>🐟 PecesGuía © 2026</p>

    <p>
        Información sobre peces y acuariofilia.
    </p>

</footer>


<script>

    const searchInput = document.getElementById("searchInput");
    const litrosInput = document.getElementById("litros");
    const phInput = document.getElementById("ph");
    const temperaturaInput = document.getElementById("temperatura");

    const cards = document.querySelectorAll(".fish-card");


    function filterFish() {

        const search = searchInput.value.toLowerCase();
        const litros = Number(litrosInput.value);
        const ph = Number(phInput.value);
        const temperatura = Number(temperaturaInput.value);


        cards.forEach(card => {

            const name = card.dataset.name;
            const fishLitros = Number(card.dataset.litros);
            const fishPh = Number(card.dataset.ph);
            const fishTemp = Number(card.dataset.temp);


            const matchesSearch =
                name.includes(search);

            const matchesLitros =
                !litros || fishLitros <= litros;

            const matchesPh =
                !ph || fishPh === ph;

            const matchesTemp =
                !temperatura || fishTemp <= temperatura;


            if (
                matchesSearch &&
                matchesLitros &&
                matchesPh &&
                matchesTemp
            ) {

                card.style.display = "block";

            } else {

                card.style.display = "none";

            }

        });

    }


    searchInput.addEventListener("input", filterFish);

    litrosInput.addEventListener("input", filterFish);

    phInput.addEventListener("change", filterFish);

    temperaturaInput.addEventListener("input", filterFish);

</script>

</body>
</html>
