# Szopka

**A Kraków folk-art tradition, built in code.**
An interactive 3D *szopka krakowska* floating in space: foil-bright towers, a dragon in his cave, a Christmas market, snow you can shake off, and fireworks over Kraków.

**[▶ Open the live demo](https://agata-c.github.io/szopka/)** · [Polski](README.pl.md)

[![Watch the Szopka demo video](szopka-preview.jpg)](szopka-front-360-demo.mp4)

[▶ Watch the 14-second video](szopka-front-360-demo.mp4)

---

## What is a szopka?

*Szopka krakowska* is a Kraków folk-art tradition: glittering, many-towered models built from cardboard and coloured foil, inspired by the city's churches and landmarks. It is listed by UNESCO as Intangible Cultural Heritage. Every year, on the first Thursday of December, the builders bring their szopkas to Kraków's Main Market Square for a contest.

This one is digital. Everything you see, from every tower to every snowflake and pretzel, is generated in code. There are no image files and no 3D models.

## What you can do

| Action | What happens |
|---|---|
| Drag / scroll / pinch | Rotate and zoom around the island |
| Click the dragon | The Wawel dragon breathes fire (no SMS required) |
| Click Lajkonik | A tap of his mace brings a year of good luck |
| Click the sheep, the shepherd or the chimney sweep | Each one reacts |
| Click the trumpeter's window | He plays the hejnał from the tower |
| Click the sky | Fireworks |
| Double-click, or press **S** | Shake the island and watch the snow fly off |
| Press **C** | Call a comet |
| Day / Night · Snow · Sound | The buttons at the bottom |
| PL / EN | Switch the language |

Psst... there may be a secret key near the dragon.

## Kraków details hidden in the scene

- **Smok Wawelski**, the Wawel dragon, lives in the cave. In the legend he was defeated by a sheep stuffed with sulphur, which is why a sheep stands right next to him. (In real Kraków, his statue breathes fire if you pay by SMS. This one does it for free.)
- **Lajkonik**, the bearded rider in a hobby-horse who dances through Kraków in a procession every year, on the Thursday after Corpus Christi.
- **The hejnał**, the trumpet call played every hour from St. Mary's tower. It breaks off mid-phrase, in memory of the trumpeter shot by an arrow while warning the city. Here, too, it plays on the full hour.
- **The market**: obwarzanki and pretzels on a blue cart, flowers (sold on the Main Square all year round), oscypki, gingerbread hearts and hand-blown glass baubles.
- **The chimney sweep**, a Polish good-luck figure: hold a button when you see one.
- **The baca**, a highland shepherd with his flock, and the **Kraków pigeons**.
- The **Polish** and **Kraków** flags on the towers.

## How it was made

This project is an experiment in **directing AI to build graphics**, without drawing a single pixel by hand.

- **Concept, art direction, references and every design decision:** Agata Poniatowska-Ormicka
- **Character designs:** the dragon and the sheep were designed in Midjourney as "vinyl toy" turnarounds, then translated into code shape by shape
- **Technical specs & code review:** Claude (Anthropic)
- **Code:** Space Bunny, a stealth model in OpenCode, over about 30 build rounds
- **Music & sound effects:** made with Suno
- **Hejnał recording:** [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Cracow_trumpet_signal.ogg) (public domain)

The workflow ran in rounds: a precise spec, the build, a review of the code and screenshots, then fixes. Each round changed only what was asked.

**Tech:** a single `index.html` with [Three.js](https://threejs.org/) (r169, from a CDN) and the Web Audio API. All geometry, textures (foil, rock, lace, embroidery) and animation are procedural.

## Run it locally

The sounds load over HTTP, so open it through a small local server rather than by double-clicking the file:

```bash
npx serve .
```

or

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` (or the address `serve` prints).

## License

**Szopka** by **Agata Poniatowska-Ormicka** is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt it, including commercially, as long as you give appropriate credit. If you build on it, a tag or a link back would make my day.

Third-party parts keep their own terms: Three.js (MIT), and the hejnał recording (public domain, Wikimedia Commons).

