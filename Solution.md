## Assignment 6.3 — Overflow & Layout Fixing

### 1. `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Overflow</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>CSS Overflow Examples</h1>

    <h2>Overflow: Visible</h2>
    <div class="box visible">
        This is sample content. This text overflows the fixed-size container and remains visible outside it.
    </div>

    <h2>Overflow: Hidden</h2>
    <div class="box hidden">
        This is sample content. Extra text is hidden when it exceeds the container height.
    </div>

    <h2>Overflow: Auto</h2>
    <div class="box auto">
        This is sample content. Extra text appears through scrolling when required. 
        More content is added here to demonstrate overflow behavior.
        More content is added here to demonstrate overflow behavior.
    </div>

    <h2>Overflow: Scroll</h2>
    <div class="box scroll">
        This is sample content. Scroll to read the remaining text.
        More content is added here.
        More content is added here.
    </div>

    <h2>Fixed Layout</h2>
    <div class="fixed">
        This container uses overflow auto to prevent content from breaking the layout.
        Extra content can be viewed using the scrollbar.
    </div>
</body>
</html>
```

### 2. `style.css`

```css
body {
    font-family: Arial, sans-serif;
    margin: 20px;
    background: #f0f4f8;
}

.box, .fixed {
    width: 300px;
    height: 100px;
    border: 2px solid navy;
    padding: 10px;
    margin-bottom: 30px;
    background: lightblue;
}

.visible {
    overflow: visible;
}

.hidden {
    overflow: hidden;
}

.auto {
    overflow: auto;
}

.scroll {
    overflow: scroll;
}

.fixed {
    max-width: 100%;
    box-sizing: border-box;
    overflow: auto;
    background: lightyellow;
}
```

### 3. Explanation

- `visible`: Overflowing content remains visible.
- `hidden`: Extra content is clipped.
- `auto`: Scrollbars appear when needed.
- `scroll`: Scrollbars are provided.
- `overflow: auto`: Helps prevent content from breaking the layout.

**Submission:** Open the page using Live Server, test each container, and take a screenshot showing the overflow examples and fixed layout.