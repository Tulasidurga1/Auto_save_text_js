# Auto_save_text_js
# Hosted Link :-https://tulasidurga1.github.io/Auto_save_text_js/
# explanation:-
### HTML:

<!DOCTYPE html>: This declaration defines the document type and version of HTML being used.

<html lang="en">: This is the opening tag for the HTML document, and it specifies the document's language as English.

<head>: This section contains metadata about the web page, such as character encoding, viewport settings, the title of the page, and a link to an external CSS file.

<meta charset="UTF-8">: Sets the character encoding to UTF-8, which includes a wide range of characters from various languages.

<meta name="viewport" content="width=device-width, initial-scale=1.0">: Configures the viewport to adjust the page's width to the device's width and sets the initial zoom level to 1.0.

<title>Auto Save Textarea</title>: Sets the title of the web page, which is displayed in the browser's title bar or tab.

<link rel="stylesheet" href="style.css">: Links an external CSS file named "style.css" to style the page's content.

<body>: This is the body of the web page where the visible content is placed.

<div class="container">: A <div> element with a class of "container" is used to create a centered content container.

<h1>Auto Save Textarea</h1>: An <h1> heading displaying the title of the page.

<textarea id="myTextarea" rows="10" cols="50" placeholder="Start typing here..."></textarea>: This <textarea> element has an ID of "myTextarea," 10 rows, 50 columns, and a placeholder text instructing the user to start typing.

<script src="script.js"></script>: Links an external JavaScript file named "script.js" to provide functionality for the page.

### CSS (style.css):
The CSS code defines the styles for various elements on the page, including the body, container, headings, and textarea. It specifies font styles, background colors, padding, borders, and other visual aspects to make the page visually appealing.

### JavaScript (script.js):
The JavaScript code provides the functionality for auto-saving text entered into the textarea:

const textarea = document.getElementById("myTextarea");: This line gets a reference to the <textarea> element with the ID "myTextarea" so that it can be manipulated in JavaScript.

function saveToLocalStorage() { ... }: This function is defined to save the content of the textarea to the browser's local storage.

localStorage.setItem("savedText", textarea.value);: Inside the saveToLocalStorage function, this line stores the current value of the textarea in the local storage under the key "savedText."

The code then checks if there's existing data in local storage with the key "savedText" using localStorage.getItem("savedText"). If data exists, it populates the textarea with that saved text.

textarea.addEventListener("input", saveToLocalStorage);: An event listener is added to the textarea. It listens for input changes (typing) and calls the saveToLocalStorage function whenever the user types or modifies the content. This ensures that the content is automatically saved to local storage as the user types.

In summary, this code creates a web page with a styled textarea that automatically saves its content to the browser's local storage as the user types. The saved content is also loaded back into the textarea if it exists in local storage.
