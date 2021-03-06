# open

Open a file or url in the user's preferred application.

# Usage

```javascript
var open = require("open");
open("http://www.google.com");
```

`open` takes an optional argument specifying the program to be used to open the
file or URL.

```javascript
open("http://www.google.com", "firefox");
```

# Installation

    npm install open

# How it works

- on `win32` uses `start`
- on `darwin` uses `open`
- otherwise uses the `xdg-open` script from [freedesktop.org]

# Warning

The same care should be taken when calling open as if you were calling
[child_process.exec](http://nodejs.org/api/child_process.html#child_process_child_process_exec_command_options_callback)
directly. If it is an executable it will run in a new shell.
