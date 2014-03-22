debug-console
=============

A simple togglable interactive mode for node.js.

You can start and stop it from any place in your code.
It allows you to interact with your global objects and evaluate new pieces. You can use arrow keys to navigate through commands you ran.

Please note that it switches stdin to rawMode, so if you have any listeners on it, it's best to close them.

There are two functions available:

* ```start([name]);```
    * Starts interactive mode
    * If name is specified it's printed at the beginning of interactive session
* ```stop();```
    * Stops interactive mode

To quit type ```:q```

Example usage:

```javascript
var interactive = require('debug-console');
interactive.start('Point 1');

//Interactive mode started at: Point 1
//> console.log(5)
//5
//undefined
//> :q
//Interactive mode off
```

Licensed under MIT license. Copyright (c) 2014 Adam Paszke