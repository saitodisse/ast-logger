# simple instrument javascript proposal

- using debug lib (https://www.npmjs.com/package/debug)


#### install debug

```
npm i
```

#### run

```
DEBUG=* ./file1.js
```

![alt text](https://files.gitter.im/saitodisse/WonM/blob "Result")


## TODO

- [ ] insert snippet below at top of the file
```js
var debug = require('debug')('__FILE_NAME_HERE__');
```

- [ ] insert snippet below on top of each function
```js
var __debug_data__ = {
  name: '__FUNCTION_NAME__',
  arguments: arguments,
  line: {original_line: __ORIGINAL_LINE_NUMBER__}
};
```

- [ ] insert snippet below before each return statement
```js
__debug_data__.return_data = __RETURN_EXPRESSION__;
debug(__debug_data__);
```