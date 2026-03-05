# NeoPower Energy — B2B Clean Energy Website

## File Structure

```
neopower-site/
├── index.html              ← Homepage
├── css/
│   └── style.css           ← All styles (global design system)
├── js/
│   └── main.js             ← All interactivity
├── images/                 ← Add your product & factory photos here
│   └── (add photos here)
└── pages/
    ├── products.html        ← Product catalog with specs & quote forms
    ├── about.html           ← Company story, factory photos, certifications
    └── contact.html         ← Contact form, company info, FAQ
```

## Customization Checklist

### 🏢 Company Information
Replace all placeholder content throughout the pages:
- **Company name**: NeoPower Energy Co., Ltd.
- **Phone**: +86 755 1234 5678
- **WhatsApp**: +86 138 0000 0000
- **Email**: sales@neopowerenergy.com
- **Address**: Building A, Longhua Innovation Park, Longhua District, Shenzhen 518109

### 📸 Photos to Add (images/ folder)
- `factory-exterior.jpg` — Factory building exterior
- `production-line.jpg` — SMT/assembly line
- `qc-lab.jpg` — Quality control laboratory
- `warehouse.jpg` — Warehouse or shipping area
- `rnd-center.jpg` — R&D department
- `showroom.jpg` — Product showroom
- Product photos for each of the 5 product lines

To add photos in `about.html`, replace the `.photo-slot` divs:
```html
<div class="photo-slot">
  <img src="../images/factory-exterior.jpg" alt="Factory exterior" />
</div>
```

To add product photos in `products.html`, replace the `.product-detail-visual` SVG:
```html
<div class="product-detail-visual">
  <img src="../images/power-station.jpg" alt="Portable Power Station" style="width:100%;height:100%;object-fit:cover;" />
</div>
```

### 📜 Certificates
In `about.html`, find the certificate placeholder comment and add:
```html
<img src="../images/ce-certificate.jpg" alt="CE Certificate" style="width:100%; border-radius:8px;" />
```

### 🗺️ Google Maps
In `contact.html`, replace the `.map-placeholder` div with:
```html
<iframe
  src="https://www.google.com/maps/embed?pb=YOUR_MAP_EMBED_URL"
  width="100%" height="260"
  style="border:0; border-radius:12px;"
  allowfullscreen loading="lazy">
</iframe>
```

### 📧 Form Backend
The contact forms currently show a success toast (frontend only).
To make them actually send emails, connect a backend service:
- **Formspree**: Change `<form data-ajax>` to `<form action="https://formspree.io/f/YOUR_ID" method="POST">`
- **EmailJS**: Initialize in main.js with your service credentials
- **Custom backend**: Send POST data from the `data-ajax` handler in main.js

### 🎨 Branding Colors
Edit CSS variables in `css/style.css` (`:root` section):
```css
--teal:  #00d4aa;   /* Primary accent — change to your brand color */
--green: #1aff8c;   /* Secondary accent */
--navy:  #0a1628;   /* Background dark */
```

### 👥 Team Members
In `about.html`, update the team cards with real names, roles, and photos.

## Technology
- Pure HTML5, CSS3, Vanilla JavaScript
- Google Fonts: Rajdhani (headings) + DM Sans (body)
- Fully responsive (mobile/tablet/desktop)
- No frameworks or build tools required — open index.html directly in a browser

## Browser Support
Chrome 80+, Firefox 75+, Safari 13+, Edge 80+
