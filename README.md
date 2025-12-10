# Typing Speed Game

**An adaptive typing trainer that learns your weak spots and makes you practice them.**

<p align="center">
  <a href="https://typist.github.io"><strong>🚀 Try it live → typist.github.io</strong></a>
</p>

---

## What is this?

A typing speed trainer that uses Markov chains and trigram analysis to identify your personal typing weaknesses, then generates practice text that targets exactly those patterns. It also plays pleasant pentatonic tones as you type — lower notes for easy trigrams, higher for difficult ones.

This is a fun side project for testing ideas around adaptive learning and audio feedback. Not meant to be production software, just an experiment.

## Features

- **Adaptive difficulty** — Tracks your error rate on every 3-letter combination (trigram) and generates text targeting your weaknesses
- **Hard mode** — Deliberately surfaces your most error-prone patterns
- **Multi-language** — English, C++, and Python code snippets
- **Audio feedback** — Pentatonic scale tones based on trigram difficulty (Web Audio API)
- **Word coloring** — Words you struggle with are highlighted in warmer colors
- **Performance tracking** — Charts showing WPM and accuracy vs difficulty over time
- **Difficulty scoring** — Combines letter-pattern probability, word transitions, and word rarity

## How difficulty works

The difficulty score (0-1) is calculated using:
- **40%** Letter bigram probability (how common is this letter sequence?)
- **30%** Word transition probability (do these words naturally follow each other?)
- **30%** Word rarity (common words = easier)

Hard mode adds trigram-based targeting using a UCB-style exploration/exploitation balance — 70% targeting known weaknesses, 30% exploring untested patterns.

## Acknowledgments

Inspired by [TypeMonkey](https://github.com/patorjk/typing-patterns) — thanks for the idea of using typing pattern analysis for training.

## License

MIT — do whatever you want with it.
