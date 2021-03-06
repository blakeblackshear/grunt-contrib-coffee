# grunt-contrib-coffee
> Compile CoffeeScript files to JavaScript (part of the [grunt-contrib](https://github.com/gruntjs/grunt-contrib) collection). Submitted by [Eric Woroshow](https://github.com/errcw).

### Overview

Inside your `grunt.js` file add a section named `coffee`. This section specifies the files to compile and the options passed to [CoffeeScript](http://coffeescript.org/#usage).

#### Parameters

##### files ```object```

This defines what files this task will process and should contain key:value pairs.

The key (destination) should be an unique filepath (supports [grunt.template](https://github.com/cowboy/grunt/blob/master/docs/api_template.md)) and the value (source) should be a filepath or an array of filepaths (supports [minimatch](https://github.com/isaacs/minimatch)).

Note: When the value contains an array of multiple filepaths, the contents are concatenated in the order passed.

##### options ```object```

This controls how this task (and its helpers) operate and should contain key:value pairs, see options below.

#### Options

##### bare ```boolean```

Compile the JavaScript without the top-level function safety wrapper.

#### Config Example

``` javascript
coffee: {
  compile: {
    options: {
      bare: true
    },
    files: {
      "path/to/result.js": "path/to/source.coffee",
      "path/to/another.js": ["path/to/sources/*.coffee", "path/to/more/*.coffee"]
    }
  }
}
```

## Release History

* 2012/08/10 - v0.2.0 - Refactored from grunt-contrib into individual repo.