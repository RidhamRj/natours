# natours
 Natours Project

[Live Preview](https://catalinpit.github.io/natours/)

*Taking notes while building the application from Jonas's tutorial => [Advanced CSS and SASS](https://udemy.com/course/advanced-css-and-sass).*

*The application might look different from the one from the tutorial. I am trying to change it as much as possible.*

# TABLE OF CONTENTS
- [natours](#natours)
- [TABLE OF CONTENTS](#table-of-contents)
- [THE THREE PILLARS TO WRITE GOOD HTML AND CSS](#the-three-pillars-to-write-good-html-and-css)
- [HOW CSS WORKS: A LOOK BEHIND THE SCENES](#how-css-works-a-look-behind-the-scenes)

# THE THREE PILLARS TO WRITE GOOD HTML AND CSS

**Responsive design**

* Fluid layouts
* Media queries
* Responsive images
* Correct units
* Desktop-first vs mobile-first

**Maintainable and scalable code**

* Clean
* Easy-to-understand
* Growth
* Reusable
* How to organize files
* How to name classes
* How to structure HTML

**Web performance**

* Less HTTP requests
* Less code
* Compress code
* Use a CSS preprocessor
* Less images
* Compress images

# HOW CSS WORKS: A LOOK BEHIND THE SCENES

**What happens to CSS when a webpage is loaded?**

Load HTML => Parse HTML => The browser builds the `Document Object Model (DOM)` (where the entire decoded HTML code is stored).

Parse HTML => Load CSS => Parse CSS => `CSS Object Model (CSSOM)`.

Parse CSS

* Resolve conflicting CSS declarations (cascade)
* Process final CSS values

**CASCADE**

It is the process of combining different stylesheets and resolving conflicts between different CSS rules and declarations when more than one rule applies to a certain element. 

`IMPORTANCE` **>** `SPECIFICITY` **>** `SOURCE ORDER`

Firstly, the cascade starts by giving the conflicting declarations different importances based on where they are declared, so based on their source.

**Importance**

1. User `!important` declarations (*most important declarations*)
2. Author `!important` declarations
3. Author declarations
4. User declarations
5. Default browser declarations

**Specificity** (SAME IMPORTANCE)

1. Inline styles
2. IDs
3. Classes, pseudo-classes, attribute
4. Elements, pseudo-elements

**Source order** (SAME SPECIFICITY)

The last declaration in the code will override all the other declarations and will be applied.

**Points to remember:**

* CSS declarations marked with `!important` have the highest priority.
* Only use `!important` as a last resource. It is better to use correct specificities - **more maintainable code**!
* Inline styles always have priority over styles in external stylesheets. (You should NOT use inline styles)
* A selector that contains **1** ID is more specific than one with **1000** classes.
* A selector that contains **1** class is more specific than one with **1000** elements.
* The universal selector `*` has no specificity value.
* Rely more on **specificity** than on the **order** of selectors. 
* Rely on order when using 3rd-party stylesheets - always put your author stylesheet last.