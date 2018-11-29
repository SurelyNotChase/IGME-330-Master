# `this` Binding Notes

## I. Overview
- in 230 we discussed how the value of `this` in a function depends on how it is called -> https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-6.md#section4
- if a function is called by an event handler or event listener, the value of `this` is the object that triggered the event (a button in an `.onclick` handler,  or the `window` in an `.onload` handler function for example)
- this can sometimes create issues - see below!

## II. counter-1.html

- no surprises here!
- clicking the button increments the counter

**counter-1.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Counter 1</title>
</head>
<body>
<button id="clickButton">Click Me!</button>
<p id="label">???</p>

<script>
"use strict";
let counter = 0;
	
function incrementCounter(){
		counter ++;
}

function updateLabel(){
	label.innerText = counter;
}

clickButton.addEventListener("click",incrementCounter);
clickButton.addEventListener("click", updateLabel);

</script>
</body>
</html>
```

## III. counter-2.html

- here we are trying an object-oriented approach, and encapsulating our counter logic and state into a `Counter` class

**counter-2.html**

```html

```

## Reference
- [MDN - `Function.bind()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)