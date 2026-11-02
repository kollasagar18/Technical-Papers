d# Browser Rendering – How Does a Browser Render HTML, CSS, and JavaScript into the DOM?

## Introduction

Whenever we open a website in a browser like Chrome or Firefox, we can see text, images, buttons, colors, and different layouts. But have you ever thought about how all these things appear on the screen? Actually, the browser performs several steps before displaying a webpage. It takes HTML, CSS, and JavaScript files, processes them, and converts them into something that we can see and interact with. This complete process is called browser rendering.

## 1. HTML to DOM

HTML is used to create the basic structure of a webpage. When we open a website, the browser first reads the HTML code from top to bottom. It understands the tags and creates a tree-like structure called the DOM (Document Object Model).

For example:

```html
<html>
<body>
    <h1>Hello World</h1>
    <p>Welcome to my website.</p>
</body>
</html>
```

Here, the browser reads the HTML elements and creates a DOM tree. Each HTML element becomes a node in that tree. JavaScript can use this DOM to access and change webpage elements.

## 2. CSS to CSSOM

HTML only provides the structure, but CSS makes the webpage look better. It is used to add colors, fonts, sizes, spacing, and layouts.

When the browser reads CSS files, it understands the styling rules and creates a structure called CSSOM (CSS Object Model). The browser uses this information to decide how each HTML element should look.

For example:

```css
h1 {
    color: blue;
    font-size: 30px;
}
```

This code changes the heading color to blue and sets its font size to 30 pixels.

## 3. JavaScript Execution

JavaScript is used to make websites interactive. For example, when we click a button, submit a form, or change some content on a webpage, JavaScript helps perform those actions.

The browser uses a JavaScript engine to execute JavaScript code. When JavaScript changes an HTML element, the browser updates the DOM.

For example:

```javascript
document.querySelector("h1").textContent = "Welcome!";
```

Here, JavaScript selects the heading and changes its text from "Hello World" to "Welcome!".

## 4. Render Tree Creation

After processing HTML and CSS, the browser combines the DOM and CSSOM information to create something called the Render Tree.

The Render Tree contains the visible elements of the webpage along with their styles. For example, an element with `display: none` will not be included in the Render Tree because it is not visible on the screen.

## 5. Layout Process

After creating the Render Tree, the browser needs to decide where each element should appear on the screen. It calculates the width, height, position, margin, and padding of every visible element.

This step is called Layout. If we change the size or position of an element, the browser may need to calculate the layout again.

## 6. Painting and Compositing

Once the layout is completed, the browser starts painting the webpage. In this step, it draws the text, images, backgrounds, borders, and other visual elements.

After painting, the browser combines different layers through a process called Compositing. Finally, the completed webpage appears on our screen.

## Conclusion

Browser rendering happens every time we open or interact with a website. First, the browser processes HTML and creates the DOM. Then it reads CSS and creates the CSSOM. JavaScript can also change the webpage whenever needed. After that, the browser creates the Render Tree, calculates the layout, paints the elements, and combines everything using compositing. By understanding this process, we can learn how browsers work and how to build websites that load faster and perform better.

