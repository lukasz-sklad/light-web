# LightCraft Web (Lightroom Alternative)

Wersja przeglądarkowa **LightCraft** (Rust + WebAssembly + WebGPU/WebGL2 + egui) — nieniszcząca cyfrowa ciemnia fotograficzna, wywoływanie plików RAW i zaawansowana korekcja tonalna.

## Dostęp online

Aplikacja jest serwowana bezpośrednio pod adresami:
- **[https://light.lmk.one/](https://light.lmk.one/)**
- **[https://lightcraft.lmk.one/](https://lightcraft.lmk.one/)**
- Kopia GitHub Pages: **[https://lukasz-sklad.github.io/light-web/](https://lukasz-sklad.github.io/light-web/)**

## Kluczowe możliwości i domyślna konfiguracja

- **Silnik:** Rust `wasm32-unknown-unknown` skompilowany z optymalizacjami `wasm-opt -O2` i prekompresją Brotli/Gzip.
- **Domyślna konfiguracja:**
  - Język interfejsu: **Polski (PL)**
  - Motyw: **Ciemny (Dark mode)**
  - Akceleracja graficzna: **WebGPU** (z płynnym fallbackiem do **WebGL2**)
- **Obsługa parametrów URL:**
  - `?file=<url>` — automatyczne pobieranie zdjęcia z zewnętrznego adresu URL (z automatycznym mostkiem CORS `https://lmk.one/api/cors`), import do biblioteki oraz automatyczne otwarcie w widoku szczegółów (`view.detail`).
  - `?lang=pl` / `?lang=en` — dynamiczny wybór języka interfejsu.
- **Formaty:** RAW (DNG, CR2, CR3, NEF, ARW, RAF, RW2, ORF...), TIFF, JPEG, PNG, WebP, AVIF, JPEG XL (.jxl).
