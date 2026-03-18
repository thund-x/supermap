# Change Log

## v3.0.5 -> v4.0.0

- Dropped CommonJS modules support. Stay in version 3 if you still depend on CommonJS.\

- Removed default `SuperMap` export. Import the map as `import { SuperMap } from
  "@thunder04/supermap;`. 

- Removed `options.expireAfter`. Add its value with the `set` method's `ttl`
  parameter.

- Removed `options.intervalTime`. Expired items are now removed as soon as
  possible.

- Renamed `options.itemsLimit` to `options.capacity`.

- Renamed `options.onSweep` to `options.onEntryExpiry`.

- Replaced overloaded `first(key?: boolean)` method with `first()` and
  `firstKey()` methods respectively.

- Replaced overloaded `last(key?: boolean)` method with `last()` and
  `lastKey()` methods respectively.

- Replaced overloaded `find(..., key?: boolean)` method with `find(...)` and
  `findKey(...)` methods respectively.

- Replaced `sweep()` with `retain()`. Retain now keeps items which the callback
  returns `false` instead of `true`.

- Add `filterMut` that operate on the map in-place.
