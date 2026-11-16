# Factory Dashboard Alert Recall Test

CS 6795 (Cognitive Science) final project, OMSCS, Georgia Tech. Wilson Tu.

A browser-based short-term memory test that checks whether grouping factory alert words under meaningful category labels (chunking) improves recall.

**Live test:** https://wtu4979.github.io/factory-recall-test/

## How it works
- Each round shows a list of single-word factory alerts for 8 seconds.
- The participant then types back every word they remember, one per line.
- Scoring: exact match, or one typo allowed for words of 5+ letters. Repeats and words not on the list count as intrusions.
- List lengths: 3, 5, 7, 9, 11 items.
- One unscored practice round, then 10 scored rounds in 2 blocks of 5.
- Conditions:
  - **Grouped:** words shown under category labels (FLUID, ELECTRICAL, MECHANICAL, HANDLING, SAFETY, MACHINING).
  - **Ungrouped:** the same kind of words, shuffled, with no labels.
  - The first block's condition is random; the second block uses the other one.
- Green/red feedback is shown after each round.

## Data
At the end, the participant downloads (or copies) a CSV with these columns:

`participant_id, round, block, condition, n_items, display_ms, n_correct, n_intrusions, accuracy, recall_ms, alerts_shown, response, timestamp`

No names or personal information are collected. Each participant gets a random code.

## Running locally
`index.html` is a single self-contained file. Open it in any modern browser.
