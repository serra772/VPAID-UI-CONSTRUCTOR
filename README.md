# VPAID Constructor

A visual drag-and-drop editor for creating VPAID 2.0 / VAST 3.0 interactive ad creatives. Build rich-media ads with video, carousels, CTAs, and legal text — then export a production-ready ZIP with `vpaid.js`, `test.html`, and `vast.xml`.

## Features

- **Visual Canvas** — drag, resize, and position components on a 1280×720 canvas with real-time preview
- **Component Library**:
  - **Video Window** — video player with play/pause, mute/unmute, volume slider, configurable autoplay delay, and per-component click-through URL
  - **Product Carousel** — image carousel with configurable slide interval, click URLs, and external navigation controls (arrows + dots)
  - **CTA Button** — customizable text, colors, border radius, and link
  - **Legal Text** — inline editable (double-click on canvas), configurable font, size, and color
  - **Background Image** — full-canvas background from URL
- **Tracking** — impression tracker, click tracker, custom tracking URL template with `[EVENT_ID]` substitution
- **erid Support** — embedded erid tag in the generated creative
- **Project Import** — load previously generated projects from VAST XML (file upload or URL)
- **One-Click Export** — generates a ZIP archive containing:
  - `vpaid.js` — self-contained VPAID 2.0 creative with all assets and logic
  - `vast.xml` — VAST 3.0 wrapper with MediaFile, AdParameters, and tracking
  - `test.html` — standalone test player

## Getting Started

1. Open `constructor.html` in any modern browser (Chrome, Firefox, Safari, Edge)
2. Enable components via checkboxes in the sidebar
3. Configure settings: video URL, images, click URLs, tracking pixels
4. Drag and resize components on the canvas
5. Click **Preview** to test the ad
6. Click **Generate Project** to download the ZIP

> No build tools, Node.js, or server required. Everything runs client-side.

## Project Import

Click **Load Project** to restore a previously generated project:
- **From URL** — paste a VAST XML URL and click Load
- **From File** — upload a `vast.xml` file

The constructor extracts `AdParameters` (full config), `MediaFile` (vpaid.js URL), and `AdTitle` (project name) from the VAST XML.

## Dependencies

Loaded via CDN (no installation needed):
- [JSZip](https://stuk.github.io/jszip/) — ZIP archive generation
- [FileSaver.js](https://github.com/nickstenning/FileSaver.js) — client-side file downloads

## File Structure

```
constructor.html   — the entire application (single-file, ~70KB)
README.md          — this file
```

---

# VPAID Конструктор

Визуальный drag-and-drop редактор для создания интерактивных рекламных креативов формата VPAID 2.0 / VAST 3.0. Собирайте rich-media рекламу с видео, каруселью товаров, CTA-кнопками и юридическим текстом — затем экспортируйте готовый ZIP с файлами `vpaid.js`, `player.html` и `vast.xml`.

## Возможности

- **Визуальный холст** — перетаскивание, изменение размера и позиционирование компонентов на холсте 1280×720 с предпросмотром в реальном времени
- **Библиотека компонентов**:
  - **Video Window** — видеоплеер с кнопками play/pause, mute/unmute, ползунком громкости, настраиваемой задержкой автовоспроизведения и индивидуальной ссылкой перехода
  - **Product Carousel** — карусель изображений с настраиваемым интервалом слайдов, ссылками и внешней навигацией (стрелки + точки)
  - **CTA Button** — настраиваемый текст, цвета, скругление углов и ссылка
  - **Legal Text** — редактирование прямо на холсте двойным кликом, настройка шрифта, размера и цвета
  - **Background Image** — фоновое изображение на весь холст по URL
- **Трекинг** — трекер показов, трекер кликов, шаблон URL трекинга с подстановкой `[EVENT_ID]`
- **Поддержка erid** — встроенная маркировка erid в генерируемом креативе
- **Импорт проекта** — загрузка ранее сгенерированных проектов из VAST XML (загрузка файла или по URL)
- **Экспорт в один клик** — генерирует ZIP-архив, содержащий:
  - `vpaid.js` — самодостаточный VPAID 2.0 креатив со всеми ресурсами и логикой
  - `vast.xml` — обёртка VAST 3.0 с MediaFile, AdParameters и трекингом
  - `player.html` — тестовый плеер

## Начало работы

1. Откройте `constructor.html` в любом современном браузере (Chrome, Firefox, Safari, Edge)
2. Включите компоненты с помощью чекбоксов в боковой панели
3. Настройте параметры: URL видео, изображения, ссылки перехода, пиксели трекинга
4. Перетащите и измените размер компонентов на холсте
5. Нажмите **Preview** для предпросмотра
6. Нажмите **Generate Project** для скачивания ZIP

> Не требуются инструменты сборки, Node.js или сервер. Всё работаeт на стороне клиента.

## Импорт проекта

Нажмите **Load Project** для восстановления ранее сгенерированного проекта:
- **По URL** — вставьте ссылку на VAST XML и нажмите Load
- **Из файла** — загрузите файл `vast.xml`

Конструктор извлекает `AdParameters` (полный конфиг), `MediaFile` (URL vpaid.js) и `AdTitle` (имя проекта) из VAST XML.

## Зависимости

Загружаются через CDN (установка не требуется):
- [JSZip](https://stuk.github.io/jszip/) — генерация ZIP-архивов
- [FileSaver.js](https://github.com/nickstenning/FileSaver.js) — скачивание файлов на стороне клиента

## Структура файлов

```
constructor.html   — всё приложение (один файл, ~70КБ)
README.md          — этот файл
```
