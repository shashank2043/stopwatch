# Stopwatch Application

This project is a simple stopwatch application built using **HTML**, **CSS**, and **JavaScript**. It allows users to start, stop, and reset the timer with a visually appealing interface.

## Features

- Start the stopwatch to measure elapsed time.
- Stop the stopwatch to pause the timer.
- Reset the stopwatch to reset the time to `00:00:00.00`.
- Displays time in the format: `HH:MM:SS:MS` (Hours, Minutes, Seconds, Milliseconds).
- Smooth UI transitions with hover effects on buttons.

## How to Use

1. Open the `index.html` file in any modern web browser.
2. Click on the **Start** button to begin the stopwatch.
3. Click on the **Stop** button to pause the stopwatch.
4. Click on the **Reset** button to reset the timer to its initial state.

## File Structure

```
project-directory
|-- index.html    # Main HTML file
|-- styles.css    # CSS file for styling
|-- script.js     # JavaScript file for stopwatch functionality
```

## Code Highlights

### HTML

Defines the structure of the application:

```html
<div id="container">
  <div id="display">00:00:00.00</div>
  <div id="buttons">
    <button id="startBtn" onclick="start()">Start</button>
    <button id="stopBtn" onclick="stop()">Stop</button>
    <button id="resetBtn" onclick="reset()">Reset</button>
  </div>
</div>
```

### CSS

Customizes the appearance and adds transitions for buttons:

```css
#startBtn {
  background-color: hsl(120, 100%, 50%);
}
#startBtn:hover {
  background-color: hsl(120, 100%, 40%);
}
#stopBtn {
  background-color: hsl(0, 100%, 65%);
}
#stopBtn:hover {
  background-color: hsl(0, 100%, 55%);
}
#resetBtn {
  background-color: hsl(228, 100%, 50%);
}
#resetBtn:hover {
  background-color: hsl(228, 100%, 40%);
}
```

### JavaScript

Implements the stopwatch logic:

```javascript
function start() {
    if (!isRunning) {
        startTime = Date.now() - elapsedTime;
        timer = setInterval(update, 10);
        isRunning = true;
    }
}

function stop() {
    if (isRunning) {
        clearInterval(timer);
        isRunning = false;
    }
}

function reset() {
    clearInterval(timer);
    isRunning = false;
    elapsedTime = 0;
    display.textContent = "00:00:00.00";
}
```

## Browser Compatibility

This application is compatible with all modern browsers, including:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

## Future Enhancements

- Add a lap functionality to record intermediate times.
- Allow customization of the timer format (e.g., exclude milliseconds).
- Make it mobile-responsive for smaller screens.

## License

This project is open source and available under the [MIT License](LICENSE).

---

Feel free to customize and extend this project as per your requirements!

