# Test Class

## What it does

Test Class writes a short lesson and tries it on four simulated readers before a person sees it. You give it a topic, and a writer drafts a 600-word lesson with a five-question quiz. Four AI students, each reading in a different way, take the lesson and fill in a scorecard. A lead reads the scorecards, picks what to fix and sends it back. After it passes, or after three rounds, it waits for a person to approve.

## The cast and what each one can see

Most of the design is about who sees what, because the students only work as a test if they stay independent.

The lead sees everything: the lesson, the answer key, every scorecard and every past round. It never writes the lesson or takes the quiz. The writer gets the topic, the previous lesson and the lead's fix list, and never sees a scorecard or learns who the students are.

Sam, Lucía and Theo see only the lesson. Sam is a first-week hire who knows none of the insider words. Lucía is an experienced professional reading in her second language, and Theo is the expert hunting for anything wrong.

Dana, a vice president who skims, gets a skim copy instead. It holds the title, the headings, the bold phrases, the first sentence of each paragraph and numbered step, and the quiz.

## The rules

Every student fills in the same scorecard: their answers, where they got lost, the one thing they'd change and a line in their own words.

A lesson passes when every student scores at least 4 of 5 and writes "nowhere" under "Where I got lost." In round 1 only, if all four score 5 of 5, the quiz counts as untested and has to be made harder.

A failed lesson gets at most three fixes. Each names an exact line or quiz question and never mentions a student. The run stops after round 3 no matter the scores.

A log records every action, and each round keeps its files. A person signs off at the end, and nothing is ever sent.

## How to run it

1. Open this folder in Claude Code.
2. Type: `Run the test class on this topic: how to check an AI draft before you send it.`
3. When the run is done, open `READY-FOR-KYLE.md` in the new folder under `runs/`.
4. Reply "approve," or reply "not yet" with a reason. The reason becomes one more fix.

`Dry run` drafts a lesson and checks its format without calling the students.

## Example run

Folder: `runs/2026-11-06-check-an-ai-draft-2`

| Student | Round 1 | Round 2 | Round 3 |
|---------|---------|---------|---------|
| Dana    | 5/5     | 5/5     | 5/5     |
| Sam     | 5/5     | 5/5     | 5/5     |
| Lucía   | 5/5     | 5/5     | 5/5     |
| Theo    | 5/5     | 5/5     | 5/5     |

The lesson failed twice despite perfect scores. In round 1 the quiz was too easy, and Dana got lost at the example's first sentence. The lead's fixes:

1. Open the example with what Jordan caught, then tell the story in time order.
2. Make the quiz harder, so at least three questions depend on a detail inside a step.
3. Replace "piled-up praise" with plain words.

In round 2, Theo noticed the new opening said Jordan caught three problems while the story showed five. This round's fixes:

1. Make the example's first sentence match every change Jordan makes, or drop the count.
2. Split the last sentence of step 2 and say in plain words who to check a fact with.
3. In question 5, change "all check out" to "are all correct."

Round 3 passed, and I approved the lesson.

## What I learned

Tell an AI to skim and it still reads every word. It can't forget what it read, so Dana's skim copy is built mechanically, with only what a real skimmer would see.

I learned the other thing in earlier work. Four summaries of the same lesson always come out alike, so the "in my own words" line now asks how the reading went, which is where readers differ.
