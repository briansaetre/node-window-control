# node-window-control
Manage windows in Windows and macOS.
(forked from node-window-manger)

# Quick start

The following example shows how to get the currently focused window's title and hide it.

```javascript
const { windowManager } = require("node-window-control");

const window = windowManager.getActiveWindow();

// Prints the currently focused window bounds.
console.log(window.getBounds());

// This method has to be called on macOS before changing the window's bounds, otherwise it will throw an error.
// It will prompt an accessibility permission request dialog, if needed.
windowManager.requestAccessibility();

// Sets the active window's bounds.
window.setBounds({ x: 0, y: 0 });
```

# Documentation

The documentation and API references are located in the [`docs`](docs) directory.
