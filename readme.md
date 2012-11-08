# VI Front-end standards

The following document outlines a reasonable style guide for Front-end development within VI Company.
It is not meant to be prescriptive and I do not wish to impose my style
preferences on other people's code. However, these guidelines do strongly
encourage the use of existing, common, sensible patterns.

This is a living document and new ideas are always welcome. Please
contribute.


## Pillars of Front-end development

* Separation of presentation, content, and behavior (Progressive Enhancement).
* Markup should be well-formed, semantically correct and generally valid.
* Javascript should progressively enhance the experience (Unobtrusive Javascript).


## Javascript

We use [idiomatic.js](https://github.com/svankerkfort/idiomatic.js) with the following rules and exceptions:

### Rules and exceptions

* We use tabs for whitespace with an indent size of 4 spaces.
* We use single quotes!
* We don't use a space between the parens and arguments or condition.

  ```javascript
    // Allowed

    if (condition) {
      // statements
    }

    function foo(arg, arg2) {
      // do stuff
    }
  ```


## CSS

We use [idiomatic-css](https://github.com/svankerkfort/idiomatic-css) with the following rules and exceptions:

### Rules and exceptions

* Don't use IDs for styling.
  * They mess up [specificity](http://htmldog.com/guides/cssadvanced/specificity/) because they are too strong.
  * Styling using IDs makes it impossible to use the same element twice on the same page.
* We prefer relative units (em & rem) over absolute units (px).

### Grids

TODO: determine the best grid (for the project).

* [Dead Simple Grid](https://github.com/mourner/dead-simple-grid)
* [Golden Grid System](http://goldengridsystem.com)
* [Bootstrap Grid](http://twitter.github.com/bootstrap/scaffolding.html#gridSystem)
* [OOCSS Grid](https://github.com/stubbornella/oocss)


### Reset

We prefer [Normalize.css](http://necolas.github.com/normalize.css/) for our projects. In case we're building an app you could consider a real reset stylesheet.


## HTML(5)

* When using HTML5, which allows for either HTML or XHTML style syntax, we prefer the strictness of XHTML. Therefore, all tags must be properly closed ([source](http://w3.org/TR/xhtml1/#C_2)).
* All tags and attributes must be written in lowercase. Additionally, we prefer that any attribute values also be lowercase, when the purpose of the text therein is only to be interpreted by machines.
* All attributes must have a value, and must use double-quotes ([source](http://w3.org/TR/xhtml1/#h-4.4)).


## TODO: Code organization

Code organization is an important part of any CSS code base, and crucial for
large code bases.

* Logically separate distinct pieces of code.
* Use separate files (concatenated by a build step) to help break up code for
  distinct components.
* If using a preprocessor, abstract common code into variables for color,
  typography, etc.


## Build and deployment

We use grunt.js for client-side linting, testing and compressing.

* [Our grunt.js documentation](https://github.com/svankerkfort/vi-standards/blob/master/grunt.md)
* [grunt.js](https://github.com/cowboy/grunt)


## Acknowledgements

We got our inspiration, quotations and guidelines from the following sources:

* [idiomatic.js](https://github.com/svankerkfort/idiomatic.js)
* [idiomatic-css](https://github.com/svankerkfort/idiomatic-css)
* [OOCSS](https://github.com/stubbornella/oocss)
* [SMACCS](http://smacss.com)
* [Front-end Manifesto](http://f2em.com)