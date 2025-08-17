# Aniflix Frontend

## Demo
Watch the walkthrough here:
https://drive.google.com/file/d/1olCj6TbSXh3wK5V8vSFTvZJso2eKGuSP

## Overview
React app that provides a streaming-style UI (home slider, banners, cards) and plays videos with captions via Plyr. Uses React Router for navigation and fetches data from the Aniflix backend.

## Quick Start
```bash
# from aniflix-frontend-main/
npm install
# set API base in .env
echo 'REACT_APP_API_URL=http://localhost:7000/api/' > .env
npm start
```

## Key Scripts
- `npm start` – run dev server
- `npm run build` – production build

## Environment
- `REACT_APP_API_URL` – backend REST base (e.g., http://localhost:7000/api/)

## Notable Components
- `components/Slider/Home Slider/Slider.jsx` – Swiper carousel fetching banner IDs
- `components/Banner/Banner.jsx` – fetches and displays movie/series/season meta; deep-links to watch pages
- `components/VideoPlayer/VideoPlayer.jsx` – Plyr-based player with optional VTT captions and download/next buttons
- `pages/movies/MoviesPage.jsx`, `pages/series/SeriesPage.jsx` – grid lists with category filters
- `pages/watch/ItemWatch.jsx` and `pages/watch/EpisodeWatch.jsx` – playback screens
- `pages/season/SeasonPage.jsx` – season details + episodes list

## Routes (examples)
- `/` – home slider
- `/movies` – movies grid
- `/tvseries` – series grid
- `/watch?mid=<movieId>` – play a movie
- `/series?seid=<seriesId>` – series details
- `/season?sid=<seasonId>` – season & episodes
- `/epiwatch?eid=<sid>s<eid>` – play an episode

## Tech
- React 18, react-router-dom
- Swiper for carousels
- Plyr (plyr-react) for the video player
- axios / fetch for API calls
