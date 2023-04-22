The loading attribute on an img element can be set to lazy to tell the browser not to fetch the image resource until it is needed (as in, when the user scrolls the image into view). As an additional benefit, lazy loaded elements will not load until the non-lazy elements are loaded - this means users with slow internet connections can view the content of your page without having to wait for the images to load.

Give your new img element a loading attribute set to lazy.

Step 8
The Referer HTTP header contains information about the address or URL of a page that a user might be visiting from. This information can be used in analytics to track how many users from your page visit freecodecamp.org, for example. Setting the rel attribute to noreferrer omits this information from the HTTP request. Give your a element a rel attribute set to noreferrer.

The <blockquote> HTML element indicates that the enclosed text is an extended quotation. Usually, this is rendered visually by indentation (see Notes for how to change it). A URL for the source of the quotation may be given using the cite attribute, while a text representation of the source can be given using the <cite> element.

The <article> HTML element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.

The <aside> HTML element represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.

Step 27
Create an html selector and give it a font-size property set to 62.5%. This will set the default font size for your web page to 10px (the browser default is 16px).

This will make it easier for you to work with rem units later, as 2rem would be 20px.

Step 29
Create an h1 selector, and set the font-family property to Anton with the fallback of sans-serif.

Step 32
Now you are ready to start putting together the grid layout. CSS Grid offers a two-dimensional grid-based layout, allowing you to center items horizontally and vertically while still retaining control to do things like overlap elements.

Begin by creating a main selector and giving it a display property set to grid.

Step 33
Now you can style the layout of your grid. CSS Grid is similar to Flexbox in that it has a special property for both the parent and child elements.

In this case, your parent element is the main element. Set the content to have a three-column layout by adding a grid-template-columns property with a value of 1fr 94rem 1fr. This will create three columns where the middle column is 94rem wide, and the first and last columns are both 1 fraction of the remaining space in the grid container.

The max-content keyword value
According to W3C specifications, max-content represents a box’s ideal size in a given axis when given infinite available space.

In other words, max-content represents the size a box needs to contain all of its content without being wrapped or it overflows the box.

The min-content keyword value
According to the W3C specifications, the min-content is the smallest size a box can take without overflowing its content.

For horizontal content, the min-content uses the length of the widest bit of content in the element box and automatically sets that length value as the box width.

Step 34
Use the minmax function to make your columns responsive on any device. The minmax function takes two arguments, the first being the minimum value and the second being the maximum. These values could be a length, percentage, fr, or even a keyword like max-content.

Wrap each of your already defined values of the grid-template-columns property in a minmax function, using each value as the second argument. The first argument should be 2rem, min-content, and 2rem respectively.

Step 35
To add space between rows in the grid layout, you can use the row-gap property. Give the main selector a row-gap property of 3rem.

Step 36
Your magazine will have three primary sections. You already set the overall layout in the main rule, but you can adjust the placement in the child rules.

One option is the grid-column property, which is shorthand for grid-column-start and grid-column-end. The grid-column property tells the grid item which grid line to start and end at.

Create a .heading rule and set the grid-column property to 2 / 3. This will tell the .heading element to start at grid line 2 and end at grid line 3.

Step 38
For additional control over the layout of your content, you can have a CSS Grid within a CSS Grid.

Set the display property of your .heading selector to grid.

Step 39
Now you can style the content of the .heading element with CSS Grid.

The CSS repeat() function is used to repeat a value, rather than writing it out manually, and is helpful for grid layouts. For example, setting the grid-template-columns property to repeat(20, 200px) would create 20 columns each 200px wide.

Give your .heading element a grid-template-columns property set to repeat(2, 1fr) to create two columns of equal width.

Step 41
Remember that the grid-column property determines which columns an element starts and ends at. There may be times where you are unsure of how many columns your grid will have, but you want an element to stop at the last column. To do this, you can use -1 for the end column.

Create a .hero selector and give it a grid-column property set to 1 / -1. This will tell the element to span the full width of the grid.

Step 44
Create an img selector and give it a width property set to 100%, and an object-fit property set to cover.

The object-fit property tells the browser how to position the element within its container. In this case, cover will set the image to fill the container, cropping as needed to avoid changing the aspect ratio.

Step 51
The default settings for CSS Grid will create additional rows as needed, unlike Flexbox. Give the .social-icons selector a grid-template-columns property set to repeat(5, 1fr) to arrange the icons in a single row.

Step 52
If you wanted to add more social icons, but keep them on the same row, you would need to update grid-template-columns to create additional columns. As an alternative, you can use the grid-auto-flow property.

This property takes either row or column as the first value, with an optional second value of dense. grid-auto-flow uses an auto-placement algorithm to adjust the grid layout. Setting it to column will tell the algorithm to create new columns for content as needed. The dense value allows the algorithm to backtrack and fill holes in the grid with smaller items, which can result in items appearing out of order.

For your .social-icons selector, set the grid-auto-flow property to column.

Step 53
Now the auto-placement algorithm will kick in when you add a new icon element. However, the algorithm defaults the new column width to be auto, which will not match your current columns.

You can override this with the grid-auto-columns property. Give the .social-icons selector a grid-auto-columns property set to 1fr.

Step 54
Much like Flexbox, with CSS Grid you can align the content of grid items with align-items and justify-items. align-items will align child elements along the column axis, and justify-items will align child elements along the row axis.

Give the .social-icons selector an align-items property set to center.

Step 56
Your .text element is not a CSS Grid, but you can create columns within an element without using Grid by using the column-width property.

Give your .text selector a column-width property set to 25rem.

Step 57
Magazines often use justified text in their printed content to structure their layout and control the flow of their content. While this works in printed form, justified text on websites can be an accessibility concern, for example presenting challenges for folks with dyslexia.

To make your project look like a printed magazine, give the .text selector a text-align property set to justify.

Step 58
The ::first-letter pseudo-selector allows you to target the first letter in the text content of an element.

Create a .first-paragraph::first-letter selector and set the font-size property to 6rem. Also give it a color property set to orangered to make it stand out.

float
The float CSS property places an element on the left or right side of its container, allowing text and inline elements to wrap around it. The element is removed from the normal flow of the page, though still remaining a part of the flow

Step 59
The other text has been shifted out of place. Move it into position by giving the .first-paragraph::first-letter selector a float property set to left and a margin-right property set to 1rem.

Step 61
To give the hr a color, you need to adjust the border property. Give the hr selector a border property set to 1px solid rgba(120, 120, 120, 0.6).

Step 64
A quote is not really a quote without proper quotation marks. You can add these with CSS pseudo selectors.

Create a .quote::before selector and set the content property to " with a space following it.

Also, create a .quote::after selector and set the content property to " with a space preceding it.

Step 66
You will need to have a column for text and a column for images. Give the .text-with-images selector a grid-template-columns property set to 1fr 2fr. Also set the column-gap property to 3rem to provide more spacing between the columns.

Step 73
The images should be within a two column, three row layout.

Give the .image-wrapper selector a grid-template-columns property set to 2fr 1fr and a grid-template-rows property set to repeat(3, min-content). This will give our grid rows that adjust in height based on the content, but columns that remain a fixed width based on the container.

Step 74
The gap property is a shorthand way to set the value of column-gap and row-gap at the same time. If given one value, it sets the column-gap and row-gap both to that value. If given two values, it sets the row-gap to the first value and the column-gap to the second.

Give the .image-wrapper selector a gap property set to 2rem.

Step 75
The place-items property can be used to set the align-items and justify-items values at the same time. The place-items property takes one or two values. If one value is provided, it is used for both the align-items and justify-items properties. If two values are provided, the first value is used for the align-items property and the second value is used for the justify-items property.

Give the .image-wrapper selector a place-items property set to center.

Step 76
Create an .image-1, .image-3 rule and give it a grid-column property set to 1 / -1. This will allow the first and third images to span the full width of the grid.

Step 77
Now that the magazine layout is finished, you need to make it responsive.

Start with a @media query for only screen with a max-width of 720px. Inside, create an .image-wrapper selector and give it a grid-template-columns property of 1fr.

This will collapse the three images into one column on smaller screens.

Step 78
Create another @media query for only screen with a max-width of 600px. Within, create a .text-with-images rule and give it a grid-template-columns property of 1fr.

This will collapse your bottom text area into a single column on smaller screens.