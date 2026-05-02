# Mituvos Baidarės — Svetainės redagavimo gidas

## Kaip paleisti svetainę lokaliai

Prieš redaguodami patikrinkite pokyčius naršyklėje:

```bash
node serve.mjs
```

Tada atsidarykite [http://localhost:3000](http://localhost:3000) naršyklėje.

---

## Telefono numerių keitimas

Telefono numeriai pasirodo **dviejose** vietose: kontaktų skiltyje ir polapinio apačioje (footer).

Faile `index.html` suraskite šiuos fragmentus (**Ctrl + F** → ieškokite `617 21486`):

### Kontaktų skyriuje (dideli mygtukai)

```html
<a href="tel:+37061721486" class="btn-phone" ...>
  ...
  +370 617 21486
</a>
<a href="tel:+37068333141" class="btn-phone" ...>
  ...
  +370 683 33141
</a>
```

Pakeiskite **abu** atributus: `href="tel:+370XXXXXXXXX"` ir tekstą `+370 XXX XXXXX`.

### Footer skiltyje

```html
<a href="tel:+37061721486">+370 617 21486</a>
<a href="tel:+37068333141">+370 683 33141</a>
```

Pakeiskite tokiu pat principu.

---

## Facebook nuorodos keitimas

Faile `index.html` suraskite (**Ctrl + F** → `facebook.com/p/Mituvos`):

Nuoroda pasirodo **trijose** vietose — galerijos sekcijoje, kontaktų sekcijoje ir footer'yje:

```html
href="https://www.facebook.com/p/Mituvos-Baidares-100083102182447/"
```

Pakeiskite visas tris į savo naują Facebook puslapio nuorodą. Pati lengviausia eiga — **Replace All** (`Ctrl + H`):
- Ieškoti: `https://www.facebook.com/p/Mituvos-Baidares-100083102182447/`
- Pakeisti į: jūsų nauja nuoroda

---

## Instagram nuorodos keitimas

Faile `index.html` suraskite (**Ctrl + F** → `instagram.com/mituvosbaidares`):

Nuoroda pasirodo **trijose** vietose — ta pati `Replace All` procedūra:
- Ieškoti: `https://www.instagram.com/mituvosbaidares/`
- Pakeisti į: jūsų nauja Instagram nuoroda

---

## Nuotraukų keitimas galerijos karuselėje

Galerijos karuselėje yra **5 placeholder nuotraukos**. Norėdami pakeisti:

1. Įkelkite savo nuotraukas į aplanką `brand_assets/` (arba sukurkite atskirą aplanką, pvz. `photos/`).

2. Faile `index.html` suraskite galerijos sekciją — ieškokite `id="galerija"`.

3. Kiekvieną placeholder pakeiskite savo nuotraukos keliu:

**Prieš:**
```html
<img src="https://placehold.co/800x600/163324/68B5B0?text=Baidarės+Mituvoje"
     alt="Baidarės Mituvos upėje" />
```

**Po:**
```html
<img src="brand_assets/baidares-upeje.jpg"
     alt="Baidarės Mituvos upėje" />
```

Taip pat galite pakeisti antraštę po nuotrauka — tai yra `<div class="c-caption">` elementas:

```html
<div class="c-caption">Baidarės Mituvos upėje</div>
```

### Nuotraukų rekomenduojamas dydis
- **Plotis:** bent 1200 px
- **Aukštis:** bent 900 px (proporcija 4:3)
- **Formatas:** `.jpg` arba `.webp` (geriausia kokybė / dydžio santykiui)

---

## Glamping sekcijos nuotraukos keitimas

Glamping sekcijoje yra vienas didelis placeholder vaizdas. Suraskite:

```html
<img src="https://placehold.co/800x600/163324/68B5B0?text=Glamping+teritorija"
     alt="Glamping stovyklavietė Mituvos Baidarės" />
```

Pakeiskite į savo nuotrauką:

```html
<img src="brand_assets/glamping-teritorija.jpg"
     alt="Glamping stovyklavietė Mituvos Baidarės" />
```

---

## Logotipo atnaujinimas

Logotipas saugomas `brand_assets/mituvosbaidares.jpeg`. Norėdami atnaujinti:

1. Įdėkite naują logotipo failą į `brand_assets/`.
2. Faile `index.html` pakeiskite visus `src="brand_assets/mituvosbaidares.jpeg"` į naują failo pavadinimą.

---

## Greita turinio redakcija

| Ką keisti | Kur ieškoti `index.html` |
|---|---|
| Telefonai | `tel:+370617` |
| Facebook nuoroda | `facebook.com/p/Mituvos` |
| Instagram nuoroda | `instagram.com/mituvosbaidares` |
| Galerijos nuotraukos | `id="galerija"` → `c-slide` elementai |
| Glamping nuotrauka | `Glamping+teritorija` |
| Verslo adresas | `Mantvilių k.` |
| Copyright metai | `© 2024` |
