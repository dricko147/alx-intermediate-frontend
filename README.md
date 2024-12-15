# alx-intermediate-frontend

CSS Preprocessors: SASS/SCSS for Efficient Styling
Objective
Learn to use CSS preprocessors for more efficient and manageable styling by exploring SASS/SCSS features and techniques.

Topics Covered
Introduction to SASS/SCSS
What is SASS/SCSS? SASS (Syntactically Awesome Style Sheets) and SCSS (Sassy CSS) are popular CSS preprocessors that add powerful features to CSS. They allow developers to write code that is more maintainable, scalable, and readable by introducing variables, nesting, modules, mixins, and more.

Why Use SASS/SCSS?

Enhanced CSS: SASS/SCSS extends CSS with advanced features.
Maintainability: Easier to manage large stylesheets.
Reusability: Encourages code reuse with mixins and modules.
Variables and Nesting
Variables

Variables allow you to store values that can be reused throughout your stylesheet, making it easier to maintain consistent styling. They are declared using the $ symbol.

$primary-color: #333;
$font-stack: Helvetica, sans-serif;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
Nesting

Nesting enables you to write CSS rules in a hierarchical structure that mirrors the HTML structure, improving readability and organization.

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
Mixins and Functions
Mixins

Mixins allow you to create reusable chunks of CSS. You can pass arguments to mixins to make them more flexible.

@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, 0.25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme(DarkRed);
}
Functions

SASS functions let you perform calculations and return values. They are useful for creating dynamic styles.

@function double($number) {
  @return $number * 2;
}

.box {
  width: double(20px);
}
Partials and Import
Partials

Partials are small SASS files that contain snippets of CSS. They are useful for organizing styles into modular, reusable pieces. A partial file name begins with an underscore (e.g., _variables.scss).

Importing Partials You can import partials into your main SASS file using the @use or @import rule to keep your styles organized.

// styles.scss
@use 'variables';
@use 'mixins';

body {
  font: 100% variables.$font-stack;
}
Compiling SASS/SCSS
Tools for Compiling

To use SASS/SCSS, you need to compile it into standard CSS. This can be done using command-line tools, task runners, or build systems like:

Command Line: sass input.scss output.css
Watching Files: sass --watch input.scss:output.css
Build Tools: Webpack, Gulp, or Grunt
Workflow Integration

Integrating SASS/SCSS compilation into your development workflow ensures that your styles are always up-to-date.

By mastering these features of SASS/SCSS, you can create more efficient and manageable stylesheets that improve the maintainability and scalability of your projects.

Additional Resources
Sass Basics
Sass flow control directives
Sass references