[README.md](https://github.com/user-attachments/files/32206823/README.md)
# ZavisCAD — webová stránka

Oficiálna webová stránka **ZavisCAD** — služby zákazkovej 3D tlače, 3D CAD modelovania a technického poradenstva pre jednotlivcov aj firmy.

🔗 Live: [zaviscad.sk](https://www.zaviscad.sk)

## O projekte

Stránka predstavuje dve hlavné cieľové skupiny hneď pod úvodným nadpisom:

- **Pre jednotlivcov** — prekreslenie a 3D tlač zlomených/stratených súčiastok.
- **Pre firmy** — prevod starej 2D dokumentácie (PDF) na presné 3D CAD modely, návrh inžinierskych prípravkov.

Návštevník môže priamo zo stránky odoslať nezáväzný dopyt cez formulár, ktorý posiela email majiteľovi (Web3Forms). Stránka je dvojjazyčná (SK/EN) a obsahuje aj samostatné podstránky FAQ a O mne.

## Štruktúra projektu

```
index.html          hlavná stránka (hero, PRE JEDNOTLIVCOV / PRE FIRMY, kontaktný formulár)
faq.html             často kladené otázky (rozbaľovací zoznam)
o-mne.html           stránka o zakladateľovi
robots.txt           pravidlá pre vyhľadávače
sitemap.xml          mapa stránok pre SEO

diel-povodny.png     obrázok pôvodného dielu (panel PRE JEDNOTLIVCOV)
diel-3d-navrh.png    obrázok 3D CAD návrhu (panel PRE JEDNOTLIVCOV)
vykres-stary.jpg     fotka starej dokumentácie (panel PRE FIRMY)
vykres-novy.png      reálny CAD výkres (panel PRE FIRMY)
```

Žiadny build krok, žiadne závislosti — čistý HTML/CSS/JS. Stačí nahrať súbory a stránka funguje.

## Technické detaily

- **Bez frameworkov** — každá stránka je samostatný `.html` súbor s vlastným `<style>` a `<script>` blokom.
- **Fonty:** Space Grotesk (nadpisy), Inter (text), JetBrains Mono (technické detaily/kódy) — cez Google Fonts.
- **SK/EN prepínač:** jednoduchý JS systém založený na `data-i18n` atribútoch a slovníku prekladov v `<script>`. Jazyk sa nepamätá medzi stránkami (každá stránka štartuje v slovenčine).
- **Kontaktný formulár:** odosiela sa cez [Web3Forms](https://web3forms.com) (žiadny vlastný backend). Obsahuje honeypot pole proti spamu.
- **SEO:** meta title/description, canonical URL a JSON-LD (`ProfessionalService`) štruktúrované dáta na `index.html`.

## Nasadenie

Stránka beží na **Vercel**, prepojená s týmto GitHub repozitárom — každý push do `main` sa automaticky nasadí na produkciu.

## Ako pridať/upraviť obsah

- **Formulár / kontaktné údaje:** `index.html`, sekcia `#kontakt`.
- **FAQ otázky:** `faq.html` — každá otázka je blok `.faq-item`, odpoveď pod ňou.
- **Texty a preklady:** na konci každého súboru je JS objekt `translations` so `sk` a `en` verziou všetkých textov.
