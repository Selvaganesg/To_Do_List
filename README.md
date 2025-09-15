# Ex03 To-Do List using JavaScript
## Date:

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo-List</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <div class="container">
        <center>
            <h1>Todo - List</h1>
            <ul id="ullist">

            </ul>
            <input id="addtask">
            <button onclick="show()">ADD</button>
            <h1>Completed</h1>
            <ul id="donelist">

            </ul>
        </center>
    </div>

    <script src="./index.js"></script>
</body>
</html>

style.css

body{
    background-color: #E6CFA9;
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
}

.container{
    background-color: #EFF5D2;
    width: 300px;
    height: 350px;
}

li{
    list-style: none;
}

index.js

var input = document.getElementById("addtask")
var ullist  = document.getElementById("ullist")
var donelist = document.getElementById("donelist")

let list = new Array();
        
function show(){
    if(input.value!=''){
        list.push(input.value)
        ullist.innerHTML += '<li id="'+(list.length-1)+'"><button onclick="get('+(list.length-1)+')">'+input.value+'</button></li><br>'
        input.value = " "
    }
}

function get(id){
    donelist.innerHTML += "<li>"+(list[id])+"</li>"
    document.getElementById(id).style.display="none"
}


```

## OUTPUT

![alt text](<Screenshot 2025-09-15 103814.png>)

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
