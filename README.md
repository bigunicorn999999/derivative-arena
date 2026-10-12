# Derivative Arena

[Open hosted Derivative Arena](https://derivative-arena.peachythyme16.chatgpt.site) — the Sites copy is private to its owner.

For GitHub Pages, choose Settings → Pages → Deploy from a branch → main → / (root). Website files are at the repository root.

# Derivative Arena

Open **index.html** in your browser to practice. The app and formula fonts are included; no internet connection or installation is needed for this option. Keep this folder together.

For a localhost version, double-click **Start Local Website.cmd** on Windows. Keep its terminal open while practicing. It uses Node.js from your computer (including the bundled Codex runtime) and serves only on your own computer at http://127.0.0.1:4173. If that address already works, the server is already running. Close the terminal to stop a manually launched server.

## What is included

- 1,201 questions in 59 problem families, covering 12 primary concepts.
- 10-, 20-, or 40-question rounds; 30-, 60-, 120-, or 240-second timers, plus untimed practice.
- Hard-only, sprint, core bee mix, and optional stretch difficulty filters.
- Answer key, solution approaches, concept recommendations, per-question times, and focused retry rounds.
- Searchable question bank and full question/answer export in `question-bank.json`.
- Browser-local round recovery and recent scores. Storage is separate for a file opened directly and a localhost URL, and may be unavailable in private browsing.

## Scoring

Displayed formulas use **ln** for natural logarithms and **arcsin**, **arccos**, and **arctan** for inverse trigonometric functions. Machine-readable expression fields in the exported bank retain their symbolic-library names.

Solve on paper or type in the scratchpad. Reveal the answer to stop the clock, then mark whether your answer was correct. **Scoring is self-graded; typed answers are not automatically checked.** Equivalent mathematical expressions may be correct even if they look different from the answer key.

A timeout counts as missed. The timer keeps running when you switch tabs or close the browser. After reopening the app, choose **Resume round**. Time spent reading revealed solutions is excluded from solve-time statistics. Unattempted questions from an early-ended round are excluded from concept diagnostics but remain in the round's score denominator.

### Equivalent answer forms

The main answer now favors a compact expression with fewer nested fractions. **Other equivalent forms** shows up to three additional useful versions, such as a common denominator, a factored expression, an expanded numerator, or the original differentiation-rule form. Simple answers may have no useful alternative to display. Equivalent forms are available in answer reveals, the searchable bank, and the end-of-round review, and are included in the exported question bank.

Each listed form was checked symbolically against the original derivative on the stated domain. The alternatives are examples, not an exhaustive list of correct answers. Cancellation does not remove exclusions from the original problem. Fractions inside an original function argument or variable exponent are sometimes kept because eliminating them would make the answer longer or less readable.

TAMU's published 2025 rules describe multiple-choice qualifiers and whiteboard elimination rounds, but do not specify a required simplified answer form. This site does not prescribe an official contest format. The organizers decide judging requirements; for practice, mathematically equivalent answers on the stated domain count as correct.

The concept breakdown uses primary tags, so a missed mixed-rule question does not prove which individual step caused the mistake. Use the solution approach to identify your actual error. Small samples are tentative.

## Bank provenance and validation

Two questions are actual examples reported in a [2013 TAMU faculty account](https://tamuscience.com/2013/11/13/derivative-bee/). The other 1,199 entries are original parameterized practice variants, not a historical college contest archive. There are 59 structural families, not 1,201 unrelated techniques.

The [published TAMU page](https://artsci.tamu.edu/mathematics/outreach/programs/dirivativebee.html) describes the 2025 event and Calculus I scope. It gives example qualifying time limits of 2 or 4 minutes. This site's 20-question format is for training. Check with the organizers for current rules. The [UC Merced event page](https://appliedmath.ucmerced.edu/integration_bee) was consulted for context; it supplied no questions used here.

The 1,129 explicit-derivative entries were differentiated with SymPy and each checked independently at three real test points with high-precision numerical differentiation: 3,387 checks. The 72 implicit answers were checked symbolically by substituting into F_x + F_y y' = 0. Numerical checks are evidence, not a proof across every possible domain. All 2,402 question/answer formulas were also checked for successful typesetting.

Question domain notes are part of the problem. The default restriction is x > 0 within the real, differentiable domain, with zero denominators excluded. Inverse trigonometric functions use principal real branches; angles are in radians. Higher derivatives and hyperbolic functions are labeled **Stretch** and excluded from the default core mix. Difficulty labels are editorial estimates, not measured contest rankings.

## Files

- `index.html`, `app.js`, `style.css`: the practice site.
- `question-bank.json`: portable question bank with expressions, LaTeX answers, approaches, domains, and provenance.
- `bank.js`: the same bank packaged for offline browser loading.
- `verification.json`: answer-validation summary and concept counts.
- `vendor/katex`: locally bundled formula renderer, fonts, and license.
- `server.cjs`: optional local server; no external packages required.

Functional checks covered complete rounds, scoring, family diversity, timeouts, refresh recovery, focused practice, filters, unseen-question preference, and responsive layouts. The app makes no external requests during practice.

