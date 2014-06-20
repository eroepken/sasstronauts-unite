#Slide Notes:

##Conversion

* Can be done the other way around as well.

##Importing

* This will look for _file.scss and _another-file.scss.
* You can also import a whole file inside of an element, if you choose. For example:

  .element {
    @import 'file';
  }

* Can't have a partial and non-partial of the same name in the same folder. For example:

  $family: unquote("Droid+Sans");
  @import url("http://fonts.googleapis.com/css?family=#{$family}");

* Interpolation is allowed in CSS import statements only, not Sass import statements.
* The underscore tells Sass not to compile the partial to it's own CSS file. Otherwise, it will be compiled as a CSS import.

##Extending

* You can also extend upon an element which extends another element.
* "Selector sequences, such as `.foo .bar` or `.foo + .bar`, currently can’t be extended." - Sass Documentation on @extend
* @extend is currently not supported inside of @media directives.
* Use the !optional flag to signify that the compiler can pass over it if the extended element doesn't exist.