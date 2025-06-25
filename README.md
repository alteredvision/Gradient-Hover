A sleek, modern button component with captivating animated gradient border effects on hover.

Features:

🎨 Customizable color schemes

⚡ Smooth CSS-powered animations

📱 Fully responsive

🛠 No external dependencies

🎛 Easy-to-modify animation parameters
__________________________________________________________________________________

Installation
Option 1: Direct Copy
1. Copy the following code into your project:
```html
<script>
if (CSS && CSS.registerProperty) {
    CSS.registerProperty({
        name: '--border-angle',
        syntax: '<angle>',
        inherits: false,
        initialValue: '0deg'
    });
}
</script>

<style>
    .animated-border-btn {
        position: relative;
        background: #2e2e2e;
        color: #aaaaaa;
        padding: 0.5rem 1rem;
        margin: 1rem;
        border-radius: 2rem;
        font-weight: 600;
        border: 2px solid transparent;
        cursor: pointer;
        transition: all 0.2s ease;
    }

    .animated-border-btn:hover {
        background: 
            linear-gradient(#171717, #171717) padding-box,
            conic-gradient(
                from var(--border-angle, 0deg),
                #171717 80%,
                #f16363 86%,
                #fca5a5 90%,
                #f16363 94%,
                #171717 100%
            ) border-box;
        animation: border-spin 2s linear infinite;
        color: whitesmoke;
    }
    
    @keyframes border-spin {
        to {
            --border-angle: 360deg;
        }
    }
</style>
```
Usage
Add the button to your HTML:
```HTML
<button class="animated-border-btn">
    Hover Me
</button>
```
2. Customize the colors by editing the conic-gradient values in the CSS.

Customization
Change Colors
Modify the gradient colors in the conic-gradient:

```CSS
conic-gradient(
    from var(--border-angle, 0deg),
    #171717 80%,
    #6366f1 86%,  /* Change accent color */
    #a5b4fc 90%,  /* Change highlight color */
    #6366f1 94%,
    #171717 100%
)
```
Adjust Animation Speed
```CSS
.animated-border-btn:hover {
    animation: border-spin 1.5s linear infinite; /* Faster animation */
}
```
Change Border Thickness
```CSS
.animated-border-btn {
    border: 3px solid transparent; /* Thicker border */
}
```
Browser Support
Browser	Support
Chrome	✅ 90+
Firefox	✅ 89+
Safari	✅ 15+
Edge	✅ 90+
Note: For older browsers, consider adding a fallback solid border.

License
MIT License - Free for personal and commercial use.
