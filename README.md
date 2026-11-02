<!DOCTYPE html>
<html lang="fr">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WebBoost France | Création de Sites Web</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Segoe UI', sans-serif;
    scroll-behavior:smooth;
}

body{
    background:#081220;
    color:white;
    overflow-x:hidden;
}

/* Fond animé */

.background-animation{
    position:fixed;
    inset:0;
    z-index:-1;
    background:
    radial-gradient(circle at 15% 25%, rgba(0,120,212,.35), transparent 30%),
    radial-gradient(circle at 80% 75%, rgba(0,183,255,.25), transparent 30%);
    animation:bgMove 10s infinite alternate ease-in-out;
}

@keyframes bgMove{
    from{
        transform:scale(1);
    }

    to{
        transform:scale(1.2);
    }
}

/* Header */

header{
    position:fixed;
    top:0;
    width:100%;
    padding:20px 10%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
    transition:.4s;
}

header.scrolled{
    background:rgba(255,255,255,.08);
    backdrop-filter:blur(15px);
    box-shadow:0 5px 25px rgba(0,0,0,.3);
}

.logo{
    font-size:28px;
    font-weight:700;
    color:#00b7ff;
}

nav a{
    text-decoration:none;
    color:white;
    margin-left:25px;
    transition:.3s;
}

nav a:hover{
    color:#00b7ff;
}

/* Hero */

.hero{
    min-height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:20px;
}

.hero h1{
    font-size:4rem;
    max-width:900px;
    opacity:0;
    transform:translateY(40px);
    animation:fadeUp 1s forwards;
}

.hero p{
    margin-top:20px;
    font-size:1.2rem;
    color:#d2d2d2;
    max-width:700px;
    opacity:0;
    transform:translateY(40px);
    animation:fadeUp 1s .3s forwards;
}

@keyframes fadeUp{
    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* Bouton */

.btn{
    margin-top:35px;
    display:inline-block;
    padding:16px 34px;
    background:#00b7ff;
    color:white;
    text-decoration:none;
    border-radius:50px;
    font-weight:600;
    position:relative;
    overflow:hidden;
    transition:.3s;
    opacity:0;
    transform:translateY(40px);
    animation:fadeUp 1s .6s forwards;
}

.btn:hover{
    transform:scale(1.05);
}

.btn::before{
    content:"";
    position:absolute;
    top:0;
    left:-100%;
    width:100%;
    height:100%;
    background:linear-gradient(
    90deg,
    transparent,
    rgba(255,255,255,.5),
    transparent
    );
}

.btn:hover::before{
    left:100%;
    transition:.8s;
}

/* Sections */

.section{
    padding:100px 10%;
    opacity:0;
    transform:translateY(70px);
    transition:1s;
}

.section.show{
    opacity:1;
    transform:translateY(0);
}

.section-title{
    text-align:center;
    font-size:2.5rem;
    margin-bottom:20px;
}

.section-subtitle{
    text-align:center;
    color:#c6c6c6;
    margin-bottom:50px;
}

/* Services */

.services{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:30px;
}

.card{

    background:rgba(255,255,255,.06);
    border:1px solid rgba(255,255,255,.1);
    backdrop-filter:blur(15px);

    padding:35px;
    border-radius:20px;

    transition:.4s;
}

.card:hover{
    transform:translateY(-12px);
    box-shadow:0 20px 50px rgba(0,183,255,.2);
}

.card h3{
    margin-bottom:15px;
    color:#00b7ff;
}

.card .price{
    font-size:2rem;
    margin:15px 0;
    font-weight:bold;
}

/* Contact */

.contact-container{
    max-width:700px;
    margin:auto;
}

form{
    display:flex;
    flex-direction:column;
    gap:20px;
}

input,
textarea{
    padding:16px;
    border:none;
    border-radius:12px;
    background:rgba(255,255,255,.08);
    color:white;
}

input::placeholder,
textarea::placeholder{
    color:#ccc;
}

button{
    border:none;
    background:#00b7ff;
    color:white;
    font-weight:600;
    padding:16px;
    border-radius:12px;
    cursor:pointer;
    transition:.3s;
}

button:hover{
    background:#0095d9;
}

/* Footer */

footer{
    text-align:center;
    padding:30px;
    border-top:1px solid rgba(255,255,255,.1);
    color:#aaa;
}

/* Mobile */

@media(max-width:768px){

.hero h1{
    font-size:2.5rem;
}

nav{
    display:none;
}

.section{
    padding:80px 7%;
}
}

</style>
</head>

<body>

<div class="background-animation"></div>

<header>

<div class="logo">
WebBoost France
</div>

<nav>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
</nav>

</header>

<section class="hero">

<h1>
Boostez votre activité grâce à un site web professionnel
</h1>

<p>
Nous créons des sites modernes, rapides et optimisés pour transformer vos visiteurs en clients.
</p>

<a href="#contact" class="btn">
Demander un devis gratuit
</a>

</section>

<section id="services" class="section">

<h2 class="section-title">
Nos Services
</h2>

<p class="section-subtitle">
Des solutions adaptées aux entrepreneurs et PME
</p>

<div class="services">

<div class="card">
<h3>Site Vitrine</h3>
<div class="price">499€</div>
<p>
Présentez votre entreprise avec un site moderne et professionnel.
</p>
</div>

<div class="card">
<h3>Site Premium</h3>
<div class="price">999€</div>
<p>
Référencement Google, design avancé et optimisation complète.
</p>
</div>

<div class="card">
<h3>Maintenance</h3>
<div class="price">49€/mois</div>
<p>
Sécurité, mises à jour et assistance technique.
</p>
</div>

</div>

</section>

<section id="contact" class="section">

<h2 class="section-title">
Contact
</h2>

<p class="section-subtitle">
Parlez-nous de votre projet
</p>

<div class="contact-container">

<form>

<input
type="text"
placeholder="Votre nom"
required
>

<input
type="email"
placeholder="Votre adresse email"
required
>

<textarea
rows="6"
placeholder="Décrivez votre projet..."
required
></textarea>

<button type="submit">
Envoyer ma demande
</button>

</form>

</div>

</section>

<footer>
© 2026 WebBoost France • Tous droits réservés
</footer>

<script>

/* navbar */

window.addEventListener("scroll", () => {

document
.querySelector("header")
.classList.toggle("scrolled", window.scrollY > 50);

});

/* animation sections */

const observer = new IntersectionObserver((entries)=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

},{
threshold:0.2
});

document
.querySelectorAll(".section")
.forEach(section=>observer.observe(
