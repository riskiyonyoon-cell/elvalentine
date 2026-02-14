<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>El & Eli 💗</title>

<style>
* {
  box-sizing: border-box;
  font-family: 'Segoe UI', sans-serif;
}

body {
  margin: 0;
  background: linear-gradient(180deg, #ffdde1, #ee9ca7);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.phone {
  width: 100%;
  max-width: 390px;
  aspect-ratio: 9 / 16;
  background: #fff;
  border-radius: 25px;
  padding: 20px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.2);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow: hidden;
}

h1 {
  text-align: center;
  color: #ff4d6d;
  margin-bottom: 10px;
}

#text {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-size: 18px;
  color: #333;
  padding: 10px;
}

img {
  width: 100%;
  border-radius: 15px;
  margin-top: 10px;
}

button {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 12px;
  font-size: 16px;
  margin-top: 10px;
  cursor: pointer;
}

#next {
  background: #ff4d6d;
  color: white;
}

#no {
  background: #eee;
  color: #999;
  cursor: not-allowed;
}

#dm {
  background: #833ab4;
  color: white;
  display: none;
}

.love {
  font-size: 22px;
}
</style>
</head>

<body>

<audio autoplay loop>
  <source src="https://www.bensound.com/bensound-music/bensound-love.mp3">
</audio>

<div class="phone">
  <div>
    <h1>El & Eli 💕</h1>
    <div id="text"></div>
    <img id="photo" style="display:none;"
      src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Seventeen_2022.jpg"
      alt="Wonwoo & Jeonghan">
  </div>

  <div>
    <button id="next">Next 💗</button>
    <button id="no">NO ❌</button>
    <button id="dm" onclick="goDM()">DM Me 💌</button>
  </div>
</div>

<script>
const texts = [
  "Hey El… 💗",
  "I don’t know how to say this properly, but you make my days softer.",
  "Kadang aku capek sama dunia, tapi kamu tuh… safe place.",
  "Talking to you feels like listening to my favorite song on repeat.",
  "You’re sweet without trying, and that’s dangerous 😌",
  "Kalau kamu Wonwoo, aku rela jadi lagu mellow-nya.",
  "Atau kalau kamu Jeonghan, aku tetap jatuh tiap senyum kamu 😭💘",
  "I like you. Not loudly. But honestly.",
  "So… can I stay? 🌷"
];

let index = 0;
const textEl = document.getElementById("text");
const photo = document.getElementById("photo");
const nextBtn = document.getElementById("next");
const dmBtn = document.getElementById("dm");

textEl.innerHTML = texts[0];

nextBtn.onclick = () => {
  index++;
  if (index < texts.length) {
    textEl.innerHTML = texts[index];
    if (index === 5) {
      photo.style.display = "block";
    }
  } else {
    nextBtn.style.display = "none";
    dmBtn.style.display = "block";
    textEl.innerHTML = "<div class='love'>💗💗💗💗💗💗💗<br>I hope this made you smile.</div>";
  }
};

function goDM() {
  window.location.href = "https://instagram.com/drugstprn";
}
</script>

</body>
</html>

