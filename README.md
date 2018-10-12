<!DOCTYPE HTML>
<html>
<head>
<title></title>

 
<script type="text/javascript">

// shane viola ite154 web programming project 1

changeShow() {

	var show = parseInt( document.getElementById("show").value );
	document.getElementById("output") = show;
}

vipmemb() {

	if parseInt( document.getElementById("vipmem").checked == true ) {
	
		vipmem = 10
	}
	else {
	
		vipmem = 0
	}
		
		


purchaseTix() {

	var numtix = parseInt( document.getElementById("numtix").value );
	
	
	// calculate
	var total = (show * numtix) - vipmem;
	
	// construct output
	var msg = "<div>Results of your order</div>
	msg = "<div>Selected event: " + show + "</div>
	
	



</script>

<style type="text/css">

body {
	background-color: #F3EFE0;
	font-family: arial;
	color: #217C7E;
}

#contentwrap {
	border: 8px #9A3334 solid;
	padding: 20px;
	width: 600px;
	margin: 20px auto 0px auto;
	border-radius: 25px;
	background: white;
	background-image: url("http://newton.ncc.edu/gansonj/ite254/img/wonderpets.png");
	background-repeat: no-repeat;
	background-position: right 40%;
}

#heading {
	font-size: 2.2em;
	border-bottom: 6px #217C7E double;
	padding: 10px 0px 10px 0px;
	color: darkred;
	text-align: center;
}

#formdiv {

	padding-top: 25px;
}

.formtext {
	font-size: 1em;
	margin-top: 20px;
}

.formfield {
	border: 2px darkred solid;
	background: lightyellow;
	color: darkred;
	font-size: 1.1em;
	padding: 2px;
}

#orderbutton {
	border: 2px purple solid;
	background-color: lightyellow;
	font-size: 1.25em;
	border-radius: 25px;
}

</style>

</head>
<body>

<div id="contentwrap">

	<div id="heading">Online Event Order Form</div>
	
	<div id="formdiv">
		
		<form>
	
			<div class="formtext">Choose a show</div>
			<select class="formfield" style="width:280px;" id="show" onchange="changeShow()">
				<option value="s">Sesame Street Live ( $29.99 )</option>
				<option value="w">The Wiggles Live ( $35.49 )</option>
				<option value="d">Dora Live in Concert ( $49.95 )</option>
			</select>
			
			<div class="formtext">Enter number of tickets (4 max)</div>
			<input type="text" class="formfield" id="numtix">
			
			<div class="formtext">Are you a VIP member</div>
			<input type="checkbox" id="vipmem" onchange="vipmemb()"/> Yes I am ($10.00 discount on total order)
		
			<div style="margin-top:10px;">
				<input type="button" value="Order Tickets" id="orderbutton" onClick="purchaseTix()">
			</div>
		
		</form>
			
		<div id="output"></div>
	
	</div> <!-- ends div#formdiv -->
		
</div> <!-- ends div#contentwrap -->

</body>
</html>
