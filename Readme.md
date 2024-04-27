# Conquering Responsive Layout Course By : Kevin Powell


## Day 01

1. Every elements in the HTML are by defaults response.
2. Never use value in pixels.
3. Use percentage instead of pixels.
4. Child totally depends on the parent. for example if the parent is having 80% (1000px) width  and, when we give 50% width to it's child it means 50% (500px) of 80% (100px).
5. Never ever give width and height explicitly untill, it is not required.
6. if you are giving padding and margin then try to give it is in em (depend on the parent container) or rem (depend on the body).
 By default 1 em or rem = 16px 



## Day 02

rem and em are both CSS units that are relative to the font size of an element. However, they have different behaviors and use cases.

1. rem (root em):

rem units are relative to the font size of the root element (html).
They are not affected by the font size of their parent elements.
Typically used for setting global sizing that you want to scale consistently across the entire     document.
Useful for setting margins, padding, and other layout-related properties.

Examples :

html {
    font-size: 16px; /* Base font size */
}

body {
    font-size: 1rem; /* Equivalent to 16px */
}

h1 {
    font-size: 2rem; /* Equivalent to 32px */
}

p {
    margin-bottom: 1.5rem; /* Margin will be 24px (1.5 * 16px) */
}

2. em 

em units are relative to the font size of the parent element.
They cascade: if you nest elements with em units, they'll be relative to their parent's font size.
Useful for creating layouts where sizes are proportional to the font size of their containing elements.

Examples : 

.container {
    font-size: 18px;
}

.box {
    font-size: 1.2em; /* Equivalent to 21.6px (1.2 * 18px) */
}

.box-inner {
    font-size: 0.8em; /* Equivalent to 17.28px (0.8 * 21.6px) */
}


## Day 03

min-width 

Specifies the minimum width that an element can have.
If the content within the element requires more space than the specified minimum width, the element will expand to accommodate it.
Useful for ensuring that elements have a minimum size to prevent content from becoming unreadable or overlapping.
Applied to block-level and replaced elements like divs, images, and tables.

Example:

.container {
    min-width: 300px; /* Ensure container has at least 300 pixels width */
}


max-width

Specifies the maximum width that an element can have.
If the content within the element would exceed the specified maximum width, the element will shrink to fit within this constraint.
Useful for creating responsive designs by limiting the maximum width of elements on larger screens, preventing them from becoming too wide.
Applied to block-level and replaced elements like divs, images, and tables.
Example:

.container {
    max-width: 800px; /* Ensure container does not exceed 800 pixels width */
}
