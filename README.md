# Apartmani Orhideja — demo web stranica

Jednostranična (single-page) demo prezentacija za obiteljski smještaj **Apartmani Orhideja**,
Banjol, otok Rab — 9 apartmana.

> Demo izrađen za prezentaciju klijentu. Sadržaj (nazivi apartmana, cijene, recenzije,
> kontakt podaci) je izmišljen, a fotografije su Unsplash placeholderi.

## Pokretanje

Nije potreban build. Otvorite `index.html` u pregledniku ili poslužite mapu statički:

```bash
npx serve .
```

## Deploy

Statička stranica — spremna za Vercel, Netlify, GitHub Pages ili bilo koji statički hosting.
Nema build koraka ni ovisnosti u `package.json`.

## Tehnologija

- HTML5 (semantički: `header` / `main` / `section` / `footer`)
- TailwindCSS preko CDN-a s prilagođenom paletom i tipografijom
- Vanilla JavaScript, bez frameworka i bez vanjskih JS biblioteka
- Google Fonts: Playfair Display (naslovi) + Inter (tijelo teksta)

## Sadržaj stranice

| Sekcija | Opis |
|---|---|
| Hero | Fotografija preko cijelog ekrana s Ken Burns efektom i dva CTA-a |
| O nama | Priča obitelji, brojke, potpis domaćina |
| Apartmani | 9 kartica s filtrima po kapacitetu i modalom s detaljima |
| Galerija | 12 fotografija u masonry rasporedu s lightboxom |
| Sadržaji | 8 pogodnosti s ikonama |
| Lokacija | Google Maps embed i udaljenosti |
| Recenzije | 3 testimoniala |
| Kontakt | Obrazac za upit s validacijom i kontakt kartice |

## Funkcionalnosti

- **HR / EN prekidač** — svi tekstovi kroz `data-hr` / `data-en` atribute, izbor se pamti u `localStorage`
- **Responsive**, mobile-first (3 / 2 / 1 kolona)
- **Scroll animacije** preko `IntersectionObserver`, uz poštivanje `prefers-reduced-motion`
- **Lightbox** galerija s navigacijom tipkovnicom (← → Esc)
- **Modal apartmana** s galerijom sličica i prečacem na obrazac
- **Plutajući WhatsApp gumb** i sticky „Rezervirajte sada" nakon scrolla
- **Fallback za slike** — ako vanjska fotografija ne učita, `imgFallback()` podmeće zamjensku
- Lazy-loading svih slika osim hero fotografije

## SEO

- Meta title i description s ključnim riječima (*apartmani Banjol*, *smještaj Rab*, *apartmani otok Rab*)
- Open Graph i Twitter Card meta tagovi
- JSON-LD strukturirani podaci (`LodgingBusiness`)
- Alt tagovi s relevantnim ključnim riječima na svim slikama

## Prije produkcije

- Zamijeniti Unsplash placeholdere stvarnim fotografijama objekta
- Zamijeniti Tailwind CDN lokalno buildanim CSS-om (CDN ispisuje upozorenje u konzoli)
- Spojiti obrazac na stvarni backend ili servis (Formspree, Netlify Forms, vlastiti endpoint)
- Unijeti stvarne kontakt podatke, cijene i ID kod objekta

## Struktura

```
.
├── index.html    # cijela stranica: markup, stilovi i skripta
└── README.md
```
