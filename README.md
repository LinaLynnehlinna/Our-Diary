<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Gantuangko & Clerigo - 12 SFCG</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive, sans-serif;
      margin: 0;
      padding: 20px;
      background: linear-gradient(to bottom right, #ffe4e1, #fff0f5);
    }
    h1 {
      text-align: center;
      color: #ff69b4;
      font-size: 2.5em;
      text-shadow: 2px 2px #ffc0cb;
    }
    .entry-box {
      background: #fff;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(255, 182, 193, 0.5);
      border: 2px solid #ffb6c1;
      transition: transform 0.2s ease;
    }
    .entry-box:hover {
      transform: scale(1.02);
    }
    label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
      color: #ff69b4;
    }
    input[type="date"], textarea {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      border: 2px solid #ffb6c1;
      border-radius: 10px;
      background-color: #fffafc;
      font-family: inherit;
    }
    textarea {
      height: 100px;
    }
    textarea:focus, input[type="date"]:focus {
      outline: none;
      border-color: #ff69b4;
      box-shadow: 0 0 5px #ff69b4;
    }
    .save-btn {
      display: block;
      margin: 20px auto;
      padding: 10px 20px;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 20px;
      font-size: 1.2em;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(255, 182, 193, 0.5);
      transition: background-color 0.3s;
    }
    .save-btn:hover {
      background-color: #ff1493;
    }
  </style>
</head>
<body>
  <h1>My Diary</h1>

  <div class="entry-box">
    <label for="date1">Date</label>
    <input type="date" id="date1">
    <label for="entry1">Entry</label>
    <textarea id="entry1" placeholder="Write your thoughts..."></textarea>
  </div>

  <div class="entry-box">
    <label for="date2">Date</label>
    <input type="date" id="date2">
    <label for="entry2">Entry</label>
    <textarea id="entry2" placeholder="Write your thoughts..."></textarea>
  </div>

  <div class="entry-box">
    <label for="date3">Date</label>
    <input type="date" id="date3">
    <label for="entry3">Entry</label>
    <textarea id="entry3" placeholder="Write your thoughts..."></textarea>
  </div>

  <div class="entry-box">
    <label for="date4">Date</label>
    <input type="date" id="date4">
    <label for="entry4">Entry</label>
    <textarea id="entry4" placeholder="Write your thoughts..."></textarea>
  </div>

  <div class="entry-box">
    <label for="date5">Date</label>
    <input type="date" id="date5">
    <label for="entry5">Entry</label>
    <textarea id="entry5" placeholder="Write your thoughts..."></textarea>
  </div>

  <button class="save-btn" onclick="saveEntries()">💾 Save My Diary</button>

  <script>
    // Load saved entries from localStorage
    window.onload = function() {
      for (let i = 1; i <= 5; i++) {
        document.getElementById('date' + i).value = localStorage.getItem('date' + i) || '';
        document.getElementById('entry' + i).value = localStorage.getItem('entry' + i) || '';
      }
    };

    // Save entries to localStorage
    function saveEntries() {
      for (let i = 1; i <= 5; i++) {
        localStorage.setItem('date' + i, document.getElementById('date' + i).value);
        localStorage.setItem('entry' + i, document.getElementById('entry' + i).value);
      }
      alert("✅ Your diary has been saved!");
    }
  </script>
</body>
</html>
