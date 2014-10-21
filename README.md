loop-grid-selector
===

Range selector for [loop-grid](https://github.com/mmckegg/loop-grid).

## API

```js
var Selector = require('loop-grid-selector')
```

### `var selection = Selector(shape)`

Returns an extended instance of ObservGrid with `shape` specified.

### selector.start(inputGrid, done)

Pass in an observable ArrayGrid. `done` will be called on `stop` or before subsequent `start`.

Any truthy values will trigger a selection. Simultaneous true values will trigger range selection. `selection` will have `.set(selectedIndexes)` called on every change.

### selector.clear()

Sets `selection` to an empty array.

### selector.stop()

Release watch of `inputGrid` and call `done`.