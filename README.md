# Portfolio Showcase

A modern, interactive portfolio website showcasing my systems programming, physics engines, databases, and web development projects.

**Live Site:** [View Portfolio](https://francis-chung.github.io/portfolio-showcase) *(once deployed)*

## Features

- **Dynamic Project Filtering**: Browse projects by category (all, systems, physics, web, quantum)
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Dark/Light Theme**: Automatically adapts to system preferences with manual override support
- **Interactive Animations**: Smooth transitions and scroll-triggered effects (respects `prefers-reduced-motion`)
- **Zero Dependencies**: Built with vanilla HTML, CSS, and JavaScript for maximum performance
- **Accessible**: Keyboard navigation, semantic HTML, and ARIA labels throughout

## Design Philosophy

The portfolio uses a **deep technical aesthetic** with an electric accent palette, inspired by terminal interfaces and development tools. The design emphasizes:

- **Asymmetric grid layouts** with floating project cards
- **Typography hierarchy** using Space Grotesk for headings and Inter for body text
- **Motion design** that's purposeful but respectful of accessibility preferences
- **Real content** showcasing actual projects with live demos and GitHub links

## Projects Featured

### Systems Programming
- **KV-Database**: Rust-based in-memory key-value store with WAL and skip list implementation
- **Omnibus**: Real-time data bus for rocket telemetry
- **Universe**: Monorepo for embedded systems and deployable applications

### Physics Engines
- **ephys**: C++ 2D rigidbody engine with WebAssembly demo
- **fysics**: TypeScript physics engine with React visualization

### Quantum Computing
- **qlang**: Symbolic expression engine with quantum compilation (Grover, QAOA)

### Web Applications
- **Elegancy Platform**: Company website and strategy research platform
- **Omnibus DAQms**: Real-time monitoring dashboard with WebSocket streaming
- **Planit**: Gamified productivity and task management app

## Local Development

No build step required. Simply open `index.html` in a modern browser:

```bash
# Clone the repository
git clone https://github.com/francis-chung/portfolio-showcase.git
cd portfolio-showcase

# Serve locally (choose one)
python -m http.server 8000
# or
npx serve
# or just open index.html directly
```

Then visit `http://localhost:8000`

## Deployment

### GitHub Pages

1. Push to GitHub
2. Go to repository Settings → Pages
3. Select branch `main` and folder `/` (root)
4. Save and wait for deployment

### Netlify/Vercel

Simply drag the `portfolio-showcase` folder into their web interface, or connect the GitHub repository for automatic deployments.

### Custom Server

Upload `index.html` to any static web host. No server-side processing required.

## Customization

### Updating Projects

Projects are defined in the HTML within the `.projects-grid` section. Each project card follows this structure:

```html
<article class="project-card" data-category="systems web">
  <div class="project-header">
    <div class="project-icon">🗄️</div>
    <div class="project-links">
      <a href="GITHUB_URL" class="icon-link">⚡</a>
    </div>
  </div>
  <h3 class="project-title">Project Name</h3>
  <p class="project-description">Description...</p>
  <div class="project-tags">
    <span class="tag">tag1</span>
  </div>
  <div class="project-status">
    <span class="status-dot"></span>
    <span>Status text</span>
  </div>
</article>
```

### Color Scheme

Colors are defined as CSS custom properties in the `:root` selector at the top of the `<style>` block:

```css
:root {
  --bg-primary: #0a0e14;
  --accent-electric: #00d9ff;
  /* ... */
}
```

Modify these values to change the entire color scheme. Both light and dark themes are defined.

### Typography

Fonts are loaded from Google Fonts. To change typefaces, update the `<link>` tag and the CSS variables:

```css
--font-display: 'Space Grotesk', system-ui, sans-serif;
--font-body: 'Inter', system-ui, sans-serif;
```

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari 14+, Chrome Android 90+)

The site uses modern CSS features like `clamp()`, CSS Grid, custom properties, and `text-wrap: balance`. Fallbacks are provided where appropriate.

## Performance

- **No build step**: Direct HTML/CSS/JS for instant loading
- **Font optimization**: Uses `font-display: swap` for Google Fonts
- **Minimal JavaScript**: Only for filtering and smooth scroll interactions
- **Optimized animations**: Hardware-accelerated transforms, respects `prefers-reduced-motion`

## License

MIT License - feel free to use this as a template for your own portfolio. Attribution appreciated but not required.

## Contact

**Francis Chung**
- GitHub: [@francis-chung](https://github.com/francis-chung)
- Email: francis.chung@example.com

---

Built with passion for systems and craft. No frameworks, just HTML, CSS, and JavaScript.
