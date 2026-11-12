# Scooter Bennett Septic website

Static site built with Eleventy, hosted on Netlify. Domain: scooterbennettseptic.com.

## Pages
Home (/), Services (/services/, one section per service), About (/about/), Service Areas (/service-areas/), Contact (/contact/), plus Thank You, Privacy and 404.

## Where to change things
- Phone, email, FL DOH license number, Facebook, GA4 ID: `src/_data/site.json`
- Header and menu: `src/_includes/header.njk`
- Footer and mobile Call Now bar: `src/_includes/footer.njk` (also holds email, hours placeholder and FL DOH license number (set in site.json)). No street address is shown anywhere: this is a service area business.
- Page copy: `src/index.njk`, `src/services.njk`, `src/about.njk`, `src/service-areas.njk`, `src/contact.njk`
- Home page schema and FAQ schema: `src/_includes/schema-home.njk` (keep FAQ text matching the page)
- Images: `src/images/` (WebP)

## Estimate form
Netlify Forms (form name "estimate"). After the first deploy, set the notification email in Netlify: Forms > estimate > Form notifications. Successful sends go to /thank-you/.

## Before launch
Replace every [BRACKETED] placeholder: hours. Check site.url in site.json matches the live domain (www or not).

## Deploy
Push to main. Netlify builds with `npm run build` and publishes `_site`.
