# Hamburger

A CSS-only implementation of the layered slide-in UI menu concept popularized by Facebook, Google and Mailbox. Inspired by Hakim's [Meny](https://github.com/hakimel/meny) and powered by CSS3.

## Introduction

Verethragna manages and displays lectures in accordance with openlectures production guidelines and specifications. The database is bidirectionally synchronized to Google Drive. Subsequent updates will allow advanced user-tracking and extensive third-party API integration

## Quick Start

Hamburger is registered on [Bower](https://github.com/twitter/bower). To install via Bower:

```bash
bower install hamburger
```

If that's not your cup of tea, clone the repository to a local directory and you're ready to rock and roll!

## Using Hamburger

Add ```_hamburger.scss``` to your stylesheet by importing it into your main encapsulation file

```scss
@import "hamburger";
```

Hamburger targets the HTML5 ```nav``` and ```main``` elements for implementation of the sliding functionality. Any navigation or content you want to keep off-canvas goes inside ```nav```. Everything else that should remain onscreen goes inside ```main```.

Here's a sample document layout:
```html
<body>
  <nav>
    Menu Item 1
    Menu Item 2
    Menu Item 3
  </nav>
  <main>
    Lorem Ipsum Dolor Sit Amet
  </main>
</body>
```

If you wish to have the navigation menu appear to move towards the front of the screen as it slides in (like how it's done in Mailbox), put your navigations inside a menu item:
```html
<nav>
  <menu>
    Menu Item 1
    Menu Item 2
    Menu Item 3
  </menu>
</nav>
```

Note that in all cases, the ```main``` element has to come after the ```nav``` element for the animation to work properly (we're using the CSS adjacent selector to make the magic happen).

If you need to provide support for browsers without HTML5 support, you should use the [html5shiv](https://github.com/aFarkas/html5shiv) to implement the ```nav```,```menu``` and ```main``` elements.

## Versioning

Development will be maintained under the Semantic Versioning guidelines as much as possible in order to ensure transparency and backwards compatibility.

Releases will be numbered with the following format:

`<major>.<minor>.<patch>`

And constructed with the following guidelines:

+ Breaking backward compatibility bumps the major (and resets the minor and patch)
+ New additions without breaking backward compatibility bump the minor (and resets the patch)
+ Bug fixes and miscellaneous changes bump the patch

For more information on SemVer, visit http://semver.org/.

## Roadmap

+ Add CSS and SASS versions
+ Give users greater control over features like opacity and scaling
+ Add stylized documentation
+ Add more samples (e.g with backgrounds or shadows)

## Bug Tracking and Feature Requests

Have a bug or a feature request? [Please open a new issue](https://github.com/kenlimmj/hamburger/issues).

Before opening any issue, please search for existing issues and read the [Issue Guidelines](https://github.com/necolas/issue-guidelines), written by [Nicolas Gallagher](https://github.com/necolas/).

## Contributing

Please submit all pull requests against *-wip branches.
All markup should conform to their respective community style guidelines:
+ [HTML and CSS](http://github.com/mdo/code-guide)

## Code Status

[![Code Climate](https://codeclimate.com/github/kenlimmj/hamburger.png)](https://codeclimate.com/github/kenlimmj/hamburger)
[![Build Status](https://secure.travis-ci.org/kenlimmj/hamburger.png)](http://travis-ci.org/kenlimmj/hamburger)
[![Dependency Status](https://gemnasium.com/kenlimmj/hamburger.png)](https://gemnasium.com/kenlimmj/hamburger)

DISCLAIMER: These nice badge things are provided as-is, because everyone seems to have them. They do not, in any way, reflect the real awesomeness of our code (Yeah right).

DISCLAIMER to DISCLAIMER: If looks like these things always show that the build is failing, or that we're out of date, really, we're not :P

## Author

**Kenneth Lim**
+ http://twitter.com/kenlimmj
+ http://github.com/kenlimmj

## Copyright and License

Licensed under the MIT License (MIT).

Copyright © 2013 The Legless Llama LLP.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
