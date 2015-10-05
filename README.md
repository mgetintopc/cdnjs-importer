<!---------------------------------------------------------------------------->
<!-- STOP, LOOK & LISTEN!                                                   -->
<!-- ====================                                                   -->
<!-- Do NOT edit this file directly since it's generated from a template    -->
<!-- file, using https://github.com/IonicaBizau/node-blah                   -->
<!--                                                                        -->
<!-- If you found a typo in documentation, fix it in the source files       -->
<!-- (`lib/*.js`) and make a pull request.                                  -->
<!--                                                                        -->
<!-- If you have any other ideas, open an issue.                            -->
<!--                                                                        -->
<!-- Please consider reading the contribution steps (CONTRIBUTING.md).      -->
<!-- * * * Thanks! * * *                                                    -->
<!---------------------------------------------------------------------------->

![cdnjs-importer](http://i.imgur.com/OLwedYJ.png)

# `$ cdnjs-importer` [![Donate now][donate-now]][paypal-donations]

Easy way to import a library into CDNJS.

## Installation

You can install the package globally and use it as command line tool:

```sh
$ npm i -g cdnjs-importer@2.0.0-beta
```

Then, run `cdnjs-importer --help` and see what the CLI tool can do.

```sh
$ cdnjs-importer --help
Usage: cdnjs-importer [options]

Options:
  -g, --git-url <git-url>  Your library git url.
  -p, --path <path>        The path to your cdnjs local repository.
  -h, --help               Displays this help.
  -v, --version            Displays version information.

Examples:
  cdnjs-importer -g git@github.com:IonicaBizau/gh.js.git # adds gh.js to cdnjs
  cdnjs-importer -g ... -p path/to/cdnjs

The default cdnjs repository location is in ~/cdnjs

Documentation can be found at https://github.com/cdnjs/cdnjs-importer
```

## Example

Here is an example how to use this package as library. To install it locally, as library, you can do that using `npm`:

```sh
$ npm i cdnjs-importer
```

```js
// Dependencies
var CdnJsImporter = require("cdnjs-importer")
  , Path = require("path")
  ;

// Test adding CaiuSS
CdnJsImporter({
    cdnjs: Path.resolve(__dirname, "../../cdnjs")
  , debug: true
  , libs: [
        "git@github.com:IonicaBizau/CaiuSS.git"
    ]
}, function (res) {
    console.log(res);
});

```

## Documentation

For full API reference, see the [DOCUMENTATION.md][docs] file.

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## Press Highlights
None yet. If you wrote or found an article about this project, [add it][contributing] in this section.  :memo:

## License
[KINDLY][license] © [Ionică Bizău][website]–The [LICENSE](/LICENSE) file contains
a copy of the license.

[license]: http://ionicabizau.github.io/kindly-license/?author=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica@gmail.com%3E&year=2015
[contributing]: /CONTRIBUTING.md
[website]: http://ionicabizau.net
[docs]: /DOCUMENTATION.md
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=MG98D7NPFZ3MG
[donate-now]: http://i.imgur.com/6cMbHOC.png
