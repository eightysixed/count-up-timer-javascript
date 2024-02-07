<html>
<body style="background-color:#E3EBF8;">

<head>
  <title>Count Up Timer</title>
  <!-- Make the webpage responsive -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<!-- All of this can be easily customized to the user's liking -->
<style>
.countUp {
  font-family: "Papyrus", "Verdana", monospace;
  text-align: center;
  margin-bottom: 20px;
}
.countUp .timeElapsed {
  display: inline-block;
  padding: 10px;
  background: #151515;
  margin: 0;
  color: white;
  min-width: 2.6rem;
  margin-left: 13px;
  border-radius: 10px 0 0 10px;
  font-size: 30px;
  font-family: "Papyrus", "Verdana", monospace;
}
.countUp span[class*="timeRef"] {
  border-radius: 0 10px 10px 0;
  margin-left: 0;
  background: #e8c152;
  color: black;
  font-family: "Papyrus", "Verdana", monospace;
  font-size: 30px;
}
.header {
  font-family: "Papyrus", "Verdana", monospace;
  font-weight: bold;
  text-align: center;
  font-size: 30px;
}
.footer {
  text-align: center;
  font-family: "Papyrus", "Verdana", monospace;
  font-weight: bold;
  font-size: 30px;
}
</style>

<div class="header" id=header>
  <span class="header"><p>It's been...</p></span>
</div>

<div class="countUp" id=countUp>
  <span class="timeElapsed years">00</span>
  <span class="timeElapsed timeRefYears">years</span><br><br>
  <span class="timeElapsed days">00</span>
  <span class="timeElapsed timeRefDays">days</span><br><br>
  <span class="timeElapsed hours">00</span>
  <span class="timeElapsed timeRefHours">hours</span><br><br>
  <span class="timeElapsed minutes">00</span>
  <span class="timeElapsed timeRefMinutes">minutes</span><br><br>
  <span class="timeElapsed seconds">00</span>
  <span class="timeElapsed timeRefSeconds">seconds</span>
</div>

<div class="footer" id=footer>
  <span class="footer"></span>
</div>

<!-- The JavaScript Code that makes it all work -->

<script>
 window.onload = function() {
   countUpFromTime("Jan 1, 2000 12:00:00", "countUp");
 };
 function countUpFromTime(countFrom, id) {
   countFrom = new Date(countFrom).getTime();
   var now = new Date(),
       countFrom = new Date(countFrom),
       startTime = new Date(countFrom).toLocaleString(),
       timeDifference = (now - countFrom);

   var secondsPerDay = 60 * 60 * 1000 * 24,
       secondsPerHour = 60 * 60 * 1000;
   days = Math.floor(timeDifference / (secondsPerDay) * 1);
   years = Math.floor(days / 365);
   if (years > 1){ days = days - (years * 365) }
   hours = Math.floor((timeDifference % (secondsPerDay)) / (secondsPerHour) * 1);
   minutes = Math.floor(((timeDifference % (secondsPerDay)) % (secondsPerHour)) / (60 * 1000) * 1);
   seconds = Math.floor((((timeDifference % (secondsPerDay)) % (secondsPerHour)) % (60 * 1000)) / 1000 * 1);

   var idEl = document.getElementById(id);
   idEl.getElementsByClassName("years")[0].innerText = years;
   idEl.getElementsByClassName("days")[0].innerText = days;
   idEl.getElementsByClassName("hours")[0].innerText = hours;
   idEl.getElementsByClassName("minutes")[0].innerText = minutes;
   idEl.getElementsByClassName("seconds")[0].innerText = seconds;

   clearTimeout(countUpFromTime.interval);
   countUpFromTime.interval = setTimeout(function(){ countUpFromTime(countFrom, id); }, 1000);

   footerText = "Since <br>" + startTime;
   document.getElementById("footer").innerHTML = footerText;
 }
</script>

</body>
</html>
