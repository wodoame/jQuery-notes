In jQuery, the `$(document).ready()` function is used to ensure that your code runs only after the DOM (Document Object Model) has been fully loaded. This is important because attempting to manipulate or interact with DOM elements before they are fully loaded can lead to unexpected behavior.

Here's an example of how you can use `$(document).ready()`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document Ready Example</title>
  <script src="https://code.jquery.com/jquery-3.6.4.min.js"></script>
  <!-- Include the jQuery library from a CDN (Content Delivery Network) -->
</head>
<body>

  <!-- Your HTML content here -->

  <script>
    // This code will be executed once the DOM is fully loaded
    $(document).ready(function() {
      // Your jQuery code goes here
      // For example, you can manipulate DOM elements or attach event handlers
      console.log("Document is ready!");

      // Example: Change the text of an element with the ID "exampleElement"
      $("#exampleElement").text("Hello, jQuery!");
    });
  </script>

</body>
</html>
```

In the above example, replace `"#exampleElement"` with the actual ID or selector of the element you want to manipulate. This ensures that your jQuery code runs only when the DOM is ready.

Alternatively, you can use the shorthand form `$(function() { /* your code here */ });` as a shortcut for `$(document).ready(function() { /* your code here */ });`.

Keep in mind that in modern web development, using `$(document).ready()` is somewhat optional with the latest versions of jQuery. You can often place your `<script>` tags at the end of the `<body>` element to achieve a similar effect, as browsers now typically load scripts asynchronously. However, in some cases, you may still prefer to use `$(document).ready()` for clarity or compatibility with older browsers.
