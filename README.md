# FrontendBlitz
## CGPA CALCULATOR

### In home.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CGPA/GPA Calculator</title>
    <!--Link css file - style.css-->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
</head>
<body>
    <div class="home-page">
        <div class="home-title">
            <h1>CGPA/GPA CALCULATOR</h1>
        </div>

        <div class="home-buttons">
            <!-- Create buttons with images to link gpa.html and cgpa.html -->
            <!-- Write your code here -->

        </div>
    </div>
</body>
```
### In style.css
```

.home-page {
    width: 100%;
    height: 500px;
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
}

.home-title {
    margin-top: 30px;
    display: flex;
    justify-content: center;
}

.home-buttons {
    display: flex;
    justify-content: space-around;
}

.home-button {
    width: 30%;
    height: fit-content;
    margin-top: 30px;
}

#icon {
    width: 100%;
}
```
### In gpa.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GPA CALCULATOR</title>
    <!-- Link css page - stylegpa.css -->

</head>
<body>
    <div class="content-box">
        <div class="title-box">
            <h2 id="title">GPA CALCULATOR</h2>
        </div>
        <div class="input-fields">
            <div class="credit-field">
                <h5 class="input-text">Credit for Subject 1</h5>
                <!--Get inputs for credit using input tag-->
            </div>
            <div class="credit-field">
                <h5 class="input-text">Grade Point</h5>
                <!--Get inputs for grade using input tag-->
            </div>
        </div>
        <div class="button-div">
            <!-- Create button tag with class buttons to "Add Entry"-->
        </div>
        <div class="button-div">
            <!-- Create button tag with class buttons to "Calculate"-->
        </div>

    </div>

    <!-- Link javascript code - scriptgpa.js-->
</body>
</html>
```

### In stylegpa.css
```
body {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  font-family: "Poppins", sans-serif;
}

.content-box {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: column;
  /* Adjust border as needed */
  width: 60%;
  margin: 50px;
}

.title-box {
  height: max-content;
  border: 1px solid black;
  width: 100%;
  display: flex;
  /* Center items */
}

.input-fields {
  display: flex;
  /* Ensure items wrap to next row */
  width: 100%;
  /* Center items horizontally */
}

.credit-field {
  width: 40%;
  /* Adjust margin as needed */
}

.credit-field h5,
.credit-field input {
  width: calc(100% - 20px);
  margin-bottom: 10px;
}

.input {
  padding: 10px;
  /*Insert border radius and border attribute as per your need*/
  box-sizing: border-box; 
}

.button-div {
  display: flex;
  justify-content: center;
}

.buttons {
  padding: 15px;
  width: 20%;
  margin: 10px;
}
```

### In scriptgpa.js
```
document.addEventListener('DOMContentLoaded', function() {
    var addButton = document.querySelector('.buttons[type="submit"]');
    var creditCount = 2;
    
    addButton.addEventListener('click', function(event) {
        event.preventDefault();
        
        var inputFields = document.querySelector('.input-fields');
        inputFields.appendChild(createInputField('Credit for Subject ' + creditCount++, 'Enter credit for subject'));
        inputFields.appendChild(createInputField('Grade Point', 'Enter grade for subject'));
    });
    
    function createInputField(labelText, placeholderText) {
        var field = document.createElement('div');
        field.className = 'credit-field';
        
        var text = document.createElement('h5');
        text.className = 'input-text';
        text.textContent = labelText;
        
        var input = document.createElement('input');
        input.className = 'input';
        input.type = 'number';
        input.placeholder = placeholderText;
        
        field.appendChild(text);
        field.appendChild(input);
        
        return field;
    }
});
```

### In cgpa.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GPA CALCULATOR</title>
    <!-- Link css file stylecgpa.css-->

</head>
<body>
    <div class="content-box">
        <div class="title-box">
            <h2 id="title">CGPA CALCULATOR</h2>
        </div>
        <div class="input-fields">
            <div class="gpa-field">
                <h5 class="input-text">GPA - Semester 1</h5>
                <!--Get inputs for gpa using input tag-->
            </div>



    
        </div>
        <div class="button-div">
            <!-- Create button tag with class buttons to "Add Entry"-->
        </div>
        <div class="button-div">
            <!-- Create button tag with class buttons to "Calculate"-->
        </div>

    </div>

     <!-- Link javascript code - scriptcgpa.js-->
</body>
</html>

```

### In stylecgpa.css
```
body {
  margin: 0;
  padding: 0;
  display: flex;
  /*Align contents in center*/
  font-family: "Poppins", sans-serif;

}

.content-box {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: column;
  /* Add border size and border color */
  width: 60%;
  margin: 50px;
}

.title-box {
  height: max-content;
  border: 1px solid black;
  width: 100%;
  display: flex;
  justify-content: center;
}

.input-fields {
  display: flex;
  /*Wrap contents*/
  width: 100%;
  /* Center items horizontally */
}

.gpa-field {
  width: 40%;
  /* Adjust margin as needed */
}

.gpa-field h5,
.gpa-field input {
  width: calc(100% - 20px);
  /* Adjust margin as needed */
}

.input {
  padding: 10px;
  border-radius: 20px;
  border: 1px solid black;
  box-sizing: border-box; 

.button-div {
  display: flex;
  justify-content: center;
}

.buttons {
  padding: 15px;
  width: 20%;
  margin: 10px;
}

.home-page {
  width: 100%;
  height: 500px;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
}

.home-title {
  margin-top: 30px;
  display: flex;
  /*Align contents in the center*/
}

.home-buttons {
  display: flex;
  justify-content: space-around;
}

.home-button {
  width: 30%;
  height: fit-content;
  margin-top: 30px;
}

#icon {
  width: 100%;
}
```
### In scriptcgpa.js
```
document.addEventListener('DOMContentLoaded', function() {
    var addButton = document.querySelector('.buttons[type="submit"]');
    var gpaCount = 2;
    
    addButton.addEventListener('click', function(event) {
        event.preventDefault();
        
        var inputFields = document.querySelector('.input-fields');
        /* Create input field */
    });
    
    function createInputField(labelText, placeholderText) {
        var field = document.createElement('div');
        field.className = 'gpa-field';
        
        var text = document.createElement('h5');
        text.className = 'input-text';
        text.textContent = labelText;
        
        var input = document.createElement('input');
        input.className = 'input';
        input.type = 'number';
        input.placeholder = placeholderText;
        
        field.appendChild(text);
        field.appendChild(input);
        
        return field;
    }
});
```
#### Developed by
```
Manoj M V - 212222220023
Harsayazheni P Y - 212222040052 
```
