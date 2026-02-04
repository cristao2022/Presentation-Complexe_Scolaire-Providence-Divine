<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Salle Numérique - L'Avenir de Nos Enfants Commence Aujourd'hui</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
* {
margin: 0;
padding: 0;
box-sizing: border-box;
}
:root {
--primary: #1a365d;
--secondary: #2c5282;
--accent: #ffd23f;
--success: #28a745;
--warning: #ffc107;
--danger: #dc3545;
--light: #f8f9fa;
--dark: #343a40;
--text: #333;
--white: #fff;
}
body {
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
color: var(--text);
overflow-x: hidden;
min-height: 100vh;
}
.slides-container {
position: relative;
width: 100%;
min-height: 100vh;
padding-bottom: 100px;
}
.slide {
position: absolute;
top: 0;
left: 0;
width: 100%;
min-height: 100vh;
display: none;
flex-direction: column;
justify-content: flex-start;
align-items: center;
padding: 100px 60px 120px 60px;
text-align: center;
color: white;
opacity: 0;
transform: translateX(100%);
transition: all 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55);
z-index: 1;
overflow-y: auto;
}
.slide.active {
display: flex;
opacity: 1;
transform: translateX(0);
z-index: 10;
}
.slide.prev {
transform: translateX(-100%);
}
.slide.next {
transform: translateX(100%);
}
.slide-content {
background: rgba(255, 255, 255, 0.95);
border-radius: 25px;
padding: 60px;
max-width: 1200px;
width: 100%;
box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
animation: slideIn 0.8s ease-out;
margin-bottom: 40px;
}
@keyframes slideIn {
from {
opacity: 0;
transform: translateY(50px) scale(0.95);
}
to {
opacity: 1;
transform: translateY(0) scale(1);
}
}
.slide h1 {
font-size: 3.5em;
font-weight: 800;
margin-bottom: 30px;
color: var(--primary);
text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
line-height: 1.2;
background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}
.slide h2 {
font-size: 2em;
font-weight: 600;
margin-bottom: 40px;
color: var(--secondary);
line-height: 1.4;
}
.slide p {
font-size: 1.4em;
line-height: 1.8;
margin-bottom: 20px;
color: var(--text);
max-width: 900px;
}
.slide p.lead {
font-size: 1.8em;
font-weight: 600;
margin-bottom: 30px;
}
.slide p.quote {
font-size: 1.6em;
font-style: italic;
color: var(--secondary);
margin: 30px 0;
padding: 30px;
background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
color: white;
border-radius: 15px;
position: relative;
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}
.slide p.quote::before,
.slide p.quote::after {
content: '"';
font-size: 4em;
position: absolute;
opacity: 0.2;
color: white;
}
.slide p.quote::before {
top: -20px;
left: 10px;
}
.slide p.quote::after {
bottom: -40px;
right: 10px;
}
.slide ul {
list-style: none;
padding: 0;
margin: 30px 0;
text-align: left;
max-width: 800px;
}
.slide li {
font-size: 1.5em;
margin: 20px 0;
padding-left: 50px;
position: relative;
line-height: 1.6;
color: var(--text);
animation: fadeIn 0.6s ease-out;
}
@keyframes fadeIn {
from { opacity: 0; transform: translateX(-20px); }
to { opacity: 1; transform: translateX(0); }
}
.slide li:nth-child(1) { animation-delay: 0.1s; }
.slide li:nth-child(2) { animation-delay: 0.2s; }
.slide li:nth-child(3) { animation-delay: 0.3s; }
.slide li:nth-child(4) { animation-delay: 0.4s; }
.slide li:nth-child(5) { animation-delay: 0.5s; }
.slide li::before {
position: absolute;
left: 0;
top: 0;
font-size: 2em;
color: var(--secondary);
}
.comparison {
display: flex;
justify-content: space-around;
width: 100%;
max-width: 1000px;
margin: 40px 0;
gap: 40px;
}
.comparison-column {
flex: 1;
padding: 40px;
border-radius: 20px;
background: var(--light);
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
transition: transform 0.3s ease;
}
.comparison-column:hover {
transform: translateY(-10px);
}
.comparison-column h3 {
font-size: 2em;
margin-bottom: 30px;
color: var(--secondary);
text-align: center;
}
.comparison-column.before h3 {
color: var(--danger);
}
.comparison-column.after h3 {
color: var(--success);
}
.comparison-column p {
font-size: 1.3em;
margin: 15px 0;
color: var(--text);
text-align: left;
}
.price-box {
background: linear-gradient(135deg, var(--accent) 0%, #ff9800 100%);
padding: 50px;
border-radius: 25px;
text-align: center;
margin: 40px 0;
box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
animation: pulse 2s infinite;
}
@keyframes pulse {
0%, 100% { transform: scale(1); }
50% { transform: scale(1.03); }
}
.price-box h3 {
font-size: 1.8em;
margin-bottom: 20px;
color: var(--primary);
}
.price-amount {
font-size: 4.5em;
font-weight: 800;
color: var(--primary);
margin: 20px 0;
text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.2);
}
.price-description {
font-size: 1.4em;
color: var(--dark);
margin-top: 15px;
}
.highlight-box {
background: linear-gradient(135deg, var(--success) 0%, #20c997 100%);
padding: 40px;
border-radius: 20px;
margin: 30px 0;
color: white;
text-align: center;
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}
.warning-box {
background: linear-gradient(135deg, var(--warning) 0%, #ff9800 100%);
padding: 40px;
border-radius: 20px;
margin: 30px 0;
color: var(--dark);
text-align: center;
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}
.decision-box {
display: flex;
justify-content: space-around;
width: 100%;
max-width: 1100px;
margin: 40px 0;
gap: 30px;
}
.decision-option {
flex: 1;
padding: 40px;
border-radius: 20px;
text-align: center;
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}
.decision-option.no {
background: linear-gradient(135deg, var(--danger) 0%, #c82333 100%);
color: white;
}
.decision-option.yes {
background: linear-gradient(135deg, var(--success) 0%, #20c997 100%);
color: white;
}
.decision-option h3 {
font-size: 2em;
margin-bottom: 25px;
}
.decision-option p {
font-size: 1.3em;
margin: 15px 0;
line-height: 1.6;
}
.slide-counter {
position: fixed;
top: 30px;
right: 40px;
background: rgba(255, 255, 255, 0.95);
padding: 15px 35px;
border-radius: 50px;
font-size: 1.3em;
font-weight: 700;
color: var(--primary);
box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
z-index: 100;
}
.dots-container {
position: fixed;
bottom: 40px;
left: 50%;
transform: translateX(-50%);
display: flex;
gap: 12px;
z-index: 100;
background: rgba(255, 255, 255, 0.95);
padding: 12px 25px;
border-radius: 30px;
box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
}
.dot {
width: 12px;
height: 12px;
border-radius: 50%;
background: rgba(44, 82, 130, 0.5);
cursor: pointer;
transition: all 0.3s ease;
}
.dot.active {
background: var(--secondary);
transform: scale(1.4);
box-shadow: 0 0 10px rgba(44, 82, 130, 0.8);
}
.dot:hover {
background: var(--secondary);
transform: scale(1.3);
}
.progress-bar {
position: fixed;
top: 0;
left: 0;
height: 6px;
background: linear-gradient(90deg, var(--primary) 0%, var(--secondary) 100%);
z-index: 1000;
transition: width 0.5s ease;
}
.school-info {
margin-top: 50px;
font-size: 1.3em;
color: var(--secondary);
font-weight: 600;
}
.contact-info {
background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
padding: 40px;
border-radius: 20px;
margin: 30px 0;
color: white;
text-align: left;
max-width: 800px;
}
.contact-info h3 {
font-size: 1.8em;
margin-bottom: 20px;
text-align: center;
}
.contact-info p {
font-size: 1.3em;
margin: 15px 0;
line-height: 1.8;
}
.icon-text {
display: flex;
align-items: center;
gap: 15px;
margin: 15px 0;
}
.icon {
font-size: 2em;
color: var(--accent);
}
/* Responsividade */
@media (max-width: 1024px) {
.slide {
padding: 80px 40px 100px 40px;
}
.slide h1 {
font-size: 2.8em;
}
.slide h2 {
font-size: 1.8em;
}
.slide p {
font-size: 1.3em;
}
.slide-content {
padding: 40px;
}
.price-amount {
font-size: 3.5em;
}
.dots-container {
bottom: 30px;
gap: 8px;
}
.dot {
width: 10px;
height: 10px;
}
}
@media (max-width: 768px) {
.slide {
padding: 60px 25px 90px 25px;
}
.slide h1 {
font-size: 2.3em;
}
.slide h2 {
font-size: 1.6em;
}
.slide p {
font-size: 1.2em;
}
.slide-content {
padding: 30px 20px;
}
.comparison,
.decision-box {
flex-direction: column;
gap: 20px;
}
.price-amount {
font-size: 2.8em;
}
.slide-counter {
top: 20px;
right: 20px;
padding: 10px 25px;
font-size: 1.1em;
}
.dots-container {
bottom: 25px;
gap: 6px;
padding: 10px 20px;
}
.dot {
width: 8px;
height: 8px;
}
}
@media (max-width: 480px) {
.slide {
padding: 50px 20px 80px 20px;
}
.slide h1 {
font-size: 2em;
}
.slide h2 {
font-size: 1.4em;
}
.slide p {
font-size: 1.1em;
}
.price-amount {
font-size: 2.2em;
}
.slide-counter {
display: none;
}
.dots-container {
bottom: 20px;
padding: 8px 15px;
}
.dot {
width: 7px;
height: 7px;
}
}
</style>
</head>
<body>
<div class="progress-bar" id="progressBar"></div>
<div class="slides-container">
<!-- Slide 1: Couverture -->
<div class="slide active" id="slide1">
<div class="slide-content">
<h1>L'AVENIR DE LA RÉPUBLIQUE DÉMOCRATIQUE DU CONGO COMMENCE DANS LA SALLE DE CLASSE</h1>
<h2>Pourquoi nous créons une Salle Numérique dans notre école</h2>
<p class="quote">Nous ne formons pas seulement des élèves.<br>Nous formons les ingénieurs, médecins, professeurs et leaders<br>qui vont reconstruire et développer la République Démocratique du Congo.</p>
<div class="school-info">
<p>Complexe Scolaire Tatiana - Ciel Bleu</p>
<p>Cité Verte, Commune de Selembao - Kinshasa | Février 2026</p>
</div>
</div>
</div>
<!-- Slide 2: Réalité -->
<div class="slide" id="slide2">
<div class="slide-content">
<h1>Une réalité que tout parent congolais connaît</h1>
<p class="lead">"Je veux que mon enfant ait plus d'opportunités que moi"</p>
<ul>
<li><i class="fas fa-history"></i> Nous avons grandi dans une période difficile de notre histoire</li>
<li><i class="fas fa-book"></i> Nous avons eu un accès limité aux livres et matériels scolaires</li>
<li><i class="fas fa-dream"></i> Nous rêvons d'un avenir meilleur pour nos enfants</li>
</ul>
<div class="highlight-box">
<p style="font-size: 1.6em; font-weight: 600;">Aujourd'hui, la République Démocratique du Congo avance avec force, mais nos écoles doivent suivre ce progrès.</p>
</div>
<p class="lead"><strong>Votre enfant mérite d'apprendre avec les outils du XXIème siècle — pas du siècle dernier.</strong></p>
<p style="font-size: 1.4em; font-weight: 600; color: var(--secondary);">La technologie n'est pas un luxe. C'est le pont entre le rêve de votre enfant et la réalité de son avenir.</p>
</div>
</div>
<!-- Slide 3: Qu'est-ce que la Salle Numérique -->
<div class="slide" id="slide3">
<div class="slide-content">
<h1>Qu'est-ce que, vraiment, une Salle Numérique ?</h1>
<div class="warning-box">
<p style="font-size: 1.8em; font-weight: 700;">Ce n'est pas "un ordinateur dans la salle". C'est ouvrir des fenêtres sur le monde.</p>
</div>
<ul>
<li><i class="fas fa-globe-africa"></i> Recherche dans des bibliothèques numériques du monde entier</li>
<li><i class="fas fa-satellite"></i> Visualise le fleuve Congo vu de l'espace, la faune du Bandundu en HD</li>
<li><i class="fas fa-gamepad"></i> Pratique avec des simulations interactives — sans quitter l'école</li>
<li><i class="fas fa-laptop-code"></i> Développe la confiance avec les outils de l'université et du travail</li>
</ul>
<p class="quote">C'est comme donner des ailes à la connaissance — sans quitter notre terre, mais connecté au monde.</p>
<div class="highlight-box">
<p style="font-size: 1.3em;"><strong>Important :</strong> Nous utilisons la technologie vCloudPoint — solution intelligente qui permet à plusieurs élèves d'utiliser simultanément un système centralisé, garantissant stabilité, sécurité et faible consommation d'énergie.</p>
</div>
</div>
</div>
<!-- Slide 4: Avant x Après -->
<div class="slide" id="slide4">
<div class="slide-content">
<h1>Bénéfices concrets dans la vie quotidienne de votre enfant</h1>
<div class="comparison">
<div class="comparison-column before">
<h3><i class="fas fa-times-circle"></i> AVANT</h3>
<p><i class="fas fa-book"></i> Lit sur le pétrole dans un livre dépassé</p>
<p><i class="fas fa-pen"></i> Copie les cartes de la RDC à la main</p>
<p><i class="fas fa-hourglass-half"></i> Attend des mois pour un livre de la bibliothèque</p>
<p><i class="fas fa-file"></i> Rend un travail manuscrit</p>
</div>
<div class="comparison-column after">
<h3><i class="fas fa-check-circle"></i> APRÈS</h3>
<p><i class="fas fa-oil-well"></i> Explore une plateforme pétrolière avec animation 3D</p>
<p><i class="fas fa-map-marked-alt"></i> Interagit avec des cartes numériques de notre pays</p>
<p><i class="fas fa-book-reader"></i> Accède à des milliers de livres numériques en français</p>
<p><i class="fas fa-presentation"></i> Crée des présentations avec photos, audio et texte</p>
</div>
</div>
<div class="highlight-box">
<p style="font-size: 1.5em; font-weight: 600;">Votre enfant apprend sur la République Démocratique du Congo et le monde en profondeur, avec fierté et curiosité — développant des compétences que le marché du travail exige.</p>
</div>
</div>
</div>
<!-- Slide 5: Compétences -->
<div class="slide" id="slide5">
<div class="slide-content">
<h1>Compétences pour le marché du travail congolais</h1>
<p class="lead">La RDC a urgemment besoin de jeunes préparés pour :</p>
<ul>
<li><i class="fas fa-industry"></i> <strong>Secteur pétrolier et minier</strong> — rapports techniques, analyse de données</li>
<li><i class="fas fa-seedling"></i> <strong>Agriculture moderne</strong> — gestion des cultures avec technologie adaptée</li>
<li><i class="fas fa-landmark"></i> <strong>Tourisme</strong> — contenus numériques sur les merveilles de la RDC</li>
<li><i class="fas fa-lightbulb"></i> <strong>Entrepreneuriat</strong> — entreprises en ligne qui génèrent des revenus familiaux</li>
</ul>
<p class="lead" style="margin-top: 40px;">Dans la Salle Numérique, votre enfant développe naturellement :</p>
<ul>
<li><i class="fas fa-laptop"></i> <strong>Maîtrise de l'ordinateur</strong> — essentiel pour tout emploi formel</li>
<li><i class="fas fa-search"></i> <strong>Recherche en ligne</strong> — trouver des bourses, stages et concours</li>
<li><i class="fas fa-envelope"></i> <strong>Communication numérique</strong> — emails professionnels, CV modernes</li>
<li><i class="fas fa-brain"></i> <strong>Pensée critique</strong> — discerner les vraies nouvelles des fausses</li>
</ul>
<p class="quote">Nous ne formons pas seulement des élèves. Nous formons de futurs contributeurs au développement durable de la République Démocratique du Congo.</p>
</div>
</div>
<!-- Slide 6: En pratique -->
<div class="slide" id="slide6">
<div class="slide-content">
<h1>En pratique : ce que votre enfant fera dans la Salle Numérique</h1>
<ul>
<li><i class="fas fa-map"></i> <strong>Géographie :</strong> Explorer des cartes interactives des provinces — rivières, montagnes, ressources naturelles</li>
<li><i class="fas fa-binoculars"></i> <strong>Géographie :</strong> Comparer des images satellites de Kinshasa en 1990 et 2026</li>
<li><i class="fas fa-landmark"></i> <strong>Histoire :</strong> "Visiter" virtuellement le Musée National de l'Histoire Militaire</li>
<li><i class="fas fa-video"></i> <strong>Histoire :</strong> Écouter les témoignages des héros de l'indépendance</li>
<li><i class="fas fa-seedling"></i> <strong>Sciences :</strong> Simuler la culture du maïs, manioc, haricots adaptés au climat</li>
<li><i class="fas fa-newspaper"></i> <strong>Français :</strong> Créer un journal numérique sur les traditions de la commune</li>
<li><i class="fas fa-podcast"></i> <strong>Français :</strong> Enregistrer des podcasts avec des légendes congolaises</li>
</ul>
<div class="highlight-box">
<p style="font-size: 1.6em; font-weight: 600;">La technologie valorise notre identité — elle n'efface pas notre culture. Au contraire : elle lui donne voix et portée mondiale.</p>
</div>
</div>
</div>
<!-- Slide 7: Égalité -->
<div class="slide" id="slide7">
<div class="slide-content">
<h1>Égalité des opportunités : justice pour tous les enfants</h1>
<div class="warning-box">
<p style="font-size: 1.6em; font-weight: 600;">Réalité congolaise que nous ne pouvons ignorer :</p>
</div>
<ul>
<li><i class="fas fa-times"></i> Beaucoup de familles n'ont pas d'ordinateur à la maison</li>
<li><i class="fas fa-times"></i> Les enfants des zones rurales sont plus éloignés du monde numérique</li>
<li><i class="fas fa-times"></i> Sans accès à l'école, ces enfants n'auront jamais l'opportunité</li>
</ul>
<div class="highlight-box" style="margin-top: 40px;">
<p style="font-size: 1.6em; font-weight: 600;">Avec la Salle Numérique de notre école :</p>
</div>
<ul>
<li><i class="fas fa-check"></i> Tous les élèves — du quartier élégant ou du bidonville — ont un accès égal</li>
<li><i class="fas fa-check"></i> Personne n'est laissé pour compte à cause de la condition économique</li>
<li><i class="fas fa-check"></i> L'école promeut la justice sociale et l'inclusion</li>
</ul>
<p class="quote">Dans notre école, le fils du chauffeur a les mêmes opportunités que le fils du directeur.<br>Parce que le talent n'a pas d'adresse — et l'éducation doit être le droit de tous les enfants de la République Démocratique du Congo.</p>
</div>
</div>
<!-- Slide 8: Université -->
<div class="slide" id="slide8">
<div class="slide-content">
<h1>Préparation pour l'université en RDC et à l'étranger</h1>
<p class="lead">Universités (UNIKIN, UPN, ISTA, ISP) exigent de plus en plus :</p>
<ul>
<li><i class="fas fa-file-word"></i> Travaux numériques formatés correctement dans Word</li>
<li><i class="fas fa-database"></i> Recherche dans des bases de données académiques (pas seulement Google)</li>
<li><i class="fas fa-laptop"></i> Utilisation de plateformes comme Moodle pour les cours et évaluations</li>
<li><i class="fas fa-chart-line"></i> Présentations professionnelles dans PowerPoint</li>
</ul>
<div class="warning-box" style="margin-top: 40px;">
<p style="font-size: 1.6em; font-weight: 600;">Sans pratique scolaire préalable :</p>
<ul style="text-align: left; margin-top: 20px;">
<li><i class="fas fa-exclamation-triangle"></i> L'élève perd confiance dès le premier semestre</li>
<li><i class="fas fa-money-bill"></i> Dépense de l'argent pour des cours de base qui devraient être gratuits</li>
<li><i class="fas fa-frown"></i> Abandonne ses rêves par honte de ne pas savoir utiliser les outils</li>
</ul>
</div>
<div class="highlight-box" style="margin-top: 30px;">
<p style="font-size: 1.6em; font-weight: 600;">La Salle Numérique élimine cette barrière avant qu'elle ne détruise des rêves et des potentiels.</p>
</div>
</div>
</div>
<!-- Slide 9: Sécurité -->
<div class="slide" id="slide9">
<div class="slide-content">
<h1>Sécurité et respect des valeurs familiales</h1>
<div class="warning-box">
<p style="font-size: 1.6em; font-weight: 600;">Préoccupation légitime de tout père et mère congolais :</p>
<p style="font-size: 1.8em; font-weight: 700; margin-top: 15px;">"La technologie va-t-elle éloigner mon enfant de nos valeurs ?"</p>
</div>
<div class="highlight-box" style="margin-top: 30px;">
<p style="font-size: 1.6em; font-weight: 600;">Dans notre Salle Numérique :</p>
</div>
<ul>
<li><i class="fas fa-shield-alt"></i> <strong>Contenu 100% contrôlé</strong> — uniquement des matériels éducatifs approuvés</li>
<li><i class="fas fa-chalkboard-teacher"></i> <strong>Professeur supervise</strong> toutes les activités en temps réel</li>
<li><i class="fas fa-flag"></i> <strong>Focus sur la culture congolaise</strong> — traditions, langues nationales, histoire</li>
<li><i class="fas fa-ban"></i> <strong>Interdit réseaux sociaux, jeux</strong> et contenus inappropriés</li>
</ul>
<p class="quote">La technologie dans notre école respecte les valeurs de la famille congolaise :<br>respect des aînés, discipline, travail ardu et amour de la patrie.</p>
</div>
</div>
<!-- Slide 10: Exemples africains -->
<div class="slide" id="slide10">
<div class="slide-content">
<h1>L'exemple des pays africains qui ont progressé</h1>
<ul>
<li><i class="fas fa-chart-line"></i> <strong>l'Ile Maurice :</strong> A investi tôt dans les salles numériques — aujourd'hui référence technologique en Afrique</li>
<li><i class="fas fa-users"></i> <strong>Kenya :</strong> Programme "Digital Literacy" a atteint 1,2 million d'enfants</li>
<li><i class="fas fa-briefcase"></i> <strong>Ghana :</strong> Jeunes ont créé des startups qui ont attiré des millions en investissement</li>
</ul>
<div class="highlight-box" style="margin-top: 40px;">
<p style="font-size: 1.8em; font-weight: 700;">La République Démocratique du Congo a tout pour être le prochain grand succès africain — mais seulement si nous investissons AUJOURD'HUI dans l'éducation numérique de nos enfants.</p>
</div>
<p class="quote">Les pays qui ont progressé n'avaient pas plus d'argent que nous.<br>Ils avaient plus de courage pour investir dans les enfants.</p>
</div>
</div>
<!-- Slide 11: Témoignage -->
<div class="slide" id="slide11">
<div class="slide-content">
<h1>Une voix qui représente beaucoup de familles</h1>
<p class="quote" style="font-size: 1.5em; line-height: 1.8;">
Je suis mère célibataire, je travaille comme vendeuse au marché depuis 5h du matin.<br><br>
Je n'ai pas les moyens d'acheter un ordinateur pour mon fils — ni même internet à la maison.<br><br>
Quand j'ai appris que l'école aura une Salle Numérique, j'ai pleuré de joie.<br><br>
Mon fils ne sera pas laissé pour compte.<br><br>
Il aura aussi droit à l'avenir — comme n'importe quel enfant dans n'importe quel pays du monde.
</p>
<p style="font-size: 1.4em; font-weight: 600; margin-top: 20px; color: var(--secondary);">— Mère d'élève de 6ème année, Kinshasa</p>
<div class="highlight-box" style="margin-top: 40px;">
<p style="font-size: 1.6em; font-weight: 600;">👉 Combien de mères et pères dans cette salle ressentent exactement la même chose ?</p>
</div>
</div>
</div>
<!-- Slide 12: Partenariat -->
<div class="slide" id="slide12">
<div class="slide-content">
<h1>Un projet possible grâce à un partenariat responsable</h1>
<div class="warning-box">
<p style="font-size: 1.8em; font-weight: 700;">Notre école n'a pas les ressources pour faire cela seule.<br>Mais nous refusons de laisser nos enfants pour compte.</p>
</div>
<p class="lead" style="margin-top: 30px;">Comme beaucoup d'écoles en RDC, nous faisons face à :</p>
<ul>
<li><i class="fas fa-exclamation-triangle"></i> Budget limité — priorité a toujours été les professeurs qualifiés</li>
<li><i class="fas fa-exclamation-triangle"></i> Investissement initial en technologie exige des capitaux que nous ne disposons pas</li>
</ul>
<div class="highlight-box" style="margin-top: 30px;">
<p style="font-size: 1.6em; font-weight: 600;">C'est pourquoi nous avons décidé d'agir avec responsabilité et vision :</p>
</div>
<ul>
<li><i class="fas fa-handshake"></i> Nous avons cherché un partenaire sérieux, congolais et engagé dans l'éducation</li>
<li><i class="fas fa-building"></i> Nous avons trouvé Pulsar Tech, avec une expérience prouvée</li>
<li><i class="fas fa-project-diagram"></i> Nous avons établi un partenariat de collaboration où :</li>
</ul>
<div class="price-box">
<h3>Contribution mensuelle par élève</h3>
<div class="price-amount">5 USD</div>
<p class="price-description">(moins qu'un snack par jour — mais avec un impact pour toute la vie de votre enfant)</p>
</div>
<p class="lead"><strong>Cette valeur assure :</strong></p>
<ul>
<li><i class="fas fa-tools"></i> Maintenance technique continue (technicien dédié)</li>
<li><i class="fas fa-wifi"></i> Internet dédié à haute vitesse</li>
<li><i class="fas fa-recycle"></i> Retour progressif de l'investissement de Pulsar Tech</li>
</ul>
<p class="quote">Ce n'est pas une taxe scolaire. C'est un engagement partagé :<br>l'école offre l'espace et les professeurs,<br>Pulsar Tech offre la technologie,<br>et nous, parents, garantissons la durabilité avec une contribution accessible.</p>
</div>
</div>
<!-- Slide 13: Solidarité -->
<div class="slide" id="slide13">
<div class="slide-content">
<h1>Solidarité et flexibilité : personne n'est exclu</h1>
<div class="price-box" style="background: linear-gradient(135deg, var(--success) 0%, #20c997 100%);">
<p style="font-size: 2em; margin-bottom: 20px;">5 USD est accessible</p>
<div class="price-amount" style="font-size: 5em; color: white;">5 USD</div>
<p class="price-description" style="font-size: 1.8em; color: var(--primary); margin-top: 20px;">et PERSONNE ne sera exclu pour des difficultés économiques</p>
</div>
<div class="highlight-box" style="margin-top: 40px; background: linear-gradient(135deg, var(--warning) 0%, #ff9800 100%); color: var(--dark);">
<p style="font-size: 1.6em; font-weight: 600;">Le souci de chaque parent ici présent c'est l'avenir de son enfant en termes des opportunités dans le marché du travail.<br><br>Parce que nous croyons que le droit à l'éducation numérique ne peut pas dépendre de la condition économique.</p>
</div>
</div>
</div>
<!-- Slide 14: Appel final -->
<div class="slide" id="slide14">
<div class="slide-content">
<h1>Appel final : votre "oui" change des vies</h1>
<p class="lead">Aujourd'hui vous décidez avec le cœur de père/mère congolais</p>
<div class="decision-box">
<div class="decision-option no">
<h3><i class="fas fa-times"></i> Dire "non"</h3>
<p style="font-style: italic; margin-bottom: 20px;">"5 USD... je vais réfléchir..."</p>
<p><i class="fas fa-arrow-right"></i> Votre enfant perd l'accès quotidien à la technologie</p>
<p><i class="fas fa-arrow-right"></i> Arrive à l'université sans base numérique</p>
<p><i class="fas fa-arrow-right"></i> Reste en arrière dans un monde qui n'attend pas</p>
</div>
<div class="decision-option yes">
<h3><i class="fas fa-check"></i> Dire "oui"</h3>
<p style="font-style: italic; margin-bottom: 20px;">"5 USD par mois est mon investissement dans l'avenir"</p>
<p><i class="fas fa-arrow-right"></i> Il apprend des compétences qui valent des millions</p>
<p><i class="fas fa-arrow-right"></i> Entre à l'université avec confiance</p>
<p><i class="fas fa-arrow-right"></i> A la fierté d'être congolais préparé</p>
</div>
</div>
<p class="quote" style="font-size: 1.6em; line-height: 1.8;">
Nous ne vendons pas de technologie.<br>
Nous offrons dignité, opportunité et espoir.<br><br>
Et 5 USD par mois est peu pour qui aime son enfant assez<br>
pour investir en lui tous les jours.
</p>
</div>
</div>
<!-- Slide 15: Conclusion -->
<div class="slide" id="slide15">
<div class="slide-content">
<h1>MERCI DE CROIRE EN L'AVENIR DE NOS ENFANTS</h1>
<div class="highlight-box">
<p style="font-size: 1.5em; line-height: 1.8;">
Nous vous remercions pour votre présence, votre attention et, par-dessus tout, votre amour de père/mère — cet amour qui déplace des montagnes et transforme des réalités.
</p>
</div>
<div class="highlight-box" style="margin-top: 30px; background: linear-gradient(135deg, var(--accent) 0%, #ff9800 100%); color: var(--primary);">
<p style="font-size: 1.6em; font-weight: 600;">Ce projet n'existe que parce que :</p>
</div>
<ul style="margin-top: 30px;">
<li><i class="fas fa-heart"></i> <strong>L'école</strong> croit en l'éducation comme moteur de transformation nationale</li>
<li><i class="fas fa-heart"></i> <strong>Pulsar Tech</strong> croit au potentiel immense des enfants congolais</li>
<li><i class="fas fa-heart"></i> <strong>Vous</strong> croyez en votre enfant — et êtes prêt à lui donner les outils pour voler</li>
</ul>
<div class="highlight-box" style="margin-top: 40px; background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%); color: white;">
<p style="font-size: 1.6em; font-weight: 600; line-height: 1.8;">
Ensemble, nous construisons plus qu'une Salle Numérique.<br>
Nous construisons la génération qui portera la République Démocratique du Congo plus loin — avec compétence, fierté et vision.
</p>
</div>
<p class="quote" style="font-size: 1.3em; line-height: 1.8;">
L'enfant qui apprend aujourd'hui avec la technologie à l'école<br>
sera l'ingénieur qui demain construira des routes à Kikwit,<br>
le médecin qui guérira avec dignité à Kisangani,<br>
le professeur qui inspirera de nouvelles générations à Lubumbashi,<br>
l'entrepreneur qui créera des emplois et richesse à Kinshasa,<br>
l'agriculteur qui nourrira le pays avec innovation à Kananga.<br><br>
<strong>C'est l'avenir que nous construisons — ensemble.</strong>
</p>
</div>
</div>
<!-- Slide 16: Contact -->
<div class="slide" id="slide16">
<div class="slide-content">
<h1>Informations pratiques et contact</h1>
<div class="contact-info">
<h3><i class="fas fa-calendar-alt"></i> Prochaines étapes</h3>
<p><i class="fas fa-dot-circle"></i> <strong>Inauguration de la Salle Numérique :</strong> Le jour de la fin de l'année scolaire 2026</p>
<h3 style="margin-top: 30px;"><i class="fas fa-handshake"></i> Partenariat responsable</h3>
<p><i class="fas fa-school"></i> <strong>École :</strong> [Nom complet de l'École]</p>
<p><i class="fas fa-laptop-code"></i> <strong>Partenaire technologique :</strong> Pulsar Tech</p>
<p><i class="fas fa-cogs"></i> <strong>Portée :</strong> Infrastructure, maintenance et connectivité Internet dédiée</p>
<h3 style="margin-top: 30px;"><i class="fas fa-phone"></i> Contacts</h3>
<p><i class="fas fa-building"></i> <strong>Secrétariat de l'École :</strong> [Téléphone] | [Email]</p>
<p><i class="fas fa-user-tie"></i> <strong>Directeur(trice) :</strong> [Nom du Directeur] – [Téléphone]</p>
<p><i class="fas fa-user-graduate"></i> <strong>Coordinateur du Projet :</strong> [Nom] – [Téléphone/WhatsApp]</p>
</div>
<p class="quote" style="font-size: 1.5em; line-height: 1.8; margin-top: 30px;">
Ne laissons pas l'hésitation d'aujourd'hui<br>
se transformer en regret de demain.<br><br>
L'avenir de nos enfants n'attend pas —<br>
et nous ne pouvons pas les décevoir.
</p>
</div>
</div>
</div>
<div class="slide-counter" id="slideCounter">Slide 1 de 16</div>
<div class="dots-container" id="dotsContainer"></div>
<script>
document.addEventListener('DOMContentLoaded', function() {
const totalSlides = 16;
let currentSlide = 1;
// Créer dots de navigation
const dotsContainer = document.getElementById('dotsContainer');
for (let i = 1; i <= totalSlides; i++) {
const dot = document.createElement('div');
dot.className = 'dot';
dot.dataset.slide = i;
dot.addEventListener('click', () => goToSlide(i));
dotsContainer.appendChild(dot);
}
// Mettre à jour UI initial
updateUI();
// Fonction pour aller au slide spécifique
function goToSlide(slideNumber) {
if (slideNumber < 1 || slideNumber > totalSlides) return;
// Supprimer classes des slides anciens
document.querySelectorAll('.slide').forEach(slide => {
slide.classList.remove('active', 'prev', 'next');
});
// Ajouter classes de transition
if (slideNumber > currentSlide) {
document.getElementById(`slide${currentSlide}`).classList.add('prev');
} else if (slideNumber < currentSlide) {
document.getElementById(`slide${currentSlide}`).classList.add('next');
}
// Montrer nouveau slide
document.getElementById(`slide${slideNumber}`).classList.add('active');
currentSlide = slideNumber;
updateUI();
// Faire défiler doucement vers le haut
window.scrollTo({ top: 0, behavior: 'smooth' });
}
// Fonction pour slide suivant
function nextSlide() {
if (currentSlide < totalSlides) {
goToSlide(currentSlide + 1);
}
}
// Fonction pour slide précédent
function prevSlide() {
if (currentSlide > 1) {
goToSlide(currentSlide - 1);
}
}
// Mettre à jour UI (compteur, dots, boutons)
function updateUI() {
document.getElementById('slideCounter').textContent = `Slide ${currentSlide} de ${totalSlides}`;
// Mettre à jour dots
document.querySelectorAll('.dot').forEach((dot, index) => {
dot.classList.toggle('active', index + 1 === currentSlide);
});
// Mettre à jour barre de progression
const progress = ((currentSlide - 1) / (totalSlides - 1)) * 100;
document.getElementById('progressBar').style.width = `${progress}%`;
}
// Navigation par clavier - CORRIGÉ : PageUp/PageDown n'interfèrent pas
document.addEventListener('keydown', function(e) {
// SEULEMENT flèches horizontales, espace, Home, End et chiffres 1-9 naviguent entre slides
if (e.key === 'ArrowLeft') {
e.preventDefault(); // Empêche défilement horizontal
prevSlide();
}
else if (e.key === 'ArrowRight' || e.key === ' ') {
e.preventDefault(); // Empêche défilement avec espace
nextSlide();
}
else if (e.key === 'Home') {
e.preventDefault();
goToSlide(1);
}
else if (e.key === 'End') {
e.preventDefault();
goToSlide(totalSlides);
}
else if (e.key >= '1' && e.key <= '9') {
e.preventDefault();
const slideNum = parseInt(e.key);
if (slideNum <= totalSlides) {
goToSlide(slideNum);
}
}
// PageUp, PageDown, ArrowUp, ArrowDown NE SONT PAS traités ici
// → comportement par défaut du navigateur : défilement de la page
});
// Swipe pour mobile
let touchStartX = 0;
let touchEndX = 0;
document.addEventListener('touchstart', function(e) {
touchStartX = e.changedTouches[0].screenX;
});
document.addEventListener('touchend', function(e) {
touchEndX = e.changedTouches[0].screenX;
handleSwipe();
});
function handleSwipe() {
const swipeThreshold = 50;
if (touchStartX - touchEndX > swipeThreshold) {
nextSlide();
} else if (touchEndX - touchStartX > swipeThreshold) {
prevSlide();
}
}
// Démarrer présentation
goToSlide(1);
});
</script>
</body>
</html>
