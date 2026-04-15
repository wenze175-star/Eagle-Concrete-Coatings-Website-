# Eagle Concrete Coatings — Website

## Folder Structure

```
eagle-concrete/
├── index.html          ← Home page
├── about.html          ← About Colton
├── services.html       ← Services (Garage, Patio, Basement, Commercial)
├── gallery.html        ← Gallery + Before/After sliders
├── contact.html        ← Contact + Quote form
├── css/
│   └── style.css       ← All styles (colors, fonts, layout)
├── js/
│   └── main.js         ← Navigation, sliders, gallery filter, FAQ
├── images/             ← PUT ALL YOUR PHOTOS HERE
└── README.md           ← This file
```

---

## Setting Up in VS Code

1. Open VS Code
2. File → Open Folder → Select the `eagle-concrete` folder
3. Install the **Live Server** extension (search "Live Server" in Extensions)
4. Right-click `index.html` → "Open with Live Server"
5. Your site will open in the browser at http://127.0.0.1:5500

---

## Adding Your Photos

Place all photos inside the `images/` folder. Name them exactly as shown below:

### Hero Background
- `images/hero-bg.jpg` — A wide garage/floor shot for the home page hero

### Before / After Photos (pairs)
- `images/before-01.jpg` + `images/after-01.jpg`
- `images/before-02.jpg` + `images/after-02.jpg`
- `images/before-03.jpg` + `images/after-03.jpg`
- `images/before-04.jpg` + `images/after-04.jpg`

### Gallery Project Photos
- `images/project-01.jpg` through `images/project-09.jpg`
  (Add more by duplicating the gallery-item blocks in gallery.html)

### Service Page Photos (optional but recommended)
- `images/service-garage.jpg`
- `images/service-patio.jpg`
- `images/service-basement.jpg`
- `images/service-commercial.jpg`

### Colton's Photo (About page)
- `images/colton-kunkel.jpg`
  Then in about.html, replace the gray placeholder div with:
  `<img src="images/colton-kunkel.jpg" alt="Colton Kunkel - Eagle Concrete Coatings" />`

### Color Chips (optional - pulls from eagleconcretecoatings.com)
If you want local copies, save the color images from your current site as:
- `images/colors/tidal_wave.png`
- `images/colors/creekbed.png`
- (etc. — names match the current site filenames)

---

## Activating the Contact Form

The contact form uses **Formspree** — free, no server needed.

1. Go to https://formspree.io
2. Sign up for a free account
3. Click "New Form" and follow the setup
4. Copy your form ID (looks like: `xyzabcde`)
5. Open `contact.html`
6. Find this line:
   `action="https://formspree.io/f/YOUR_FORM_ID"`
7. Replace `YOUR_FORM_ID` with your actual form ID

Submissions will be emailed directly to you.

---

## Customizing Colors

All brand colors are defined at the top of `css/style.css`:

```css
:root {
  --navy: #0D1F3C;
  --navy-light: #1B3A6B;
  --red: #C8102E;
  --red-dark: #a50d26;
  --white: #ffffff;
}
```

Change any of these and the entire site updates automatically.

---

## Adding More Gallery Photos

In `gallery.html`, find the `.gallery-grid` section and copy/paste this block:

```html
<div class="gallery-item" data-category="residential garage">
  <img src="images/project-10.jpg" alt="Description" />
  <div class="gallery-item-overlay">
    <span class="gallery-item-label">Residential</span>
    <span class="gallery-city">Lakeville, MN</span>
  </div>
</div>
```

Change `data-category` to one of: `residential`, `commercial`, `garage`, `outdoor`
(Can have multiple, space-separated)

---

## SEO Tips

- Each page has a unique `<title>` and `<meta name="description">` — keep these updated
- Add your Google Business profile link in the footer
- Once live, submit your sitemap to Google Search Console
- Consider adding schema markup (ask for help with this if needed)

---

## Going Live

When you're ready to put it online:
- **Recommended hosts:** Netlify (free), Cloudflare Pages (free), or GoDaddy/Bluehost
- Just upload the entire `eagle-concrete` folder
- Point your domain to the host

Questions? Everything was built to be easy to edit directly in VS Code.
