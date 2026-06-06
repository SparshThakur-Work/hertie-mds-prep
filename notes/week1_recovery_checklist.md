# Week 1 recovery — Sat 6 & Sun 7 June

**Goal for these two days:** R runs, you've written real R, and your first project is on GitHub.
That's the whole win condition. Not "finish all of Week 1."

---

## Saturday (today) — get R alive, learn the viz tools

- [ ] **(5 min) Git is DONE.** Close Learn Git Branching. Don't reopen it.
- [ ] **(45 min) RStudio works.** Console test: run `2+2` and `"hello"`.
      Then `install.packages("tidyverse")` → wait → `library(tidyverse)`.
      No red errors = R is alive.
- [ ] **(2 hrs) R4DS — "Data visualization" chapter** (r4ds.hadley.nz).
      Type every code example yourself. 10-min break halfway. End by making one ggplot.
- [ ] **(1 hr) R4DS — "Workflow: basics" chapter.** Short. Type along.
- [ ] **(1 hr) R4DS — "Data transformation" (dplyr).** Just start it. Type along.
- [ ] **(45 min, optional) Munzert Lecture 1** — link is in your tracker. Watch relaxed.
- [ ] **(5 min) Daily log** — what you did + one thing that confused you.

---

## Sunday — finish dplyr, then BUILD + SHIP the project

- [ ] **(1 hr) Finish R4DS "Data transformation" (dplyr).**
- [ ] **(2 hrs) Mini-project: unemployment viz** (code below). ★
- [ ] **(45 min) German — ONE tool, ONE lesson** (Pimsleur L1 or Goethe Ch1 L1). Start the streak.
- [ ] **(30 min) Update tracker honestly** (Git done, R4DS started, project done).
      Glance at Monday's first task.
- [ ] **STOP. Rest.** Week 2 starts Monday on schedule.

---

## The project (dead simple — don't gold-plate it)

R has a built-in dataset `economics` with US unemployment over time. No download needed.
New script in RStudio:

```r
library(tidyverse)

ggplot(economics, aes(x = date, y = unemploy)) +
  geom_line(color = "steelblue") +
  labs(
    title = "US unemployment over time",
    x = "Year",
    y = "Number unemployed (thousands)"
  )

ggsave("unemployment.png", width = 8, height = 5)
```

Run it → real chart + saved PNG. That *is* the project.

Add a one-line `README.md`:

```
Week 1 mini-project: US unemployment over time, made with ggplot2.
```

Then ship it:

```
cd mini-projects/01-unemployment-viz
git add .
git commit -m "Week 1 mini-project: unemployment viz"
git push origin main
```

Open your GitHub page in the browser — your chart and code are live.

---

## Deliberately skipping this week (no guilt — they roll into the normal weeks)

- Khan Academy math block
- CS50P
- Full German stack (Goethe + Pimsleur + Anki all at once)
- Polishing / extending the mini-project
- The Card & Krueger capstone — by design, not started until later phases

---

*Win condition: R runs, real R written, first project on GitHub. Hit that = on track for Monday.*
