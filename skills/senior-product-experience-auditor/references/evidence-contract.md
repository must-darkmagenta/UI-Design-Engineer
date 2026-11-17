# Evidence and output contract

## Severity

- S0 Blocker: core task cannot complete, or evidenced security/money-loss risk requiring immediate hold.
- S1 Critical: major task failure, accessibility blocker or irreversible-action risk.
- S2 High: significant confusion or likely errors.
- S3 Medium: degraded usability or meaningful polish issue.
- S4 Low: small refinement.

Severity describes impact, not confidence. An inferred S0 risk stays inferred until tested. Do not mechanically translate all model “high priority” findings into critical defects.

## Finding

ID; screen/URL; component; severity; confidence (high / medium / low); category/layer; classification (observed defect / inferred risk / subjective preference); observed issue; user consequence or plausible concern; evidence and its source; expected behavior; recommended fix; measurable acceptance criterion; screenshot/locator or source reference. Use exact source references only when inspected. State what would raise confidence for inferred risks. Deduplicate by root cause without merging unrelated controls just because they share a word such as “label.”

Write each top finding so a teammate unfamiliar with the page can act on it:

1. **Where and what:** identify the section/component, viewport and state, with a screenshot, locator, URL or source reference actually inspected. Describe the visible arrangement or interaction, not just the category name.
2. **User path and consequence:** say what a first-time visitor tries to do and what happens. Distinguish reproduced failure from a plausible concern; do not invent user confusion or conversion impact.
3. **Change:** give a specific content, layout, hierarchy, state or behavior change that fits the existing system. “Improve contrast” or “make the CTA clearer” alone is not actionable.
4. **Check:** state the observable before/after condition and the viewport or interaction needed to verify it. If the evidence mode cannot establish the claim, name the missing test instead of presenting it as fact.

For visual/UI findings, discuss the relevant type size and wrapping, spacing, alignment, color/contrast, density, component state, or information order when observed. For UX findings, trace the path from entry to action and feedback, including alternate or error states when tested. Do not list every design dimension automatically; report the ones that explain the actual problem. A working pattern can be a strength, and a sound review can have no significant findings.

## Report

1. Verdict for the requested decision, with evidence limits.
2. Primary journey steps and tested state of each.
3. Highest-impact unique findings in order. A priority table can orient the reader, but it is not the full review: expand the top findings using the four parts above. Make lower-impact details expandable or linked when possible.
4. For a journey or launch review: the review-layer coverage matrix, including untested and inapplicable layers. Skip it for a single-screen review.
5. Regression tests and exit criteria.

For a UI review, add a short **experience walkthrough** before the findings: what a visitor sees first at each tested width, the primary action and where it leads, and the result or interruption observed. Add **what works and should survive** so a proposed redesign does not erase effective brand, content or interaction choices. State exact widths, device/browser, date and evidence mode when available. If only HTML text or a screenshot was available, do not claim mobile fold position, visual contrast, animation behavior, keyboard behavior, or screen-reader announcements as tested.

Never invent user studies, success metrics, score distributions, past failures or fixes. Auditing your own product is useful, but it is not independent validation. Repeatability requires fixed inputs and multiple recorded runs; before/after quality requires checking the actual changes and controlling for run variance.
