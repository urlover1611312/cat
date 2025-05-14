<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Compliment Cat</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <div class="cat"></div>
  <div id="compliment">Click the button to receive a compliment!</div>
  <button id="complimentBtn">Click me</button>

  <script src="script.js"></script>
</body>
</html>body {
  margin: 0;
  padding: 0;
  background-color: #2e003e; /* dark purple */
  color: white;
  font-family: 'Arial', sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow: hidden;
  text-align: center;
}

.cat {
  width: 150px;
  height: 150px;
  background: black;
  border-radius: 50% 50% 45% 45%;
  position: relative;
  animation: bounce 2s infinite;
}

.cat::before,
.cat::after {
  content: '';
  position: absolute;
  width: 40px;
  height: 40px;
  background: black;
  border-radius: 50%;
  top: -20px;
}

.cat::before {
  left: -10px;
}

.cat::after {
  right: -10px;
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
}

#compliment {
  margin: 20px;
  font-size: 1.5em;
  max-width: 90%;
}

button {
  padding: 10px 20px;
  font-size: 1.2em;
  background-color: #8e44ad;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #732d91;
}
const compliments = [
  "You have impeccable manners.",
  "I like your style.",
  "You have the best laugh.",
  "I appreciate you.",
  "You are the most perfect you there is.",
  "You are enough.",
  "You're strong.",
  "Your perspective is refreshing.",
  "I'm grateful to know you.",
  "You light up the room.",
  "You deserve a hug right now.",
  "You should be proud of yourself.",
  "You're more helpful than you realize.",
  "You have a great sense of humor.",
  "You've got all the right moves!",
  "Is that your picture next to 'charming' in the dictionary?",
  "Your kindness is a balm to all who encounter it.",
  "You're all that and a super-size bag of chips.",
  "On a scale from 1 to 10, you're an 11.",
  "You are brave.",
  "You're even more beautiful on the inside than you are on the outside.",
  "You have the courage of your convictions.",
  "Aside from food, you're my favorite.",
  "If cartoon bluebirds were real, a bunch of them would be sitting on your shoulders singing right now.",
  "You're like sunshine on a rainy day.",
  "You bring out the best in other people.",
  "Your ability to recall random factoids at just the right time is impressive.",
  "You're a great listener.",
  "How is it that you always look great, even in sweatpants?",
  "Everything would be better if more people were like you!",
  "I bet you sweat glitter.",
  "You were cool way before hipsters were cool.",
  "That color is perfect on you.",
  "Hanging out with you is always a blast.",
  "You always know — and say — exactly what I need to hear when I need to hear it.",
  "You smell really good.",
  "You may dance like no one's watching, but everyone's watching because you're an amazing dancer!",
  "Being around you makes everything better!",
  "When you say, 'I meant to do that,' I totally believe you.",
  "When you're not afraid to be yourself is when you're most incredible.",
  "Colors seem brighter when you're around.",
  "You're more fun than a ball pit filled with candy.",
  "You're someone's reason to smile.",
  "You're even better than a unicorn, because you're real.",
  "How do you keep being so funny and making everyone laugh?",
  "You have a good head on your shoulders.",
  "Has anyone ever told you that you have great posture?",
  "The way you treasure your loved ones is incredible.",
  "You're really something special.",
  "You're a gift to those around you.",
  "You're a smart cookie.",
  "You are awesome!",
  "You have a good heart.",
  "Your smile is contagious.",
  "You look great today.",
  "You're a ray of sunshine.",
  "You light up the world.",
  "You deserve all the good things.",
  "You're making a difference.",
  "You're like a rainbow.",
  "You're a true friend.",
  "You're an inspiration.",
  "You're as sweet as honey.",
  "You're thoughtful.",
  "You bring joy wherever you go.",
  "You're beautiful inside and out.",
  "You're one of a kind.",
  "You're making this world a better place.",
  "You're lovable.",
  "You're courageous.",
  "You're wonderful.",
  "You're extraordinary.",
  "You're talented.",
  "You're creative.",
  "You're thoughtful.",
  "You're a star.",
  "You're a delight.",
  "You're a dream come true.",
  "You're a gem.",
  "You're a blessing.",
  "You're amazing.",
  "You're radiant.",
  "You're the best!",
  "You're cool.",
  "You're so special.",
  "You're warm-hearted.",
  "You're a joy to be around.",
  "You're precious.",
  "You're awesome sauce.",
  "You're sweet.",
  "You're gifted.",
  "You're kind.",
  "You're charming.",
  "You're unique.",
  "You're full of life.",
  "You're full of grace.",
  "You're incredible.",
  "You're honest.",
  "You're loving.",
  "You're delightful.",
  "You're spunky.",
  "You're magnetic.",
  "You're luminous.",
  "You're thoughtful.",
  "You're the icing on the cake.",
  "You're the cherry on top.",
  "You're the best part of my day."
];

document.addEventListener("DOMContentLoaded", () => {
  const btn = document.getElementById("complimentBtn");
  const display = document.getElementById("compliment");

  btn.addEventListener("click", () => {
    const compliment = compliments[Math.floor(Math.random() * compliments.length)];
    display.textContent = compliment;
  });
});
