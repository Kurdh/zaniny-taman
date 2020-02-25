# Zaniny-taman
Tamanm chanda
<h1>Test</h1>
<h5>test</h5>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css" integrity="sha384-UHRtZLI+pbxtHCWp1t77Bi1L4ZtiqrqD80Kn4Z8NTSRyMA2Fd33n5dQ8lWUE00s/" crossorigin="anonymous">
  <link href="https://fonts.googleapis.com/css?family=Raleway&display=swap" rel="stylesheet">
  <title>Document</title>
<style>
* {
  box-sizing: border-box;
}
body {
  font-family: Raleway, arial;
  background: whitesmoke;
}
#container {
  width: 330px;
  padding: 20px 10px;
  margin: auto;
  margin-top: 50px
;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2),
  0 6px 20px 0 rgba(0, 0, 0, 0.19);
  background: white;
  margin-bottom: 50px;
  border-radius: 10px 20px 10px 20px;
}
input, select {
  width: 80px;
  padding: 8px;
  outline: none;
  border:none ;
  border-bottom: 1px solid;
}
select {
    background: white;
}
#butt {
  padding: 8px 12px;
  font-size: 15px;
  color: white;
  background: #3b5998;
  border: none;
  font-weight: bold;
  outline: none;
  border-radius: 5px;
  font-family: Raleway;
}
#butt:hover {
    background: mediumseagreen;
}
/*Made by Noor*/
#error {
  font-weight: bold;
  color: red;
}
span {
  color: #3b5998;
  font-weight: bold;
  font-size: 18px;
}
#result {
  line-height: 1.5;
  padding: 20px;
  background: #b3ff99;
  border-left: 6px solid #79ff4d;
}
#me {
  color: grey;
}
input:focus {
    border-bottom: 3px solid #3b5998;
    outline: none;
}
</style>
<script>
//Made by Noor alam
alert("According to your comments, I tried to solve some issues in this programme. I hope now it'll work properly. If you still found something wrong, I'm waiting for your comments. Thanks for checking out my code ;)");
function calculate() {
  var bDay, bMonth, bYear, cDay, cMonth, cYear, day, month, year, inMonths, inDays, inHours, inMinutes, inSeconds, a, b;
  //get Dob value
  bDay = Number(document.getElementById("birth-day").value);
  bMonth = Number(document.getElementById("birth-month").value);
  bYear = Number(document.getElementById("birth-year").value);
  // get Date value
  cDay = Number(document.getElementById("current-day").value);
  cMonth = Number(document.getElementById("current-month").value);
  cYear = Number(document.getElementById("current-year").value);
  //calculating year
  if(cYear > bYear) {
    year = cYear - bYear;
    document.getElementById("birth-year").style.borderBottom = "1px solid"; document.getElementById("error").innerHTML = ""; document.getElementById("result").style.display="block";
  }else if(cYear == bYear ) {
      year = 0;
  }
  //calculating months
  if(cMonth < bMonth) {
    cMonth += 12;
    year -= 1;
    month = cMonth - bMonth;
  }else {
    month = cMonth - bMonth;
  }
  //calculating days
  if(cDay < bDay) {
    cDay += 31;
    month -= 1;
    day = cDay - bDay;
  }else {
    day = cDay - bDay;
  }
  //converting into 
  inMonths = year * 12 + month;
  a = year * 365;
  b = month * 30;
  //converting into days
  inDays = a + b + day;
  //converting into hours
  inHours = inDays * 24;
  //converting into minutes
  inMinutes = inHours * 60;
  //converting into seconds
  inSeconds = inMinutes * 60;
  if(bYear > cYear) {
    document.getElementById("birth-year").style.borderBottom = "2px solid red";
    document.getElementById("error").innerHTML = "DOB year is invalid!";
    year = 0
    month = 0;
    day = 0;
    inMonths = 0;
    inDays = 0;
    inHours = 0;
    inSeconds = 0;
    document.getElementById("result").style.display="none";
  }
  if(bDay == "" || bYear == "" || cDay == "") {
    document.getElementById("error").innerHTML = "Empty values are not allowed!";
    document.getElementById("result").style.display="none";
  }
 /*Made by Noor*/ document.getElementById("result").innerHTML = "<b> You are: " + year + " Years " + month + " Months " + day + " Days Old. <br>" +
    inMonths + " Months Old. <br>" +
    inDays + " Days Old. <br>" +
    inHours + " Hours Old. <br>" +
    inSeconds + " Seconds Old. </b>";
}
</script>
</head>
<body>
  <div id="container">
    <span>Your date of birth:  </span><br>
    <input type="number" id="birth-day" min="1" max="31" placeholder="Day">
    <select id="birth-month">
      <option value="1">01 Jan</option>
      <option value="2">02 Feb</option>
      <option value="3">03 Mar</option>
      <option value="4">04 Apr</option>
      <option value="5">05 May</option>
      <option value="6">06 Jun</option>
      <option value="7">07 Jul</option>
      <option value="8">08 Aug</option>
      <option value="9">09 Sep</option>
      <option value="10">10 Oct</option>
      <option value="11">11 Nov</option>
      <option value="12">12 Dec</option>
    </select>
    <input type="number" id="birth-year" placeholder="Year">
    <br>
    <br>
    <span>Date to be calculated:  </span><br>
    <input type="number" id="current-day" min="1" max="31" placeholder="Day">
    <select id="current-month">
      <option value="1">01 Jan</option>
      <option value="2">02 Feb</option>
      <option value="3">03 Mar</option>
      <option value="4">04 Apr</option>
      <option value="5">05 May</option>
      <option value="6">06 Jun</option>
      <option value="7">07 Jul</option>
      <option value="8" selected>08 Aug</option>
      <option value="9">09 Sep</option>
      <option value="10">10 Oct</option>
      <option value="11">11 Nov</option>
      <option value="12">12 Dec</option>
    </select>
    <input type="number" id="current-year" placeholder="Year" value="2019">
    <br>
    <br>
    <!--Made by Noor-->
    <button id="butt" onclick="calculate()">Calculate <i class="fas fa-caret-right"></i></button>
    <hr>
    <p id="result"></p>
    <p id="error"></p>
    <hr>
    <p id="me">
      Made By: Noor Alam
    </p>
  </div>
</body>
</html>
