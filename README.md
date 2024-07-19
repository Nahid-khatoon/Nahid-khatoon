<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSE TIME TABLE-4th SEM</title>
  <style>
    table {
      width: 100%;
      border-collapse: collapse;
    }
    th, td {
      border: 1px solid #dddddd; 
      text-align: left;
      padding: 8px;
    }
    th {
      background-color: #f2f2f2;
    }
  </style>
</head>
<body BGCOLOR="#26CBDA">
<FONT COLOR="RED">
<h3>CSE TIME TABLE - 4th SEM</h3>
</FONT>
<table>
  <!-- Your table content here -->
</table>

<BR><BR>
<center>
<button type="button" onclick="checkMicroprocessorClass()">UPDATE</button>
<p id="message"></p>
<p id="time"></p>
</center>

<script>
function checkMicroprocessorClass() {
  var today = new Date();
  var day = today.getDay(); // Get the current day (0-6 where 0 is Sunday)
  var currentTime = today.getHours();

  if ((day === 1 && currentTime >= 9 && currentTime < 11) || (day === 2 && currentTime >= 9 && currentTime < 11) || (day === 4 && currentTime >= 10 && currentTime < 12)) {
    document.getElementById("message").innerText = "Microprocessor class is scheduled for this time slot.";
  } else {
    document.getElementById("message").innerText = "Microprocessor class is not scheduled for this time slot.";
  }

  var time = today.toLocaleTimeString(); // Get the current time
  document.getElementById("time").innerText = "Current Time: " + time;
}
</script>

</body>
</html>