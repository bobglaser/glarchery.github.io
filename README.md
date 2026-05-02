# Precision Archery Club Website

A Hugo-based website for an archery club featuring event calendars, coach biographies, and mission statement.

## Features

- **Homepage**: Mission statement and club overview
- **Event Calendar**: Upcoming tournaments, workshops, and regular activities
- **Coach Profiles**: Detailed biographies of coaching staff
- **About Page**: Club history and facilities information
- **Contact Information**: Hours, location, and contact details

## Getting Started

### Prerequisites
- Hugo (static site generator)
- Git

### Installation
1. Clone this repository
2. Navigate to the project directory
3. Run the development server:
   ```bash
   hugo server --buildDrafts
   ```
4. Open your browser to `http://localhost:1313`

### Building for Production
```bash
hugo --minify
```
The built site will be in the `public/` directory.

## Content Management

### Adding Events
Create new event files in `content/events/`:
```bash
hugo new content/events/new-event.md
```

Include event metadata in the front matter:
```yaml
---
title: "Event Name"
date: 2024-12-14
event_date: "2025-01-15"
event_time: "10:00 AM - 2:00 PM"
location: "Indoor Range"
registration_deadline: "2025-01-12"
---
```

### Adding Coach Profiles
Create new coach files in `content/coaches/`:
```bash
hugo new content/coaches/coach-name.md
```

### Customizing Content
- Edit `content/_index.md` for homepage content
- Modify `hugo.toml` for site configuration
- Add images to `static/images/` directory

## Site Structure

```
archery-club/
├── content/
│   ├── _index.md          # Homepage
│   ├── about.md           # About page
│   ├── contact.md         # Contact information
│   ├── coaches/           # Coach profiles
│   │   ├── _index.md
│   │   ├── sarah-martinez.md
│   │   ├── mike-thompson.md
│   │   └── jenny-kim.md
│   └── events/            # Event calendar
│       ├── _index.md
│       ├── winter-indoor-championship.md
│       ├── beginner-workshop.md
│       └── spring-3d-tournament.md
├── static/
│   └── images/            # Site images
├── themes/
│   └── basic/             # Custom theme
└── hugo.toml              # Site configuration
```

## Customization

### Adding Images
Place images in `static/images/` and reference them in content:
```markdown
![Alt text](/images/your-image.jpg)
```

### Styling
Modify the CSS in `themes/basic/layouts/_default/baseof.html` to customize the appearance.

### Navigation
Update the menu in `hugo.toml`:
```toml
[[menu.main]]
  name = "New Page"
  url = "/new-page/"
  weight = 6
```

## Deployment

The site can be deployed to any static hosting service:
- Netlify
- Vercel
- GitHub Pages
- AWS S3
- Traditional web hosting

Simply upload the contents of the `public/` directory after running `hugo --minify`.