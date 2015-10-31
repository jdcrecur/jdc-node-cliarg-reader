# jdc-node-cliarg-reader
Node command line argument reader into object

A very simple to use cli arg. reader

Example cli call to a file named ``server.js``

```
node server.js devmode arg2=one|two|potatoes arg3=2742 someOtherArg
```

In your application file you can now access these arguments very easily using the `readAll()` function:
```
var cliarg = require('cliarg').readAll();
/** the variable cliarg will now be a nice object looking like:
 * {
 * 		devmode: true,
 * 		arg2 : ['one', 'two', 'potatoes'],
 * 		arg3 : 2742,
 * 		someOtherArg : false
 * }
 **/
