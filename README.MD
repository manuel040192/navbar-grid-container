I have three components in a navbar, there are navlinks on the left, a logo on the center and a component that I don't want to be visible on the right (the component has a white-colored text on a white background) and that I created so that there would be three components with which I could have, using "display: flex" and "justify-content: space between" on the component that contains those three components, the navlinks on the left, the logo on the center and nothing on the right. The problem was when I added more padding on the left of the navlinks so that they could have a proper distance from the farthest point on the left of the navbar, the logo that I wanted to be on the center moved to the right along with the navlinks.

This is how the navbar looked:

https://i.stack.imgur.com/L9nXl.png

This is how it could look when "padding-left: 20px" and "padding-right: 20px" were removed from NavMenu, the component that contains the navlinks (the logo didn't move to the navbar's center):

https://i.stack.imgur.com/jUQ9O.png

This is how it could look when the paddings were removed and the color of the text of the component that's on the right was set to black:

https://i.stack.imgur.com/9zyZW.png

And I wanted the navbar components to be evenly-spaced similarly to this (but unlike this image I wanted: 1) An invisible component to be on the right because that's the only way I know for the logo to be on the center and the navlinks on the left, and 2) The navlinks to be 30px away from the farthest point on the left of the navbar.):

https://i.stack.imgur.com/FWTkr.png

I had the following questions: How could I change the navlinks' paddings without the logo moving to the right? And how could I make the logo to be at the center of the navbar?

I found the solutions to the logo moving when the navlinks' paddings were changed and the logo not being on the center in the code of a website's navbar, and a part of that code that I used to find those solutions can be found in the file Navbar.css.

The previous code is in Navbar_flex_container.js and the current code is in Navbar_grid_container.js.

The following are two differences between the code in Navbar.css and the code in Navbar_grid_container.js:

- In the CSS of the container of the three components I talked aboud, I used "grid-template-rows: 80px;" instead of "grid-template-rows: 100px;". The height of the navbar is of 80px, and grid-template-rows should be of 80px as well for the navlinks and the logo to be vertically centered.

- NavMenu doesn't have the CSS declaration "justify-content: space-around;", and instead, NavMenu's a has "padding-left: 30px;" and "padding-right: 15px;".
