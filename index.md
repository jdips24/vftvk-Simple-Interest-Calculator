<!Doctype html>
<html lang="en">
<meta charset="=utf-8">
<title> Simple Interest Calculator </title>
<link rel="stylesheet" href="style.css"/>

<script>
function answer()
{
   p= document.getElementById("p") .value;
   n= document.getElementById("n") .value;
   r= document.getElementById("r") .value;

   var
    Interest=(p*r*n)/100;
    var total=parseInt(Interest)+ parseInt(p);
     console.log(total)
	 
  Entered_amount= document.getElementById("Entered_amount");
  Entered_amount.innerHTML = p
  Entered_interest= document.getElementById("Entered_interest");
  Entered_interest.innerHTML = r + "%"
  Calculated_Amount= document.getElementById("Calculated_Amount");
  Calculated_Amount.innerHTML = total
  
  }
  function slidervalue()
  {
  var slider = document.getElementById("myRange");
  var output = document.getElementById("demo");
    output.innerHTML = slider.value; 

  } 
</script>

<body>
    
    <div class="calculator">
    <h1> Simple Interest Calculator</h1>
    <br>
    <label for = "Amount"> Amount: </label>
    <input id="p">
    <br> </br>
    <label for = "Interest">Interest Rate: </label>
    <input type="range" id = "r" min="1" max="100" value="20" class="slider" id="myRange" oninput="slidervalue()"> 
    <br> </br>
    <label for="time"> No. of Year: </label> 
    <input id="n" type="number" min='1' max='10' value='0' placeholder="Enter No. of Year" >
    <br> </br>
    <button onclick="answer()">Compute Interest</button>
    <table>
        <tr>
            <td>If you deposit USD : </td>
            <td><p id="Entered_amount"></p></td>
        </tr>
		<tr>
            <td>At an Interest rate of :  </td>
            <td> <p id="Entered_interest"> </p></td>
        </tr>
        <tr>
            <td>You will receive an Amount of : </td>
            <td> <p id="Calculated_Amount"></p></td>
        </tr>
        		
    </table>
	<br>
       <p> &copy;Everyone Can Get Rich </p>
</div>

</body>
</html>

