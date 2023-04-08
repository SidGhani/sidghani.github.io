<!DOCTYPE html>
<html>
<head>
	<title>Data Analytics User Survey</title>
	  <style>
    h1 {
      font-family: "Open Sans", sans-serif;
	  text-align: center;
    }
  </style>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
	<script>
		function submitForm() {
			// get form elements
			const nameInput = document.getElementById("nameInput");
			const deptInput = document.getElementById("deptInput");
			const toolsCheckboxes = document.querySelectorAll('input[name="tools"]:checked');
			const expSelect = document.getElementById("expSelect");
			const emailInput = document.getElementById("emailInput");

			// get input values
			const name = nameInput.value.trim();
			const dept = deptInput.value.trim();
			const tools = Array.from(toolsCheckboxes, el => el.value);
			const exp = expSelect.value;
			const email = emailInput.value.trim();

			// validate inputs
			if (name === "") {
				alert("Please enter your name.");
				return;
			}
			if (dept === "") {
				alert("Please enter your department.");
				return;
			}
			if (tools.length === 0) {
				alert("Please select at least one data tool/language.");
				return;
			}
			if (exp === "") {
				alert("Please select your years of experience with data.");
				return;
			}
			if (email === "") {
				alert("Please enter your email address.");
				return;
			}

			// submit form
			alert(`Thank you, ${name}! Your department is ${dept}. You use ${tools.join(", ")} for data analysis, and you have ${exp} years of experience. We will contact you at ${email} for further feedback.`);
			document.getElementById("surveyForm").reset();
		}
	</script>
</head>
<body>
	<h1>Data Analytics User Survey</h1>
	<form id="surveyForm">
		<label for="nameInput">Name:</label>
		<input type="text" id="nameInput" name="name"><br>

		<label for="deptInput">Department:</label>
		<input type="text" id="deptInput" name="dept"><br>

		<fieldset>
			<legend>What data tools/languages do you use?</legend>
			<input type="checkbox" id="alteryxCheckbox" name="tools" value="Alteryx">
			<label for="alteryxCheckbox">Alteryx</label><br>

			<input type="checkbox" id="tableauCheckbox" name="tools" value="Tableau">
			<label for="tableauCheckbox">Tableau</label><br>

			<input type="checkbox" id="sqlCheckbox" name="tools" value="SQL">
			<label for="sqlCheckbox">SQL</label><br>

			<input type="checkbox" id="pythonCheckbox" name="tools" value="Python">
			<label for="pythonCheckbox">Python</label><br>

			<input type="checkbox" id="excelCheckbox" name="tools" value="Excel">
			<label for="excelCheckbox">Excel</label><br>

			<input type="checkbox" id="powerbiCheckbox" name="tools" value="PowerBI">
			<label for="powerbiCheckbox">PowerBI</label><br>
			
			<input type="checkbox" id="powerbiCheckbox" name="tools" value="PowerBI">
			<label for="powerbiCheckbox">UiPath</label><br>

			<input type="checkbox" id="awsCheckbox" name="tools" value="AWS">
			<label for="awsCheckbox">AWS</label><br>
		</fieldset>


	<label for="experience">How many years experience do you have working in Data?</label>
<select id="experience" name="experience">
  <option value="0">0 years</option>
  <option value="1">1 year</option>
  <option value="2">2 years</option>
  <option value="3">3 years</option>
  <option value="4">4 years</option>
  <option value="5">5 years</option>
  <option value="6">6 years</option>
  <option value="7">7 years</option>
  <option value="8">8 years</option>
  <option value="9">9 years</option>
  <option value="10">10 years or more</option>
</select>

		<br> <!-- Add line break here -->

</fieldset>
			<button type="submit">Submit</button> <!-- submit button added here -->
			
			<footer>
		<p>Thank you for completing this survey, for any questions please contact sidghani@email.com</p>
	</footer>
</form>

	
