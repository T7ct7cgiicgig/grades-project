# grades-project
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نظام الدرجات</title>
<style>
  body {font-family: Arial; background: #f2f2f2; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0;}
  .box {background: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.2); width: 350px; text-align: center;}
  input, button {width: 100%; padding: 10px; margin-top: 10px; border-radius: 5px; border: 1px solid #ccc; box-sizing: border-box;}
  button {background: #007BFF; color: white; border: none; cursor: pointer;}
  .error {background: red; color: white; padding: 5px; border-radius: 5px; margin-top: 5px; display: none;}
  #grades {display: none; margin-top: 20px;}
  table {width: 100%; border-collapse: collapse; margin-top: 10px;}
  th, td {border: 1px solid #ddd; padding: 8px; text-align: center;}
  th {background: #007BFF; color: white;}
</style>
</head>
<body>

<div class="box" id="loginBox">
  <h2>تسجيل الدخول</h2>
  <input type="text" id="name" placeholder="اسم الطالب">
  <input type="text" id="code" placeholder="الكود الجامعي">
  <button onclick="login()">تأكيد</button>
  <div class="error" id="error">الكود أو الاسم غير صحيح</div>
</div>

<div class="box" id="grades">
  <h3>📌 Midterm Exam Grades</h3>
  <p><strong>Student Name:</strong> Mahmoud Ragab Abdelazim Mansour</p>
  <p><strong>Institute:</strong> Sinai Higher Institute for Tourism and Hotels - Ras Sedr</p>
  <p><strong>Grade Level:</strong> Second Year</p>

  <table>
    <tr><th>Subject</th><th>Grade / 10</th></tr>
    <tr><td>Hotel Management</td><td>10</td></tr>
    <tr><td>Tourism Marketing</td><td>10</td></tr>
    <tr><td>Tourism Studies</td><td>9</td></tr>
    <tr><td>Human Resources Management</td><td>10</td></tr>
    <tr><td>Hotel Services</td><td>10</td></tr>
    <tr><td>Hotel Accounting</td><td>9</td></tr>
    <tr><td>Tourism Law</td><td>10</td></tr>
    <tr><td>Tourism English</td><td>10</td></tr>
    <tr><td>Travel Agency Management</td><td>9</td></tr>
    <tr><td>Tourist Consumer Behavior</td><td>10</td></tr>
    <tr><td>Food Safety</td><td>10</td></tr>
    <tr><td>Tourism Statistics</td><td>9</td></tr>
  </table>
</div>

<script>
function login() {
  const name = document.getElementById("name").value.trim();
  const code = document.getElementById("code").value.trim();

  if (name === "محمود رجب عبد العظيم منصور" && code === "175039") {
    document.getElementById("loginBox").style.display = "none";
    document.getElementById("grades").style.display = "block";
  } else {
    document.getElementById("error").style.display = "block";
  }
}
</script>

</body>
</html>
