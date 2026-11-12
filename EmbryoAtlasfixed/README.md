# EmbryoAtlas

A mobile-first React + Three.js embryology study-partner prototype for preclinical medical students.

## Run locally

1. Install Node.js 18+.
2. In this folder run `npm install`.
3. Copy `.env.example` to `.env` and add a Gemini API key if you want the AI tutor enabled.
4. Run `npm run dev` and open the local URL printed by Vite.

## Included in this first build

- Stage navigator from fertilization through week 40, with early cleavage, morula, blastocyst, implantation, bilaminar disc, gastrulation, neurulation, somites, folding, organogenesis and fetal milestones.
- Procedural 3D teaching meshes using Three.js / React Three Fiber; rotate, zoom and pan with OrbitControls.
- Timeline play/pause, speed options, stage selection and local progress/bookmarks.
- Germ-layer mode with ectoderm (blue), mesoderm (red), endoderm (yellow) palette.
- Learning notes, objectives, clinical correlations, teratogen-window concept chart and local MCQ quiz.
- English/Amharic stage-name toggle; Amharic terms use ሽል for embryo and ፅንስ for fetus.
- Gemini tutor with teaching modes and pasted-notes context. The key is read from `VITE_GEMINI_API_KEY`.

## Important scope and accuracy notes

- The procedural meshes are schematic learning aids, not validated anatomical reconstructions, histology, scans, or exact morphometric models. The early/fetal model is deliberately illustrative. Do not use it as a diagnostic or clinical reference.
- Gestational age is shown as approximately two weeks greater than fertilization age. The embryonic period is weeks 3–8 after fertilization; the fetal period begins at week 9 after fertilization.
- The teratogen chart shows broad teaching windows only. Actual susceptibility depends on the specific exposure, dose, timing and organ system.
- This is an initial study-partner build. Advanced features such as true anatomical cross-sections, anatomically validated explodable layers, raycast structure selection with derivative cards, full 40-week morph targets, bilingual quiz translation, spaced-repetition scheduling and backend-secured Gemini proxy should be implemented and validated in subsequent iterations.
- For production, do not expose a long-lived Gemini API key in a client-side Vite bundle. Put Gemini calls behind a server-side endpoint with authentication, rate limits and privacy controls.

## Textbook alignment

Organized to accompany the general embryology sequence in Langman's Medical Embryology (chapters 1–7), then connect to special embryology by organ system. The app uses original summaries and prompts students to consult their own textbook edition and figures; it does not include reproduced textbook passages.
