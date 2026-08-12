# EVRVL — Everville Estate

Статичный сайт: главная + страница проектов (desktop / tablet / mobile), без сборки.

## Страницы

| URL | Источник |
| --- | --- |
| `index.html` | `Main.dc.html` — главная (все разрешения) |
| `projects.html` | `Projects Desktop v1.dc.html` — проекты, ≥1024px |
| `projects-tablet.html` | `Projects Tablet v1.dc.html` — проекты, 768–1023px |
| `projects-mobile.html` | `Projects Mobile v1.dc.html` — проекты, <768px |

Страницы проектов сами перебрасывают посетителя на нужную версию по ширине экрана.

## Структура

- `support.js` — рантайм компонента
- `assets/` — изображения, логотипы, видео; `assets/projects/` — рендеры проектов (WebP, ≤1920px)
- `fonts/` — HeadingNow 82 Light / 84 Regular (.otf)
- `dist/` — готовый к деплою комплект (те же страницы + assets/fonts/support.js)
- `*.dc.html` — исходные компоненты (шаблон + логика), из них собираются страницы

## Локальный запуск

```bash
python3 -m http.server 8000
# → http://localhost:8000/
```

## Деплой

Любой статический хостинг (GitHub Pages, Netlify, Vercel) — публикуется корень репозитория или `dist/`, сборка не нужна.
