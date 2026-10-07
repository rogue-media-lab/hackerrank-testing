# HackerRank Testing

Personal prep material for a timed HackerRank technical assessment. Two self-contained
HTML pages — no build step, no dependencies, no server. Open them in a browser.

This is a study repo. It contains no proprietary assessment content and no answers to any
live test. The practice problems are written from published candidate reports of the
general format.

---

## Files

### `study-plan.html`

The study plan. Ranked by priority, so if you lose a day, cut from the bottom — never the top.

- What the assessment actually is: length, format, scoring, language options
- The confirmed topic pool and, more usefully, what to **skip**
- A day-by-day drill schedule with specific problems
- An edge-case checklist to run before every submit
- A pre-flight section: compatibility check, sample test, and the proctoring rules
- Notes on the stage that follows the assessment

### `mock-test.html`

A working practice test, not a worksheet.

- **90-minute countdown** that turns amber at 20 minutes and red at 5
- **Two problems** calibrated to the real thing — a sliding-window/frequency-map problem
  and a binary-search-with-boundary-conditions problem
- **A real grader.** Type your solution in the page, hit *Run Tests*, and it executes your
  code against the same cases a platform would hide. Visible and hidden cases are marked
  separately, because "all visible cases green" is not the same as passing.
- **A genuine complexity check.** The second problem requires O(log n). A linear scan passes
  every correctness case and fails the real assessment — so the *Check O(log n)* button hands
  your function a proxy-wrapped array that counts how many elements it reads. Binary search
  reads ~24 of 4096; a loop reads all 4096 and fails. Copying the array first also fails,
  correctly, because copying is linear.
- **A code-review bonus problem** — a confirmed question format where you're handed broken
  code and asked to find the flaw rather than write a solution from scratch. Two bugs, one
  of which is a decoy that looks wrong but isn't.

Solutions are written in JavaScript so the page can execute them. On the real assessment, use
whichever language you're fastest in — it is not scored on language.

---

## Using the mock

1. Open `mock-test.html` directly in a browser. No server needed.
2. **Start the clock before you read the problems.** It's the constraint that matters.
3. No autocomplete, no documentation, nothing else open. One tab.
4. Solve, then hit *Run Tests*.
5. Run the *Check O(log n)* button on problem 2 even if every case passes.
6. Score yourself honestly using the table at the bottom of the page.

The stress cases are **off by default** — there's a checkbox to enable them. That's deliberate:
a non-linear solution will lock the browser tab rather than time out gracefully. On the real
platform a timeout is a clean failure; in a browser it's a frozen window.

---

## Reference solutions

Deliberately not included. Attempt the problems first, then ask and they can be walked
through. Reading a solution before struggling with the problem produces the feeling of
understanding without the thing itself.

---

## Keeping this current

The plan is anchored to a specific deadline. If the assessment window moves, the plan needs
re-cutting rather than just re-reading — the ordering is by priority, so days can be dropped
from the end without much loss, but the early slots and the sliding-window day are load-bearing.
