# 🚀 Centrum Dowodzenia Feliksa

**Dashboard z mapą miejsc dla dzieci w Warszawie i okolicach.**

59 miejsc pogrupowanych w 7 kategoriach — sale zabaw, place zabaw, muzea, teatry, zwierzęta, kawiarnie i inne atrakcje. Każde miejsce ma opis, kategorię i link do nawigacji Google Maps.

## Jak uruchomić lokalnie

To po prostu plik HTML — otwórz w przeglądarce:

```bash
xdg-open index.html   # Linux
open index.html       # macOS
start index.html      # Windows
```

Działa offline (po załadowaniu), wymaga tylko internetu do wyświetlenia mapy (Leaflet + OpenStreetMap).

## Jak wystawić do internetu

### Opcja 1: GitHub Pages (najprościej)

```bash
# Utwórz repo na GitHub
gh repo create centrum-dowodzenia-feliksa --public --source=. --remote=origin --push

# Włącz GitHub Pages w Settings → Pages → branch: main, / (root)
# Strona będzie live pod: https://<username>.github.io/centrum-dowodzenia-feliksa/
```

### Opcja 2: Netlify / Vercel (drag & drop)

1. Wejdź na [netlify.com](https://netlify.com) lub [vercel.com](https://vercel.com)
2. Przeciągnij folder `centrum-dowodzenia-feliksa/` — gotowe.

### Opcja 3: Własny serwer

Wrzuć plik `index.html` na dowolny hosting statyczny — to jeden plik, zero zależności.

## Funkcje

- 🗺️ **Mapa** z ciemnym motywem (CartoDB Dark)
- 🎯 **Filtrowanie** po 7 kategoriach
- 🔍 **Wyszukiwarka** (skrót: `/`)
- 📍 **Kliknięcie** w miejsce — zoom + popup z opisem
- 🧭 **Nawiguj** — link do Google Maps Directions

## Dane

Miejsca pochodzą z listy prywatnej, wzbogacone o:
- Współrzędne geograficzne (Nominatim + ręczne uzupełnienia)
- Opisy atrakcji
- Kategoryzację
- Emoji i kolory

## Budowa

```
centrum-dowodzenia-feliksa/
├── index.html   # cała aplikacja (CSS + JS + dane inline)
└── README.md    # ta instrukcja
```

Brak zależności npm, build tooli, frameworków — czysty HTML + CSS + JavaScript + Leaflet.