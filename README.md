<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript and DOM Manipulation</title>
  <style>
    /* Basic CSS for styling */
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background-color: #f4f4f4;
    }

    .message {
      margin-top: 20px;
      padding: 10px;
      background-color: #d3ffd3;
      border: 1px solid #d1e7d1;
    }

    .button {
      padding: 10px 15px;
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
      margin-top: 20px;
    }

    .button:hover {
      background-color: #45a049;
    }

    .remove-button {
      padding: 10px 15px;
      background-color: #f44336;
      color: white;
      border: none;
      cursor: pointer;
    }

    .remove-button:hover {
      background-color: #e41f24;
    }
  </style>
</head>
<body>
  <h1>Introduction to JavaScript and DOM Manipulation</h1>

  <p>This page demonstrates how JavaScript can manipulate HTML content and CSS dynamically.</p>

  <!-- Dynamic Content Section -->
  <div id="message" class="message">
    <p>Click the buttons below to interact with the page!</p>
  </div>

  <button class="button" id="changeTextButton">Change Text</button>
  <button class="button" id="changeStyleButton">Change Style</button>
  <button class="remove-button" id="removeElementButton">Remove Message</button>

  <div id="newElementSection">
    <button class="button" id="addElementButton">Add New Element</button>
  </div>


  
  
  
  
  
  
  <!-- Link to External JS File -->
  <script src="script.js"></script>
</body>
</html>


// Function to change text content dynamically
document.getElementById("changeTextButton").addEventListener("click", function() {
  const messageDiv = document.getElementById("message");
  messageDiv.innerHTML = "<p>The text has been changed dynamically!</p>";
});

// Function to modify CSS styles via JavaScript
document.getElementById("changeStyleButton").addEventListener("click", function() {
  const messageDiv = document.getElementById("message");
  messageDiv.style.backgroundColor = "#ffeb3b";  // Change background color
  messageDiv.style.color = "black";  // Change text color
});

// Function to remove an element when the button is clicked
document.getElementById("removeElementButton").addEventListener("click", function() {
  const messageDiv = document.getElementById("message");
  messageDiv.remove();  // Remove the message div from the DOM
});

// Function to add a new element dynamically
document.getElementById("addElementButton").addEventListener("click", function() {
  const newElementSection = document.getElementById("newElementSection");

  // Create a new element (paragraph)
  const newElement = document.createElement("p");
  newElement.textContent = "This is a new paragraph added dynamically!";
  newElement.style.backgroundColor = "#90caf9"; // Add some style

  // Append the new element to the section
  newElementSection.appendChild(newElement);
});
