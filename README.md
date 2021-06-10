# etch-a-sketch

This project is based on the toy "Etch A Sketch" and was made with HTML, CSS, and JavaScript.  
It is nothing more than a "screen" and a button to reset the drawing. The "screen" is made of a container div containing a grid of square divs implemented with **CSS Grid**. The divs of the grid change color as the user hovers the cursor over them, creating a pixelated trail. That's it. 

The script has 3 functions:

- `changeColor()`
- `setChildren()`
- `setSquares()`

An event listener is added to all grid divs with the `changeColor()` function as callback and a 'mouseenter' event. So, when the user hovers the cursor over a div, `changeColor()` is called and the background color changes to a random color. After the first pass, each pass reduces the lightness of the div by 10%, so that after 10 passes it is completely black. This functionality was implemented using a **custom data attribute (data-*)** called `data-lightness` to keep track of the current lightness of a particular div.

`setChildren()` receives the number of children divs as an argument. It first removes the current children, creates and appends the new ones and adds the event listener.

`setSquares()` prompts a popup asking for how many squares per side to make the new grid. The CSS `grid` property of the container is then updated accordingly.

---

From The Odin Project's [curriculum](https://www.theodinproject.com/courses/web-development-101/lessons/etch-a-sketch-project).
