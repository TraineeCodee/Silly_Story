
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Silly Story Generator</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      padding: 20px;
      background-color: #ced1d4;
    }
    h1 {
      color: #333;
    }
    #story {
      margin: 20px auto;
      padding: 15px;
      width: 80%;
      max-width: 600px;
      background-color: #fffae6;
      border: 2px dashed #e76e35;
      border-radius: 9px;
      font-size: 18px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #ffa500;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #ff8c00;
    }
    input {
      padding: 8px;
      font-size: 16px;
      margin-bottom: 10px;
      width: 200px;
      text-align: center;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <h1>Silly Story Generator</h1>
  <p>Enter a name (optional) and click the button to generate a random silly story!</p>
  <input type="text" id="nameInput" placeholder="Enter a name...">
  <div id="story">Your silly story will appear here!</div>
  <button onclick="generateStory()">Generate Story</button>

  <script>
    const characters = ['a talking banana', 'a sleepy dragon', 'a dancing robot', 'a mischievous cat', 'a clumsy wizard'];
    const actions = ['won a dance competition', 'ate 100 pancakes', 'invented a flying car', 'fell into a mud puddle', 'tried to juggle flamingos'];
    const locations = ['on the moon', 'in a magical forest', 'at the bottom of the ocean', 'inside a volcano', 'at a spooky haunted house'];

    function getRandomElement(arr) {
      return arr[Math.floor(Math.random() * arr.length)];
    }

    function generateStory() {
      const nameInput = document.getElementById("nameInput").value.trim();
      const name = nameInput || "Alex"; // Default name if none is entered
      const character = getRandomElement(characters);
      const action = getRandomElement(actions);
      const location = getRandomElement(locations);
      document.getElementById("story").innerText = `${name} met ${character} who ${action} ${location}!`;
    }
  </script>
</body>
</html>
