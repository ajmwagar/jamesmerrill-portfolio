# James Merrill Portfolio

Personal portfolio and blog for James Merrill, COO at Future Present Labs.

🔗 **Live Site**: https://jamesmerrill.dev

## About

This is a personal website built with [Hugo](https://gohugo.io/) using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. It includes:

- Personal blog with operations and manufacturing insights
- About page with professional background
- Contact information and speaking inquiries
- RSS feed for blog posts
- Dark/light mode toggle
- Mobile-responsive design

## Local Development

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version, v0.112.0 or later)
- [Git](https://git-scm.com/)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/jamesmerrill/jamesmerrill-portfolio.git
cd jamesmerrill-portfolio
```

2. Initialize and update the theme submodule:
```bash
git submodule update --init --recursive
```

3. Start the development server:
```bash
hugo server -D
```

4. Open http://localhost:1313 in your browser

### Adding Content

**New Blog Post:**
```bash
hugo new content posts/my-post-title.md
```

Then edit `content/posts/my-post-title.md` with your content.

**Front Matter Template:**
```yaml
---
title: "Your Post Title"
date: 2026-02-02T12:00:00-08:00
draft: false
tags: ["tag1", "tag2"]
categories: ["category"]
author: "James Merrill"
---
```

## Deployment

This site is automatically deployed to [Netlify](https://netlify.com) on every push to the `main` branch.

### Build Settings (Netlify)

- **Build command**: `hugo --gc --minify`
- **Publish directory**: `public`
- **Hugo version**: 0.120.0 (or specify in `netlify.toml`)

### Manual Deployment

If you need to deploy manually:

```bash
# Build the site
hugo --gc --minify

# The site is now in the public/ directory
# Upload to your hosting provider
```

## Customization

### Profile Image

Add your profile photo to `static/images/profile.jpg`. The recommended size is 400x400px.

### Social Links

Update social links in `hugo.toml` under `[params.socialIcons]`.

### Colors & Theme

The site supports dark and light modes. To customize:

1. Modify `assets/css/extended/custom.css` (create if it doesn't exist)
2. Add your custom CSS overrides

### Content Updates

**About Page**: Edit `content/about/index.md`

**Contact Page**: Edit `content/contact/index.md`

**Homepage**: Configure in `hugo.toml` under `[params.profileMode]`

## Site Structure

```
.
├── archetypes/          # Content templates
├── assets/             # CSS, JS, images
├── content/            # Site content
│   ├── about/         # About page
│   ├── contact/       # Contact page
│   └── posts/         # Blog posts
├── data/              # Data files
├── layouts/           # HTML templates
├── static/            # Static files (images, etc.)
├── themes/            # Hugo themes
│   └── PaperMod/      # Current theme
├── hugo.toml          # Site configuration
├── netlify.toml       # Netlify configuration
└── README.md          # This file
```

## Content Guidelines

### Blog Posts

- Use clear, descriptive titles
- Include relevant tags for discoverability
- Add a brief excerpt in the front matter
- Use markdown formatting for readability
- Include images in `static/images/posts/`

### Writing Style

- Professional but approachable
- Data-driven when making claims
- Link to sources when citing research
- Use headers to break up long content

## SEO

The PaperMod theme includes built-in SEO features:

- Open Graph tags
- Twitter Cards
- Structured data (JSON-LD)
- RSS feeds
- Sitemap generation

Customize SEO settings in `hugo.toml`:

```toml
[params]
  description = "Your site description"
  author = "James Merrill"
  images = ["images/profile.jpg"]
```

## Performance

The site is optimized for performance:

- Minified HTML/CSS/JS
- Lazy-loaded images
- Responsive images
- Fast build times
- Core Web Vitals optimized

Check performance with Lighthouse in Chrome DevTools.

## License

Content is © James Merrill. The Hugo theme (PaperMod) is licensed under the MIT License.

## Support

For technical issues with this site, contact:
- Email: james@futurepresentlabs.com
- GitHub Issues: [github.com/jamesmerrill/jamesmerrill-portfolio/issues](https://github.com/jamesmerrill/jamesmerrill-portfolio/issues)

---

Built with ❤️ and [Hugo](https://gohugo.io/)
