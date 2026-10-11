# Animated Social Links

A small front-end project made with **HTML and CSS only**: a row of round social media buttons. Each button shows the network's icon at first. On hover (or keyboard focus) it expands into a pill, the icon disappears, and the network's name appears over a matching **gradient** background.

## Features

- Pure HTML and CSS, no JavaScript
- Smooth expand animation with CSS transitions
- One custom gradient per social network
- Works with keyboard navigation (`:focus-within`)
- Easy to customize through CSS variables

## Built With

- HTML5
- CSS3 (Flexbox, custom properties, pseudo-elements)
- [Bootstrap Icons](https://icons.getbootstrap.com/)
- [Google Fonts - Outfit](https://fonts.google.com/specimen/Outfit)

## Project Structure

```
animated-social-links/
├── index.html   # Page markup and the list of social links
├── styles.css   # All styles and animations
└── README.md
```

## Usage

Open `index.html` in your browser. An internet connection is needed to load the icons and the font from their CDNs.

## Customization

### Change a link

In `index.html`, replace the `href="#"` of the network you want:

```html
<a href="https://www.instagram.com/your-profile" aria-label="Instagram"></a>
```

### Change gradient colors

Each `<li>` defines two CSS variables: `--cor1` (start color, also the icon color) and `--cor2` (end color).

```html
<li style="--cor1: #f09433; --cor2: #bc1888">
```

### Add a new network

Copy one `<li>` block, change the colors, the link, the icon class (see the [Bootstrap Icons list](https://icons.getbootstrap.com/)) and the name:

```html
<li style="--cor1: #1da1f2; --cor2: #0d6efd">
  <a href="#" aria-label="Twitter"></a>
  <span class="icon"><i class="bi bi-twitter"></i></span>
  <span class="text">Twitter</span>
</li>
```

### Default gradients

| Network   | Start color | End color |
|-----------|-------------|-----------|
| Instagram | `#f09433`   | `#bc1888` |
| YouTube   | `#ff3b3b`   | `#b00000` |
| LinkedIn  | `#0a66c2`   | `#00a0dc` |
| GitHub    | `#2b3137`   | `#6e5494` |

### Other adjustments (in `styles.css`)

- Button size: `width` and `height` of `ul li`
- Expanded width: `width` of `ul li:hover`
- Space between buttons: `gap` of `ul`
- Animation speed: the `transition` values

projet developed by https://www.linkedin.com/in/paulotraveler/