*This repository is a mirror of the [component](http://component.io) module [component/timers](http://github.com/component/timers). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-timers`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# timers

  Timer management to clear large batches of timers.

## Installation

    $ component install component/timers

## Example

  In the following example the last two timers will not fire.

```js
var Timers = require('timers');
var timers = new Timers;

timers.timeout(function(){
  console.log('one');
}, 1000);

timers.timeout(function(){
  console.log('two');
}, 2000);

timers.timeout(function(){
  console.log('three');
}, 3000);

setTimeout(function(){
  timers.clear();
}, 1500);
```

## API

### Timers()

  Initialize a new timer set with optional `ids`.

### Timers.timeout(fn:Function, ms:Number)

  Add timeout `fn`.

### Timers.interval(fn:Function, ms:Number)

  Add interval `fn`.

### Timers.clear()

  Clear all timers.

## License

  MIT
