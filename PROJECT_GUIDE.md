# YouTube Home Demo - HTML aur CSS Guide

Yeh document project mein istemal kiye gaye HTML tags, CSS selectors aur unke kaam ko Roman Urdu mein samjhata hai.

## Project files

- `index.html` - GitHub Pages ka entry page jo homepage kholta hai.
- `home.html` - YouTube jaisa homepage, video cards, category buttons aur Shorts section.
- `login.html` - Sign-in form ka visual demo.
- `signup.html` - Account creation form ka visual demo.
- `style.css` - Homepage aur login page dono ki styling.

## HTML tags

HTML tags page ka structure aur content banate hain. `home.html` aur `login.html` mein yeh tags istemal hue hain:

| Tag | Is project mein kaam |
|---|---|
| `<!DOCTYPE html>` | Browser ko batata hai ke document HTML5 hai. |
| `<html lang="en">` | HTML document ka root aur page ki language batata hai. |
| `<head>` | Page ki settings aur stylesheet link rakhta hai. |
| `<meta>` | Character encoding aur mobile viewport set karta hai. |
| `<title>` | Browser tab mein page ka naam dikhata hai. |
| `<link>` | `style.css` ko HTML page se connect karta hai. |
| `<body>` | Page ka visible content rakhta hai. |
| `<header>` | Upar ka bar: menu, logo, search, Create, notifications aur account. |
| `<button>` | Search aur form jaise controls. |
| `<a>` | Doosre page ya link par le jata hai; account, navigation aur video cards mein istemal hua hai. |
| `<form>` | Search aur demo sign-in fields ko group karta hai. |
| `<label>` | Input field ka naam batata hai; `for` ko input ke `id` se milaya jata hai. |
| `<input>` | Search, email aur password enter karne ke fields. |
| `<span>` | Chhote inline hisse, jaise logo play mark aur notification count. |
| `<sup>` | Logo ke paas chhota `PK` text. |
| `<aside>` | Homepage ka left-side navigation area. |
| `<nav>` | Main navigation aur video category links/buttons ko group karta hai. |
| `<ul>` aur `<li>` | Navigation items ki list banate hain. |
| `<main>` | Page ka main content rakhta hai. |
| `<section>` | Recommended videos, Shorts aur login form jaise page sections. |
| `<article>` | Ek video ya Short ka alag card. |
| `<h1>`, `<h2>`, `<h3>` | Page aur video headings. |
| `<p>` | Video details, channel info aur helper text. |
| `<img>` | Video aur Shorts thumbnail images. `alt` text image ka description deta hai. |
| `<svg>` | Menu, search aur navigation ke icons. |
| `<path>`, `<circle>`, `<rect>` | SVG icons ki lines aur shapes. |

### HTML attributes

- `class` elements ko CSS styling ke liye naam deta hai; misal: `class="video-card"`.
- `id` ek element ki unique pehchan hai; misal: `id="search"`.
- `href` link ka destination batata hai.
- `src` image ka address batata hai aur `alt` uska text description deta hai.
- `type` input ya button ka qisam batata hai, jaise `search`, `email`, `password` ya `button`.
- `aria-label`, `aria-labelledby` aur `aria-current` screen readers aur accessibility state ko describe karte hain.

## CSS kaise likhi gayi hai

CSS mein HTML ki tarah tags nahi hote; is mein **selectors** hote hain. Selector batata hai ke styling kis HTML element par lagegi.

### Selectors ki misaalein

- `body`, `header`, `main`, `article`, `img` - HTML tag selectors.
- `.video-card`, `.side-link`, `.login-card` - class selectors; `.` class ko select karta hai.
- `#search` - ID selector; `#` ID ko select karta hai.
- `header form input` - header ke form ke andar input select karta hai.
- `.category-chip[aria-current="page"]` - current category link ko style karta hai.
- `:hover` aur `:focus` - pointer le jane ya keyboard se focus hone par style lagate hain.
- `::before` - element ke text se pehle decorative content dikhata hai.
- `[hidden]` - hidden attribute wale element ko display nahi karta.
- `@media (max-width: ...)` - screen chhoti ho to responsive styles apply karta hai.

### Ahm CSS properties

| Property | Kaam |
|---|---|
| `color`, `background`, `background-color` | Text aur page/component ke rang set karte hain. |
| `font-family`, `font-size`, `font-weight` | Font ki family, size aur motai set karte hain. |
| `display: flex` | Header aur controls ko ek line mein arrange karta hai. |
| `display: grid` | Video cards ko columns aur rows mein arrange karta hai. |
| `grid-template-columns` | Grid mein columns ki tadaad aur size set karta hai. |
| `gap` | Grid ya flex items ke darmiyan faasla rakhta hai. |
| `position: fixed` / `sticky` | Header/sidebar ko screen par aur category bar ko scroll par visible rakhta hai. |
| `margin`, `padding` | Elements ke bahar aur andar ka faasla set karte hain. |
| `width`, `height`, `min-height` | Element ke dimensions set karte hain. |
| `border`, `border-radius` | Border aur rounded/circular shapes banate hain. |
| `overflow` | Zyada content ko clip ya scroll karne ka tareeqa set karta hai. |
| `aspect-ratio`, `object-fit` | Thumbnail ka ratio aur image crop set karte hain. |
| `:hover`, `:focus` ke styles | Clickable elements par interaction feedback dete hain. |
| `transition` | Hover ya state change ko smooth banata hai. |

## Homepage par interaction

- Search form query ko YouTube results page par bhejta hai.
- Category links YouTube par us category ke search results kholte hain.
- Menu aur notifications icons visual hain; HTML/CSS-only page mein unke controls active nahi hain.
- `login.html` aur `signup.html` sirf form ka visual demo hain; authentication ya account save nahi hota.
- Project sirf HTML aur CSS istemal karta hai. Local search filtering, account creation/login aur video upload ke liye JavaScript aur/ya backend darkar hain.
- `.github/workflows/pages.yml` - `main` ya `master` par push hone par GitHub Pages par site deploy karta hai.

## Responsive layout

`@media` rules screen ki width ke mutabiq layout badalte hain: desktop par teen video columns, medium screens par do, aur mobile par ek column. Chhoti screen par left sidebar chhup jata hai aur category bar horizontal scroll hoti hai.
