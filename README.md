# EzHairr Website

Private, bilingual luxury hair studio — Raleigh, NC.

## Project Structure

```
ezhairr/
├── index.html        # Homepage
├── services.html     # Services page
├── about.html        # About page
├── contact.html      # Contact page
├── css/
│   └── style.css     # All styles
├── js/
│   └── main.js       # Nav, scroll reveal, form
└── images/           # Drop Ezequiel's photos here
```

## Adding Photos

Each photo placeholder is labeled in the HTML. Search for `img-placeholder` in any HTML file to find where to swap in real images. Replace the placeholder divs with:

```html
<img src="images/your-photo.jpg" alt="Description of photo" />
```

Recommended photos to have ready:
- Hero photo (full-height portrait or studio shot)
- Color service photo
- Extensions service photo
- Cuts/styling service photo
- Ezequiel portrait (homepage split + about page)
- Ezequiel full portrait (about page)

## Deploying to GitHub + Vercel

### Step 1 — GitHub

1. Create a new repository at github.com (e.g. `ezhairr-website`)
2. In your terminal:

```bash
cd path/to/ezhairr
git init
git add .
git commit -m "Initial EzHairr website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ezhairr-website.git
git push -u origin main
```

### Step 2 — Vercel

1. Go to vercel.com and sign in with GitHub
2. Click "Add New Project"
3. Import your `ezhairr-website` repository
4. Framework Preset: select **Other** (it's a plain HTML site)
5. Leave all defaults and click **Deploy**
6. Vercel will give you a live URL instantly

### Step 3 — Custom Domain (ezhairr.com)

1. In your Vercel project, go to Settings > Domains
2. Add `ezhairr.com` and `www.ezhairr.com`
3. Update your domain's DNS records to point to Vercel (they'll show you exactly what to add)

### Future Updates

Any `git push` to `main` automatically redeploys via Vercel.

## Booking Link

The "Book Now" / "Reserve a Session" buttons currently link to:
`https://ezhairr.com/request-appointment`

Update this URL if Ezequiel's booking system changes (e.g. Vagaro, StyleSeat, Square, etc.).

## Contact Form

The contact form currently shows a "Message Sent" confirmation on submit but does not actually send emails. To wire it up for real, options include:
- **Formspree** (free tier, just add `action="https://formspree.io/f/YOUR_ID"` to the form)
- **Netlify Forms** (if moving to Netlify instead of Vercel)
- A backend/serverless function
