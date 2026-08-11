<!DOCTYPE html>
<html lang="fr">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Omaima & Idriss | Wedding Invitation</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cormorant+Garamond:wght@300;400;500;600&family=Great+Vibes&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">


<style>

/* =====================================================
   GENERAL
===================================================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#f6eee5;
    color:#80603b;
    font-family:'Cormorant Garamond', serif;
    overflow-x:hidden;
}

a{
    -webkit-tap-highlight-color:transparent;
}


/* =====================================================
   INTRO SCREEN
===================================================== */

.intro{

    position:fixed;
    inset:0;

    z-index:9999;

    display:flex;
    align-items:center;
    justify-content:center;

    background:
        radial-gradient(
            circle at center,
            #fffaf5 0%,
            #f5e8da 55%,
            #e8d8c5 100%
        );

    transition:
        opacity 1.2s ease,
        visibility 1.2s ease;
}

.intro.hide{

    opacity:0;

    visibility:hidden;

    pointer-events:none;
}


/* =====================================================
   INVITATION CARD
===================================================== */

.envelope{

    width:min(88vw,420px);

    height:570px;

    position:relative;

    cursor:pointer;

    animation:
        envelopeAppear 1.2s ease both;
}

@keyframes envelopeAppear{

    from{
        opacity:0;
        transform:
            translateY(35px)
            scale(.96);
    }

    to{
        opacity:1;
        transform:
            translateY(0)
            scale(1);
    }
}


.paper{

    position:absolute;

    inset:0;

    overflow:hidden;

    background:
        linear-gradient(
            145deg,
            #fffaf5,
            #f5e8db
        );

    border:
        1px solid
        rgba(160,120,70,.25);

    box-shadow:

        0 30px 80px
        rgba(78,51,27,.20),

        inset 0 0 60px
        rgba(174,132,77,.08);
}


/* =====================================================
   FLORAL ORNAMENTS
===================================================== */

.flower{

    position:absolute;

    color:#b99664;

    opacity:.38;

    font-size:55px;

    line-height:1;
}

.flower::before{
    content:"❦";
}

.f1{

    top:20px;

    left:50%;

    transform:
        translateX(-50%)
        rotate(180deg);
}

.f2{

    left:20px;

    top:150px;

    transform:
        rotate(-35deg);
}

.f3{

    right:20px;

    top:150px;

    transform:
        rotate(35deg);
}

.f4{

    bottom:25px;

    left:50%;

    transform:
        translateX(-50%);
}


/* =====================================================
   DECORATIVE LINES
===================================================== */

.ornament{

    position:absolute;

    width:1px;

    height:130px;

    background:
        linear-gradient(
            transparent,
            #b79563,
            transparent
        );

    opacity:.4;
}

.o1{

    left:55px;

    top:175px;

    transform:rotate(22deg);
}

.o2{

    right:55px;

    top:175px;

    transform:rotate(-22deg);
}


/* =====================================================
   INVITATION TEXT
===================================================== */

.invitation{

    position:absolute;

    inset:0;

    padding:
        145px
        30px
        30px;

    text-align:center;
}

.small-title{

    font-family:'Playfair Display', serif;

    letter-spacing:4px;

    font-size:10px;

    color:#9d7848;

    margin-bottom:15px;
}

.names{

    font-family:'Great Vibes', cursive;

    font-size:53px;

    line-height:1;

    color:#966c37;
}

.and{

    font-family:'Playfair Display', serif;

    font-size:20px;

    margin:7px 0;

    color:#ad8651;
}

.intro-date{

    margin-top:24px;

    font-family:'Playfair Display', serif;

    font-size:12px;

    letter-spacing:2px;

    color:#80603b;
}

.intro-place{

    margin-top:9px;

    font-size:14px;

    letter-spacing:2px;

    color:#98764c;
}


/* =====================================================
   SEAL
===================================================== */

.seal{

    position:absolute;

    left:50%;
    top:50%;

    transform:
        translate(-50%,-50%);

    width:95px;
    height:95px;

    border-radius:50%;

    background:
        radial-gradient(
            circle,
            #fffaf4 0 53%,
            #e0ccb2 54% 61%,
            #fffaf4 62%
        );

    box-shadow:
        0 8px 30px
        rgba(101,70,34,.18);

    display:flex;

    align-items:center;

    justify-content:center;

    z-index:5;
}

.seal span{

    font-family:'Great Vibes', cursive;

    font-size:36px;

    color:#9d743c;
}


/* =====================================================
   OPEN MESSAGE
===================================================== */

.open-text{

    position:absolute;

    bottom:20px;

    left:0;
    right:0;

    text-align:center;

    font-size:11px;

    letter-spacing:3px;

    color:#9e8058;

    animation:pulse 2s infinite;
}

@keyframes pulse{

    0%,100%{
        opacity:1;
    }

    50%{
        opacity:.4;
    }
}


/* =====================================================
   WEBSITE
===================================================== */

.website{

    opacity:0;

    visibility:hidden;

    transition:
        opacity 1.3s ease;
}

.website.show{

    opacity:1;

    visibility:visible;
}


/* =====================================================
   NAVIGATION
===================================================== */

.nav{

    position:fixed;

    z-index:100;

    bottom:20px;

    left:50%;

    transform:
        translateX(-50%);

    width:min(92%,650px);

    display:flex;

    justify-content:space-around;

    align-items:center;

    padding:11px 12px;

    background:
        rgba(255,250,244,.90);

    backdrop-filter:blur(18px);

    -webkit-backdrop-filter:blur(18px);

    border:
        1px solid
        rgba(153,113,61,.20);

    border-radius:50px;

    box-shadow:
        0 12px 35px
        rgba(84,57,28,.13);
}

.nav a{

    color:#80603b;

    text-decoration:none;

    font-size:12px;

    letter-spacing:1px;

    padding:8px 12px;

    transition:.3s ease;
}

.nav a:hover{

    color:#ae8248;
}


/* =====================================================
   HERO
===================================================== */

.hero{

    min-height:100vh;

    position:relative;

    display:flex;

    align-items:center;

    justify-content:center;

    text-align:center;

    overflow:hidden;

    background:

        linear-gradient(
            rgba(247,238,227,.72),
            rgba(247,238,227,.92)
        ),

        url("https://images.unsplash.com/photo-1519225421980-715cb0215aed?auto=format&fit=crop&w=1800&q=90")

        center/cover;
}

.hero::before{

    content:"";

    position:absolute;

    inset:18px;

    border:
        1px solid
        rgba(151,111,60,.30);

    pointer-events:none;
}

.hero-content{

    position:relative;

    z-index:2;

    padding:30px;
}

.hero-small{

    letter-spacing:5px;

    font-size:11px;

    text-transform:uppercase;

    color:#856440;
}

.hero-names{

    font-family:'Great Vibes', cursive;

    font-size:
        clamp(
            70px,
            15vw,
            125px
        );

    line-height:.9;

    color:#956b35;

    margin:25px 0;
}

.hero-date{

    font-family:'Playfair Display', serif;

    font-size:17px;

    letter-spacing:4px;

    color:#795a38;
}

.hero-place{

    margin-top:13px;

    font-size:17px;

    letter-spacing:3px;
}


/* =====================================================
   DIVIDER
===================================================== */

.divider{

    width:90px;

    height:1px;

    background:#b69461;

    margin:28px auto;

    position:relative;
}

.divider::after{

    content:"✦";

    position:absolute;

    left:50%;
    top:50%;

    transform:
        translate(-50%,-50%);

    background:#f7eee5;

    padding:0 10px;

    font-size:13px;

    color:#9d7847;
}


/* =====================================================
   SECTIONS
===================================================== */

section{

    padding:
        100px
        20px;

    position:relative;
}

.section-title{

    text-align:center;

    font-family:'Great Vibes', cursive;

    font-size:58px;

    color:#956d39;
}

.section-subtitle{

    text-align:center;

    margin-top:8px;

    font-size:12px;

    letter-spacing:3px;

    text-transform:uppercase;
}


/* =====================================================
   STORY
===================================================== */

.story{

    max-width:850px;

    margin:auto;

    text-align:center;

    font-size:20px;

    line-height:1.8;

    color:#70583b;
}

.arabic{

    direction:rtl;

    font-family:'Amiri', serif;

    font-size:31px;

    line-height:1.8;

    margin:
        30px
        0
        22px;

    color:#8b6638;
}


/* =====================================================
   DETAILS
===================================================== */

.details{

    background:
        linear-gradient(
            135deg,
            #eee0cf,
            #f5e9dd
        );
}

.cards{

    max-width:1000px;

    margin:
        55px
        auto
        0;

    display:grid;

    grid-template-columns:
        repeat(3,1fr);

    gap:25px;
}

.card{

    background:
        rgba(255,250,244,.75);

    border:
        1px solid
        rgba(157,116,61,.20);

    padding:
        40px
        20px;

    text-align:center;

    box-shadow:
        0 15px 40px
        rgba(103,74,39,.08);

    transition:.4s ease;
}

.card:hover{

    transform:
        translateY(-5px);

    box-shadow:
        0 20px 45px
        rgba(103,74,39,.13);
}

.card-icon{

    font-size:30px;

    color:#a27b44;

    margin-bottom:15px;
}

.card h3{

    font-family:'Playfair Display', serif;

    font-weight:500;

    letter-spacing:2px;

    font-size:16px;

    color:#7e5c36;
}

.card p{

    margin-top:12px;

    font-size:17px;

    line-height:1.6;

    color:#735a3d;
}


/* =====================================================
   MAP BUTTON
===================================================== */

.map-button{

    display:inline-block;

    margin-top:20px;

    padding:
        12px
        22px;

    border:
        1px solid
        #a17b45;

    color:#8b6739;

    text-decoration:none;

    font-size:10px;

    letter-spacing:2px;

    transition:.35s ease;
}

.map-button:hover{

    background:#9b7542;

    color:white;

    transform:
        translateY(-2px);
}


/* =====================================================
   COUNTDOWN
===================================================== */

.countdown{

    display:flex;

    justify-content:center;

    gap:35px;

    margin-top:55px;

    flex-wrap:wrap;
}

.time-box{

    min-width:100px;

    text-align:center;
}

.time-number{

    font-family:'Playfair Display', serif;

    font-size:44px;

    color:#956d38;
}

.time-label{

    font-size:10px;

    letter-spacing:3px;

    text-transform:uppercase;

    margin-top:5px;
}


/* =====================================================
   FOOTER
===================================================== */

footer{

    padding:
        80px
        20px
        130px;

    text-align:center;

    background:#eadbc9;
}

.footer-names{

    font-family:'Great Vibes', cursive;

    font-size:55px;

    color:#956d38;
}

footer p{

    margin-top:15px;

    letter-spacing:2px;

    font-size:12px;

    color:#80603d;
}


/* =====================================================
   MOBILE
===================================================== */

@media(max-width:700px){

    .envelope{

        width:88vw;

        height:560px;
    }

    .invitation{

        padding-top:145px;
    }

    .names{

        font-size:47px;
    }

    .cards{

        grid-template-columns:1fr;

        max-width:450px;
    }

    .hero-names{

        font-size:75px;
    }

    .hero-date{

        font-size:14px;

        letter-spacing:2px;
    }

    .hero-place{

        font-size:14px;

        letter-spacing:2px;
    }

    .nav{

        width:94%;

        padding:
            8px 5px;
    }

    .nav a{

        font-size:9px;

        padding:
            7px 5px;
    }

    section{

        padding:
            80px 18px;
    }

    .section-title{

        font-size:52px;
    }

    .arabic{

        font-size:27px;
    }

    .countdown{

        gap:20px;
    }

    .time-box{

        min-width:75px;
    }

    .time-number{

        font-size:36px;
    }

}


/* =====================================================
   SMALL PHONES
===================================================== */

@media(max-width:380px){

    .envelope{

        height:530px;
    }

    .names{

        font-size:43px;
    }

    .intro-date{

        font-size:10px;
    }

    .intro-place{

        font-size:12px;
    }

    .seal{

        width:85px;
        height:85px;
    }

    .hero-names{

        font-size:65px;
    }

    .nav a{

        font-size:8px;
    }

}

</style>

</head>


<body>


<!-- =====================================================
     OPENING INVITATION
===================================================== -->

<div
    class="intro"
    id="intro"
>

    <div
        class="envelope"
        onclick="openInvitation()"
    >

        <div class="paper">


            <!-- FLOWERS -->

            <div class="flower f1"></div>

            <div class="flower f2"></div>

            <div class="flower f3"></div>

            <div class="flower f4"></div>


            <!-- ORNAMENTS -->

            <div class="ornament o1"></div>

            <div class="ornament o2"></div>


            <!-- TEXT -->

            <div class="invitation">

                <div class="small-title">
                    NOTRE MARIAGE
                </div>


                <div class="names">
                    Omaima
                </div>


                <div class="and">
                    &
                </div>


                <div class="names">
                    Idriss
                </div>


                <div class="intro-date">
                    SAMEDI · 10 OCTOBRE 2026
                </div>


                <div class="intro-place">
                    DAR MEKHTARA · 18:00
                </div>

            </div>


            <!-- SEAL -->

            <div class="seal">

                <span>
                    O & I
                </span>

            </div>


            <!-- OPEN -->

            <div class="open-text">
                TOUCHEZ POUR OUVRIR
            </div>

        </div>

    </div>

</div>



<!-- =====================================================
     MAIN WEBSITE
===================================================== -->

<div
    class="website"
    id="website"
>


    <!-- =================================================
         NAVIGATION
    ================================================== -->

    <nav class="nav">

        <a href="#accueil">
            Accueil
        </a>

        <a href="#histoire">
            Notre histoire
        </a>

        <a href="#details">
            Détails
        </a>


        <!-- DIRECT GOOGLE MAPS -->

        <a
            href="https://maps.app.goo.gl/gNJ5ED1HyvU8enjd7?g_st=ic"
            target="_blank"
            rel="noopener noreferrer"
        >
            Le lieu
        </a>

    </nav>



    <!-- =================================================
         HERO
    ================================================== -->

    <section
        class="hero"
        id="accueil"
    >

        <div class="hero-content">


            <div class="hero-small">
                AVEC L'AMOUR DE NOS FAMILLES
            </div>


            <div class="hero-names">

                Omaima

                <br>


                <span
                    style="
                    font-family:'Playfair Display';
                    font-size:.35em;
                    "
                >
                    &
                </span>


                <br>

                Idriss

            </div>


            <div class="divider"></div>


            <div class="hero-date">
                SAMEDI · 10 OCTOBRE 2026
            </div>


            <div class="hero-place">
                DAR MEKHTARA · 18:00
            </div>

        </div>

    </section>



    <!-- =================================================
         STORY
    ================================================== -->

    <section
        id="histoire"
    >

        <h2 class="section-title">
            Une nouvelle histoire
        </h2>


        <div class="divider"></div>


        <div class="story">


            <p class="arabic">
                وَجَعَلَ اللهُ بَيْنَكُمَا مَوَدَّةً وَرَحْمَةً
            </p>


            <p>
                Avec beaucoup de bonheur et d'émotion,
                nous avons le plaisir de vous inviter
                à célébrer avec nous le début de notre
                nouvelle vie à deux.
            </p>


            <br>


            <p>
                Votre présence rendra cette journée
                encore plus belle et restera pour nous
                un souvenir précieux.
            </p>


        </div>

    </section>



    <!-- =================================================
         DETAILS
    ================================================== -->

    <section
        class="details"
        id="details"
    >

        <h2 class="section-title">
            Le grand jour
        </h2>


        <div class="section-subtitle">
            Nous avons hâte de vous retrouver
        </div>


        <div class="cards">


            <!-- DATE -->

            <div class="card">

                <div class="card-icon">
                    ♡
                </div>

                <h3>
                    DATE
                </h3>

                <p>
                    Samedi<br>
                    10 Octobre 2026
                </p>

            </div>



            <!-- TIME -->

            <div class="card">

                <div class="card-icon">
                    ◷
                </div>

                <h3>
                    HEURE
                </h3>

                <p>
                    À partir de<br>
                    18:00
                </p>

            </div>



            <!-- PLACE -->

            <div class="card">

                <div class="card-icon">
                    ⌖
                </div>

                <h3>
                    LE LIEU
                </h3>

                <p>

                    Dar Mekhtara<br>

                    Meknès

                </p>


                <!-- GOOGLE MAPS BUTTON -->

                <a
                    class="map-button"

                    href="https://maps.app.goo.gl/gNJ5ED1HyvU8enjd7?g_st=ic"

                    target="_blank"

                    rel="noopener noreferrer"
                >
                    VOIR L’ITINÉRAIRE
                </a>

            </div>


        </div>

    </section>



    <!-- =================================================
         COUNTDOWN
    ================================================== -->

    <section>

        <h2 class="section-title">
            Le compte à rebours
        </h2>


        <div class="divider"></div>


        <div class="countdown">


            <!-- DAYS -->

            <div class="time-box">

                <div
                    class="time-number"
                    id="days"
                >
                    00
                </div>

                <div class="time-label">
                    Jours
                </div>

            </div>



            <!-- HOURS -->

            <div class="time-box">

                <div
                    class="time-number"
                    id="hours"
                >
                    00
                </div>

                <div class="time-label">
                    Heures
                </div>

            </div>



            <!-- MINUTES -->

            <div class="time-box">

                <div
                    class="time-number"
                    id="minutes"
                >
                    00
                </div>

                <div class="time-label">
                    Minutes
                </div>

            </div>



            <!-- SECONDS -->

            <div class="time-box">

                <div
                    class="time-number"
                    id="seconds"
                >
                    00
                </div>

                <div class="time-label">
                    Secondes
                </div>

            </div>


        </div>

    </section>



    <!-- =================================================
         FOOTER
    ================================================== -->

    <footer>

        <div class="footer-names">
            Omaima & Idriss
        </div>


        <p>
            10 · 10 · 2026
        </p>


        <p>
            Avec tout notre amour ♡
        </p>

    </footer>


</div>



<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>


/* =====================================================
   OPEN INVITATION
===================================================== */

function openInvitation(){

    const intro =
        document.getElementById("intro");

    const website =
        document.getElementById("website");


    intro.classList.add("hide");


    setTimeout(function(){

        website.classList.add("show");

        document.body.style.overflowY =
            "auto";

    },700);

}



/* =====================================================
   COUNTDOWN
===================================================== */

const weddingDate =
    new Date(
        "October 10, 2026 18:00:00"
    ).getTime();



function updateCountdown(){

    const now =
        new Date().getTime();


    const difference =
        weddingDate - now;


    if(difference <= 0){

        document.getElementById("days").innerHTML =
            "00";

        document.getElementById("hours").innerHTML =
            "00";

        document.getElementById("minutes").innerHTML =
            "00";

        document.getElementById("seconds").innerHTML =
            "00";

        return;
    }


    const days =
        Math.floor(
            difference /
            (1000 * 60 * 60 * 24)
        );


    const hours =
        Math.floor(
            (
                difference %
                (1000 * 60 * 60 * 24)
            )
            /
            (1000 * 60 * 60)
        );


    const minutes =
        Math.floor(
            (
                difference %
                (1000 * 60 * 60)
            )
            /
            (1000 * 60)
        );


    const seconds =
        Math.floor(
            (
                difference %
                (1000 * 60)
            )
            /
            1000
        );


    document.getElementById("days").innerHTML =
        String(days).padStart(2,"0");


    document.getElementById("hours").innerHTML =
        String(hours).padStart(2,"0");


    document.getElementById("minutes").innerHTML =
        String(minutes).padStart(2,"0");


    document.getElementById("seconds").innerHTML =
        String(seconds).padStart(2,"0");

}



updateCountdown();


setInterval(
    updateCountdown,
    1000
);



/* =====================================================
   LOCK SCROLL BEFORE OPENING
===================================================== */

document.body.style.overflow =
    "hidden";


</script>


</body>

</html>WEDDING O&I