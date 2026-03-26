# Plex Audio Web

A Plexamp-style web app for Plex music libraries and audiobook-style `.m4b` content.

## Features

- Browse Plex audio libraries
- Recent items, albums/books, and search
- Stream audio through a server-side proxy
- Range request support for long-form audio
- Album track playback
- Audiobook playback with chapter jumping when Plex exposes chapters
- Playback rate control
- Browser-saved listening progress
- Vercel-ready deployment

## Local development

```bash
cp .env.example .env.local
npm install
npm run dev
```

Open `http://localhost:3000`.

## Vercel

Add these environment variables in the Vercel project:

- `PLEX_BASE_URL`
- `PLEX_TOKEN`
- `ALLOW_INSECURE`
- `AUDIO_SECTION_KEYS`

## Notes

- Your Plex server must be reachable from Vercel.
- Some `.m4b` files will play directly in browsers; unsupported files may need a future transcoding path.
- Put audiobooks in a music-style Plex library for best results with this app.
