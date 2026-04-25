# coolmonk-site

Personal site for [coolmonk.org](https://coolmonk.org), built with [Astro](https://astro.build).

## Stack

- **Framework**: Astro 4 (static output)
- **Fonts**: Playfair Display · Newsreader · DM Mono (Google Fonts)
- **Hosting**: DigitalOcean App Platform (GitHub integration)

## Local development

```bash
npm install
npm run dev        # http://localhost:4321
```

## Deploy

Push to `main` — App Platform builds and deploys automatically.

Build command: `npm run build`  
Output directory: `dist`

## Assets

Copy your images into `public/images/`:

```
public/
  images/
    00010020.jpg    ← Venice Biennale photo (copy from current server)
```

## Music embed

The SoundCloud embed on the homepage uses a playlist URL. To update it:

1. Go to your SoundCloud playlist → Share → Embed
2. Copy the `src` URL from the embed code
3. Replace it in `src/pages/index.astro` in the `<iframe>` block

## Structure

```
src/
  layouts/Base.astro        ← nav, footer, global head
  pages/
    index.astro             ← homepage
    work.astro              ← resume / profile
  components/
    WorkEntry.astro         ← single experience entry
  styles/
    global.css              ← all styles + design tokens
public/
  images/                   ← static images
```
