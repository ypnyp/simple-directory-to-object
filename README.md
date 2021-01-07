# simple-directory-to-object
Converts a whole directory recursively to usable NodeJS modules and objects

This is messily made. sorry.

# Usage
Usage is simple!

```js
const files = directoryToObject(module, './some/path');
console.log(files);
// output: {fileName: 'content. if successful, it'll be an entire NodeJS module instead!', directory: { maybeASubDirectory: { andThenAFile: [node module] }}}
```

Always remember to have `module` as the first argument, as it is required to load NodeJS Modules!

**You can also change the options,** as the third argument.
```
let defaultOptions = {
    extensions: ['js', 'json', 'coffee'],
    recurse: true,
    rename: function (name) {
        return name;
    },
    visit: function (obj) {
        return obj;
    }
};
```
