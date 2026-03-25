# gsap-product-landing

> Animated product landing page — a GSAP timeline orchestrates staggered entrance sequences for navbar, headline, and hero image using Expo and power2 easing curves.

---

## What this demonstrates

A focused exercise in GSAP timeline choreography — three entrance animations sequenced so each element arrives at the right moment, with easing curves chosen to match the intended feel of each element.

The navbar slides in from above with `Expo.easeInOut` (fast start, ultra-smooth stop — authoritative). The headline drives in from the left with `Expo.easeIn` (builds momentum — dramatic). The hero image rises from below with `power2.out` (decelerates gently — natural). Each curve is deliberate, not random.

---

## Timeline breakdown

```js
var tl = gsap.timeline()

tl.from("#nav",      { y: "-40%", duration: 1, opacity: 0, ease: "Expo.easeInOut" })
  .from("#main h1",  { x: "-40%", duration: 2, opacity: 0, ease: "Expo.easeIn" })
  .from("#boi",      { y:  "40%", duration: 2, opacity: 0, ease: "power2.out" })
```

The timeline runs sequentially — each `.from()` call starts after the previous one completes. GSAP timelines are the foundation of every complex multi-element animation on the web; this is where that understanding starts.

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| GSAP 3 | Timeline sequencing, easing control |
| Vanilla JavaScript | Minimal, direct |
| HTML + CSS | Layout and typography |
| Gilroy OTF | Custom locally hosted font — ExtraBold + Light pairing |

---

## Getting Started

No build step. Open directly or serve with any static server.

```bash
git clone https://github.com/YOUR_USERNAME/gsap-product-landing.git
cd gsap-product-landing && open index.html

# or with a local server
npx serve .
```

---

## Project Structure

```
gsap-product-landing/
├── index.html
├── Socks.css
├── script.js        # GSAP timeline
├── fonts/
│   ├── Gilroy-ExtraBold.otf
│   └── Gilroy-Light.otf
└── IMAGES/
    ├── emoji.png
    ├── tedaladka.png
    └── ondalonda.png
```

---

## Deploy

Drag the folder to [Netlify](https://netlify.com). No build command. Publish directory: `/`.

---

## License

MIT
