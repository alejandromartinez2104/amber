<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Amberly</title>
  <style>
    body {
      background-color: #B2AC88; /* Sage color */
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      flex-direction: column;
      text-align: center;
      padding: 20px;
      box-sizing: border-box;
    }
    h1 {
      font-size: 2rem; /* Smaller for mobile */
      margin-bottom: 20px;
      color: #333;
    }
    p {
      font-size: 1.2rem; /* Smaller for mobile */
      color: #333;
      margin: 20px;
    }
    button {
      padding: 10px 20px;
      font-size: 1rem; /* Smaller for mobile */
      border-radius: 25px;
      border: none;
      background-color: #4CAF50;
      color: white;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background-color: #45a049;
    }
    #noButton {
      position: absolute;
    }
    img {
      max-width: 100%;
      height: auto;
      margin-top: 20px;
      border-radius: 10px;
    }
    .page {
      display: none;
      width: 100%;
      max-width: 400px; /* Limits width for better mobile readability */
    }
    .page.active {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  </style>
</head>
<body>

  <!-- Page 1 -->
  <div id="page1" class="page active">
    <h1>EITHER I MIGHT BE TURNING NOT STRAIGHT OR......</h1>
    <button onclick="goToPage2()">find out the big secret</button>
  </div>

  <!-- Page 2 -->
  <div id="page2" class="page">
    <p>i am falling in love with this cousin of Jerome's. Because i just want to be with her all the time and theres no one that has made me so excited to live the rest of my life with them than her. and from here on out i just want to learn to love her the way she deserves. UNCONDITIONALLY!</p>
    <button onclick="goToPage3()">continue</button>
  </div>

  <!-- Page 3 -->
  <div id="page3" class="page">
    <p>Amberly don't ever leave because i want to tell you I LOVE YOU one day and to no one else</p>
    <button onclick="goToPage4()">continue to request</button>
  </div>

  <!-- Page 4 -->
  <div id="page4" class="page">
    <img src="https://via.placeholder.com/400" alt="Valentine Image">
    <p>WILL YOU BE MY VALENTINE DWEETY?</p>
    <button onclick="goToPage5()">Yes</button>
    <button id="noButton" onmouseover="moveNoButton()" ontouchstart="moveNoButton()">No</button>
  </div>

  <!-- Page 5 -->
  <div id="page5" class="page">
    <p>THANK YOU FOR COMING INTO MY LIFE WHEN I DIDN'T KNOW I NEEDED IT THE MOST!</p>
  </div>

  <script>
    function goToPage2() {
      document.getElementById('page1').classList.remove('active');
      document.getElementById('page2').classList.add('active');
    }

    function goToPage3() {
      document.getElementById('page2').classList.remove('active');
      document.getElementById('page3').classList.add('active');
    }

    function goToPage4() {
      document.getElementById('page3').classList.remove('active');
      document.getElementById('page4').classList.add('active');
    }

    function goToPage5() {
      document.getElementById('page4').classList.remove('active');
      document.getElementById('page5').classList.add('active');
    }

    function moveNoButton() {
      const noButton = document.getElementById('noButton');
      const x = Math.random() * (window.innerWidth - noButton.offsetWidth);
      const y = Math.random() * (window.innerHeight - noButton.offsetHeight);
      noButton.style.left = `${x}px`;
      noButton.style.top = `${y}px`;
    }
  </script>
</body>
</html>
