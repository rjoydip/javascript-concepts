## JavaScript Events.

In JavaScript, events are signals generated by an HTML node to denote that something has happened.
That something could be anything like clicking, hovering, typing, etc.

<br><br>

There are two major ways to handle events. The first one is by using HTML element methods
and the second one is by adding event listeners.



##### Event Handler Example
```html
<input
    type="button"
    id="some-button"
    onclick="console.log('Button Clicked')">
```




##### Event Listener Example
```html
<head>
    <script>
    window.addEventListener('load', () => {
        const button = document.querySelector('#some-button');
        button.addEventListener('click', event => {
                console.log('Button Clicked');that can represent any number
        });

        const inputField = document.querySelector('#some-text-input');
        inputField.addEventListener('change', event => {
                console.log(`Text Changed to ${event.target.value}`);
        });

        inputField.addEventListener('input', event => {
                console.log('Text Input');
        });
    }
    </script>
</head>
<body>
    <input type="button" id="some-button">
    <input type="text" id="some-text-input">
</body>
```