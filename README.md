 ## Real-time Character Counter

This is a simple real-time character counter that counts the number of characters in a textarea and displays the total number of characters and the number of remaining characters.
# Hosted Link
https://ronaksharma57.github.io/Real-time-Character-counter/
### Step-by-Step Explanation

#### HTML

The HTML code creates a simple webpage with a textarea and two paragraphs to display the total number of characters and the number of remaining characters.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Real-time Charater Counter</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <h2>Real-time Charater Counter</h2>
      <textarea
        id="textarea"
        class="textarea"
        placeholder="Please write your text here..."
        maxlength="50"
      ></textarea>
      <div class="counter-container">
        <p>
          Total Charaters:
          <span class="total-counter" id="total-counter"></span>
        </p>
        <p>
          Remaining:
          <span class="remaining-counter" id="remaining-counter"></span>
        </p>
      </div>
    </div>
    <script src="index.js"></script>
  </body>
</html>
```

#### CSS

The CSS code styles the textarea and the counter container.

```css
.container {
  width: 500px;
  margin: 0 auto;
}

h2 {
  text-align: center;
}

.textarea {
  width: 100%;
  height: 200px;
  padding: 10px;
  font-size: 16px;
}

.counter-container {
  margin-top: 20px;
}

.total-counter,
.remaining-counter {
  font-size: 16px;
}
```

#### JavaScript
```
const textareaEl = document.getElementById("textarea");
const totalCounterEl = document.getElementById("total-counter");
const remainingCounterEl = document.getElementById("remaining-counter");

textareaEl.addEventListener("keyup", () => {
  updateCounter();
});

updateCounter()

function updateCounter() {
  totalCounterEl.innerText = textareaEl.value.length;
  remainingCounterEl.innerText =
    textareaEl.getAttribute("maxLength") - textareaEl.value.length;
}
```
