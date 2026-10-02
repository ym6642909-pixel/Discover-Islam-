# Descubre el Islam — multilingual static site

Languages: Arabic, Spanish, English, French, Russian. Each language has an independent `/lang/` entry point with hreflang. Content files share one schema and are validated by `node tools/validate-content.mjs`.

## Add a language
Copy `content/ar.json`, translate values without changing keys/arrays, create `/xx/index.html`, add the language to `langs` in `assets/app.js`, and run the validator. Native-speaker and qualified Islamic-studies review are required.

## Add a page
Add the same page key to every language JSON, add a section with that id to the shell, add its renderer in `assets/app.js`, add a navigation label in every language, and attach a source.

## Quran
`quran/chapters.json` contains all 114 chapter entries. The final production layer must supply authorized Quran text, licensed/authorized translations, identified tafsir, and audio. Quran Foundation documents Content APIs for verses, translations, tafsir and audio, and explicitly says browser apps must not expose a client secret; use a backend/serverless proxy.

## Quality gate
1. Arabic source reviewed by a qualified Islamic-studies reviewer. 2. Every translation reviewed by a native speaker. 3. Terminology matches `content/terms.json`. 4. Quran translation/tafsir license or authorization checked. 5. Madhhab differences attributed. 6. No automatic translation as final copy. 7. Mobile 375px, keyboard, contrast, RTL/LTR and reduced motion tested. 8. Console and external links checked.
