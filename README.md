<!DOCTYPE html><html lang="en">
<head>
  <script type='text/javascript' src='//pl26698582.profitableratecpm.com/f4/6c/05/f46c05f4b2c7a00bb2020d91aba423be.js'></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animal Small World</title>
  <!-- Google AdSense: Insert your Publisher and replace with your Publisher ID -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js" data-ad-client="<ca-app-pub-9412205900221307~1031540280_></ca-app-pub-9412205900221307~1031540280"></script>"
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@700&display=swap');
    :root {
      --bg-color: #fffae6;
      --container-bg: #fff8dc;
      --outline-color: #333;
      --transition: 0.3s ease;
      --success: #4caf50;
      --error: #f44336;
      --hint: #FFD700;
      --btn-bg1: #ff9a9e;
      --btn-bg2: #fad0c4;
      --letter-size: 44px;
      --btn-font: 'Comic Neue', cursive;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html, body { width: 100%; height: 100%; overflow: hidden; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: repeating-conic-gradient(#ffe4e1 0deg 30deg, #fffae6 30deg 60deg);
      position: relative;
    }
    #game {
      position: absolute;
      top: 50%; left: 50%; transform: translate(-50%, -50%);
      width: 90vw; max-width: 380px;
      background: var(--container-bg);
      border: 6px dashed var(--outline-color);
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 8px 0 var(--outline-color), 0 16px 20px rgba(0,0,0,0.1);
      text-align: center;
    }
    /* Ad slot styling (optional) */
    .ad-slot {
      margin: 12px auto;
      text-align: center;
    }
    h1 {
      font-family: var(--btn-font);
      font-size: 2rem;
      color: #ff6f61;
      text-shadow: 2px 2px var(--outline-color);
      margin-bottom: 12px;
    }
    #controls {
      display: flex; justify-content: center; align-items: center;
      margin-bottom: 8px;
      gap: 8px;
    }
    #levelLabel,
    #difficultyLabel {
      font-family: var(--btn-font);
      color: #333;
    }
    .round-btn {
      width: 36px; height: 36px;
      background: linear-gradient(45deg, var(--btn-bg1), var(--btn-bg2));
      border: 3px solid var(--outline-color);
      border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      cursor: pointer;
      box-shadow: 0 4px 0 var(--outline-color);
      transition: transform var(--transition), box-shadow var(--transition);
      font-size: 1.2rem;
    }
    .round-btn:active {
      transform: translateY(2px);
      box-shadow: 0 2px 0 var(--outline-color);
    }
    #images { margin: 12px 0; }
    .img-card {
      width: 100%; max-width: 300px;
      margin: 0 auto 12px;
      border: 4px solid var(--outline-color);
      border-radius: 12px;
      overflow: hidden;
      background: #fff;
      box-shadow: inset 0 0 0 4px var(--outline-color);
    }
    .img-card img {
      width: 100%; display: block;
      opacity: 0; transition: opacity 0.4s ease;
    }
    .img-card img.loaded { opacity: 1; }
    input {
      width: 70%; max-width: 250px;
      padding: 10px; margin: 0 auto 12px;
      border: 4px solid var(--outline-color);
      border-radius: 30px;
      font-size: 1rem;
      font-family: var(--btn-font);
      text-align: center;
      transition: border-color var(--transition);
    }
    input:focus { border-color: #ff6f61; outline: none; }
    #letters {
      display: flex; flex-wrap: wrap; justify-content: center;
      margin-bottom: 12px;
    }
    .letter {
      width: var(--letter-size); height: var(--letter-size);
      margin: 4px;
      display: flex; align-items: center; justify-content: center;
      background: #ffd700;
      font-family: var(--btn-font);
      font-size: 1.2rem;
      color: var(--outline-color);
      border: 3px solid var(--outline-color);
      border-radius: 50%;
      cursor: pointer;
      transition: transform var(--transition), background var(--transition);
      box-shadow: 0 4px 0 var(--outline-color);
    }
    .letter:hover { transform: scale(1.2) translateY(-2px); background: #ffdd57; }
    .button {
      margin: 6px 4px; padding: 8px 20px;
      font-family: var(--btn-font); font-size: 1rem;
      color: var(--outline-color);
      background: linear-gradient(45deg, var(--btn-bg1), var(--btn-bg2));
      border: 4px solid var(--outline-color);
      border-radius: 40px;
      cursor: pointer;
      box-shadow: 0 6px 0 var(--outline-color);
      transition: transform var(--transition), box-shadow var(--transition);
    }
    .button:hover { transform: translateY(-3px); box-shadow: 0 9px 0 var(--outline-color); }
    .button:active { transform: translateY(1px); box-shadow: 0 4px 0 var(--outline-color); }
    #popup {
      position: fixed; top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(255,255,255,0.8);
      display: flex; align-items: center; justify-content: center;
      opacity: 0; pointer-events: none; transition: opacity var(--transition);
      z-index: 10;
    }
    #popup.show { opacity: 1; pointer-events: auto; }
    .popup-content {
      background: #fff;
      border: 4px solid var(--outline-color);
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      box-shadow: 0 6px 0 var(--outline-color);
    }
    #popupIcon { font-size: 3rem; margin-bottom: 8px; color: var(--outline-color); }
    #popupMessage { font-family: var(--btn-font); font-size: 1.2rem; }
  </style>
</head>
<body>
  <!-- Top Ad Slot -->
  <div class="ad-slot">
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="ca-pub-REPLACE_WITH_YOUR_PUBLISHER_ID"
         data-ad-slot="ca-app-pub-9412205900221307~1031540280"
         data-ad-format="auto"
         data-full-width-responsive="true"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>  <div id="game">
    <h1>Animal Small World</h1>
    <!-- Inline Ad Slot -->
    <div class="ad-slot">
      <ins class="adsbygoogle"
           style="display:inline-block;width:320px;height:100px"
           data-ad-client="ca-pub-REPLACE_WITH_YOUR_PUBLISHER_ID"
           data-ad-slot="ca-app-pub-9412205900221307~1031540280"></ins>
      <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
    </div><div id="controls">
  <div id="levelLabel"></div>
  <button id="musicToggleBtn" class="round-btn">🔊</button>
  <div id="difficultyLabel"></div>
</div>
<div id="images"></div>
<input id="guessInput" type="text" placeholder="Type the animal name…">
<div id="letters"></div>
<button class="button" onclick="submitWord()">Guess!</button>
<button class="button" onclick="clearWord()">Clear</button>
<button class="button" onclick="showHint()">Hint</button>

  </div>  <!-- Bottom Ad Slot -->  <div class="ad-slot">
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="ca-pub-REPLACE_WITH_YOUR_PUBLISHER_ID"
         data-ad-slot="ca-app-pub-9412205900221307~1031540280"
         data-ad-format="rectangle"
         data-full-width-responsive="false"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div><audio id="bgMusic" src="/background music/Guess the animal.mp3" preload="auto" loop autoplay></audio>

  <div id="popup">
    <div class="popup-content">
      <span id="popupIcon">✔</span>
      <p id="popupMessage">Message</p>
    </div>
  </div>
  <script>
    // Existing JS logic remains unchanged
    const guessInput = document.getElementById('guessInput');
    const imagesDiv = document.getElementById('images');
    const levelLabel = document.getElementById('levelLabel');
    const difficultyLabel = document.getElementById('difficultyLabel');
    const lettersDiv = document.getElementById('letters');
    const popup = document.getElementById('popup');
    const popupIcon = document.getElementById('popupIcon');
    const popupMsg = document.getElementById('popupMessage');
    const bgMusic = document.getElementById('bgMusic');
    const musicToggleBtn = document.getElementById('musicToggleBtn');
    let musicPlaying = true;
    const colors = ['#FF6B6B','#6BCB77','#4D96FF','#FFD93D','#EA5455','#FF7E6D','#3D84A8','#F18F01',
                    '#9C89B8','#557A95','#F6416C','#FFADAD','#9BF6FF','#BDB2FF','#FFC6FF','#A0C4FF',
                    '#FDFFB6','#CAFFBF','#B28DFF','#FFCB77','#FFE066','#9E2A63','#6D597A','#6B705C',
                    '#CB997E','#FF7F50'];
    const easyAnimals = ['Dog','Cat','Cow','Pig','Lion','Tiger','Elephant','Bear','Horse','Fish'];
    const allAnimals = ['Aardvark','Albatross','Alligator','Alpaca','Ant','Anteater','Antelope','Ape','Armadillo','Baboon',
                        'Badger','Barracuda','Bat','Beaver','Bee','Bison','Boar','Buffalo','Butterfly','Camel',
                        'Capybara','Caribou','Cassowary','Caterpillar','Cattle','Chameleon','Chimpanzee','Chipmunk',
                        'Cobra','Cockroach','Cod','Coyote','Crab','Crane','Crocodile','Crow','Deer','Dinosaur',
                        'Dolphin','Donkey','Dove','Dragonfly','Duck','Eagle','Echidna','Eel','Elk','Emu',
                        'Falcon','Ferret','Finch','Flamingo','Fox','Frog','Gazelle','Gerbil','Giraffe','Goat',
                        'Goldfish','Goose','Gorilla','Grasshopper','Guinea Pig','Hamster','Hare','Hawk','Hedgehog','Heron',
                        'Hippopotamus','Hummingbird','Hyena','Iguana','Impala','Jackal','Jaguar','Jellyfish','Kangaroo','Koala',
                        'Komodo Dragon','Lemur','Leopard','Llama','Lobster','Mole','Monkey','Moose','Moth','Narwhal',
                        'Newt','Octopus','Ostrich','Otter','Owl'];
    const animals = [...easyAnimals, ...allAnimals.slice(0, 90)];
    let currentIndex = 0;
    function getDifficulty(i) {
      if (i < easyAnimals.length) return 'Easy';
      if (i < easyAnimals.length + 30) return 'Medium';
      return 'Hard';
    }
    document.addEventListener('DOMContentLoaded', () => { renderAlphabet(); loadAnimal(currentIndex); });
    musicToggleBtn.addEventListener('click', () => {
      if (musicPlaying) { bgMusic.pause(); musicToggleBtn.textContent = '🔇'; }
      else { bgMusic.play(); musicToggleBtn.textContent = '🔊'; }
      musicPlaying = !musicPlaying;
    });
    async function loadAnimal(idx) {
      guessInput.value = ''; imagesDiv.innerHTML = '';
      levelLabel.textContent = `Level ${idx+1} of ${animals.length}`;
      difficultyLabel.textContent = `${getDifficulty(idx)} Level`;
      const card = document.createElement('div'); card.className = 'img-card';
      const img = document.createElement('img'); img.alt = animals[idx];
      try {
        const res = await fetch(`https://en.wikipedia.org/api/rest_v1/page/summary/${encodeURIComponent(animals[idx])}`);
        const data = await res.json();
        img.src = data.thumbnail?.source || `https://loremflickr.com/400/300/${encodeURIComponent(animals[idx])}?lock=${idx}`;
      } catch {
        img.src = `https://loremflickr.com/400/300/${encodeURIComponent(animals[idx])}?lock=${idx}`;
      }
      img.onload = () => img.classList.add('loaded');
      img.onerror = () => { img.src = `https://via.placeholder.com/400x300?text=${encodeURIComponent(animals[idx])}`; };
      card.appendChild(img); imagesDiv.appendChild(card);
    }
    function renderAlphabet() { lettersDiv.innerHTML = ''; for (let i = 0; i < 26; i++) { const letter = String.fromCharCode(65+i);
      const btn = document.createElement('span'); btn.className = 'letter'; btn.textContent = letter;
      btn.style.background = colors[i % colors.length]; btn.onclick = () => { guessInput.value += letter; };
      lettersDiv.appendChild(btn); } }
    function submitWord() { const guess = guessInput.value.trim().toUpperCase();
      const target = animals[currentIndex].toUpperCase().replace(/[^A-Z]/g,'');
      showPopup(guess===target, guess===target?'✔ Correct!':'✕ Wrong!'); }
    function clearWord() { guessInput.value = ''; }
    function showHint() { popupIcon.textContent='💡'; popupIcon.style.color='var(--hint)'; popupMsg.textContent=`Answer: ${animals[currentIndex]}`;
      popup.classList.add('show'); setTimeout(() => popup.classList.remove('show'),2500); }
    function showPopup(ok,msg) {
      popupIcon.textContent = ok?'✔':'✕'; popupIcon.style.color = ok?'var(--success)':'var(--error)'; popupMsg.textContent = msg;
      popup.classList.add('show'); setTimeout(() => { popup.classList.remove('show'); if(ok){ currentIndex = (currentIndex+1)%animals.length; loadAnimal(currentIndex);} },1200);
    }
  </script>
</body>
</html>
