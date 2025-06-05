# my-website
Personal Grade System[Uploading index.html…]()<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>個人成績系統</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f3e9e5;
      color: #5c3d2e;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
    }

    header {
      background-color: #d9c5b2;
      width: 100%;
      padding: 20px 0;
      text-align: center;
      font-size: 2em;
      font-weight: bold;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    main {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    form {
      background-color: #ffffff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      width: 100%;
      max-width: 400px;
      display: flex;
      flex-direction: column;
    }

    input, button {
      margin: 10px 0;
      padding: 10px;
      font-size: 1em;
      border: 1px solid #d9c5b2;
      border-radius: 8px;
    }

    button {
      background-color: #d9c5b2;
      color: #fff;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #bfa288;
    }

    .result {
      margin-top: 20px;
      font-size: 1.2em;
    }

    footer {
      text-align: center;
      padding: 10px 0;
      background-color: #d9c5b2;
      width: 100%;
      font-size: 0.9em;
    }
  </style>
</head>
<body>

<header>
  個人成績輸入系統
</header>

<main>
  <form id="gradeForm">
    <label for="subject">科目名稱</label>
    <input type="text" id="subject" name="subject" placeholder="例如：數學" required>

    <label for="grade">成績</label>
    <input type="number" id="grade" name="grade" placeholder="0 - 100" min="0" max="100" required>

    <button type="submit">送出成績</button>
  </form>

  <div class="result" id="result"></div>
</main>

<footer>
  &copy; 2025 個人成績系統
</footer>

<script>
  const form = document.getElementById('gradeForm');
  const result = document.getElementById('result');

  form.addEventListener('submit', function(event) {
    event.preventDefault();

    const subject = form.subject.value.trim();
    const grade = form.grade.value;

    if (subject && grade) {
      result.innerHTML = `科目：<strong>${subject}</strong>，成績：<strong>${grade}</strong> 分`;
      form.reset();
    }
  });
</script>

</body>
</html>


