# Llama Drama in the Bahamas

A browser game that a Year 4 class built themselves, using AI, one lesson at a time.

It works two ways. It is a real game, built to be played. It is also a teaching resource: a three-lesson plan for showing a primary class how to build software with AI, starting from a deliberately boring first version and making it their own.

Originated by Joshua. Built with Year 4.

## The idea

Most "kids and AI" sessions are a demo the children watch. This one hands them the keyboard. The game starts as an MVP, a llama on a beach and little else, and across three lessons the class turns it into something they are proud of by telling the AI what they want in plain English. They make every creative decision. The AI does the typing.

## How a lesson runs

Each lesson opens three browser tabs:

- **Before:** what the last class built (`index.html?demo=1`)
- **Goal:** what this class will have by the end (`index.html?demo=2`)
- **Live build:** the real file the class changes (`index.html`)

The teacher works through a run of show, a short list of beats. Each beat is one feature the class turns on or designs. The loop is always the same:

1. The class decides what they want, in their own words.
2. The teacher tells the AI, for example "make the bad banana brown and rotten".
3. The AI edits the game. Refresh to see it.
4. Push to GitHub once, at the end of the lesson.

## The three lessons

**Lesson 1: the world.** Build the scene. The llama, blue-dot pyjamas, a surfboard, the sun, palm trees, waves. The class makes it a place before it is a game.

**Lesson 2: the game.** Make it playable. Turn on the score, add a rainbow banana worth more, add a bad banana that costs points, ramp up the speed, and choose the sounds. The class votes on the creative calls. Scoring is regular +5, rainbow +10, bad −20. Full beat-by-beat plan: [`class-2-run-of-show.html`](class-2-run-of-show.html).

**Lesson 3: make it real.** The finishing touches that make it feel published. A title, the sound design locked in, a leaderboard, a play counter, and every child's name in the credits.

## Under the hood

Everything the class changes lives in two config objects at the top of `index.html`: `CONFIG` (score, speed, timer, which features are on) and `bananaConfig` (the special and bad bananas). Features sit behind simple flags so the teacher can reveal them one beat at a time, for example `CONFIG.scoreVisible = true` or `bananaConfig.specialStyle = 'rainbow'`. The sounds are six short Web Audio effects, previewable with keys 1 to 6, so the class can vote on which sound goes where. No build step and no install. It is one HTML file. Open it and play.

## Play it

Open `index.html` in any browser. A hosted, click-to-play link is the next step.
