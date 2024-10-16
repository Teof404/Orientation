<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Test d'Orientation</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    .question {
      margin-bottom: 20px;
    }
    .btn {
      margin-top: 20px;
    }
  </style>
</head>
<body>

<h1>Test d'Orientation Professionnelle</h1>

<div class="question">
  <p><strong>1. Quels types d’activités t’attirent le plus ?</strong></p>
  <input type="radio" name="q1" value="a"> Résolution de problèmes techniques<br>
  <input type="radio" name="q1" value="b"> Création artistique<br>
  <input type="radio" name="q1" value="c"> Interaction avec des gens<br>
  <input type="radio" name="q1" value="d"> Gestion et organisation de projets<br>
  <input type="radio" name="q1" value="e"> Travail manuel ou physique<br>
</div>

<div class="question">
  <p><strong>2. Sur quels sujets pourrais-tu passer des heures sans te lasser ?</strong></p>
  <input type="radio" name="q2" value="a"> Technologie et innovation<br>
  <input type="radio" name="q2" value="b"> Psychologie ou relations humaines<br>
  <input type="radio" name="q2" value="c"> Arts et culture<br>
  <input type="radio" name="q2" value="d"> Finance et économie<br>
  <input type="radio" name="q2" value="e"> Nature et environnement<br>
</div>

<button class="btn" onclick="calculateResults()">Voir les résultats</button>

<script>
  function calculateResults() {
    let results = {};
    let totalPoints = 0;

    const questions = document.querySelectorAll('.question input[type="radio"]:checked');
    questions.forEach((q) => {
      const answer = q.value;
      totalPoints++;
      results[answer] = (results[answer] || 0) + 1;
    });

    alert("Tu as terminé le test ! Nous allons maintenant interpréter tes réponses.");
    // Traitement des résultats ici en fonction des réponses
  }
</script>

</body>
</html>
