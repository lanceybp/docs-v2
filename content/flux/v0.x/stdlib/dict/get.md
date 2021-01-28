---
title: dict.get() function
description: >
  The `dict.get()` function returns the value of a specified key in a dictionary
  or a default value if the key does not exist.
aliases:
  - /influxdb/v2.0/reference/flux/stdlib/dict/get/
  - /influxdb/cloud/reference/flux/stdlib/dict/get/
menu:
  flux_0_x_ref:
    name: dict.get
    parent: Dictionary
weight: 301
introduced: 0.97.0
---

The `dict.get()` function returns the value of a specified key in a dictionary
or a default value if the key does not exist.

```js
import "dict"

dict.get(
  dict: [1: "foo", 2: "bar"],
  key: 1,
  default: ""
)
```

## Parameters

<p>
  {{< req "All paremeters are required" >}}
</p>

### dict
Dictionary to return a value from.

_**Data type:** Dictionary_

### key
Key to return from the dictionary.

_**Data type:** String | Boolean | Integer | Uinteger | Float | Time | Bytes_

### default
Default value to return if the `key` does not exist in the dictionary.
Must be the same type as values in the dictionary.

_**Data type:** String | Boolean | Integer | Uinteger | Float | Time | Bytes_

## Examples

##### Return a property of a dictionary
```js
import "dict"

d = [1: "foo", 2: "bar"]

dict.get(
  dict: d,
  key: 1,
  default: ""
)

// Returns foo
```