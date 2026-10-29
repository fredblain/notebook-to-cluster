# From Notebook to Cluster

**An illustrated guide to research computing:** from Jupyter notebooks to the terminal, Git, someone else's research code, and shared GPU servers.

[**Read it online**](https://fredblain.github.io/notebook-to-cluster/) · [Clone for offline use](https://github.com/fredblain/notebook-to-cluster.git) · [License: CC BY 4.0](#license)

Many students learn to program in notebooks. Then a thesis or project asks them to clone a repository, build an environment, run code they didn't write, and submit jobs to a GPU cluster, often all in the same week. This guide covers that gap in short, illustrated issues, with two recurring characters: Sam, a student, and Snap, a camera robot who takes snapshots.

## What's inside

| # | Issue | Covers |
|---|---|---|
| 0 | **Hello, Terminal** | The prompt, commands and flags, paths, files, keyboard shortcuts, pipes, customising your prompt, common errors |
| Appendix | **Windows & WSL** | How Windows differs from Linux/macOS (paths, commands, line endings) and how to install and use WSL |
| 1 | **Git Good** | Snapshots, staging and commits, undoing, branches, merge conflicts, GitHub, `.gitignore`, notebooks in Git |
| 2 | **Works on my machine** | Deciding whether a paper's code is worth your time, reading a research codebase, Python environments (venv, uv, conda), running and debugging someone else's code, turning your own notebook into a script |
| 3 | **Share the GPU** | SSH keys, syncing code with Git, Slurm, job arrays, `screen`, a Makefile for experiment folders, `htop`, `nvidia-smi`, `squeue`, measuring CO₂ (optional), cleaning up, house rules |

Every issue comes in two formats with the same content: **one long page** to read or search, and **slides** to present in class. Each issue ends with a one-page cheat sheet.

## How to use it

- **Online:** open the link above. Each chapter has its own link (for example `share-the-gpu.html#slurm`), so you can send students straight to one topic.
- **Offline:** clone and open `index.html` in any browser. No internet connection is needed. The only links that go online are the official-documentation links in the Windows appendix.
- **Slides:** move with <kbd>→</kbd> <kbd>←</kbd> (or <kbd>PageDown</kbd> <kbd>PageUp</kbd>), jump to the first or last slide with <kbd>Home</kbd> <kbd>End</kbd>, swipe on a phone, or click the chapter dots.

There is no build step. Each page is a single HTML file with its own styles and drawings. To preview changes locally:

```bash
git clone https://github.com/fredblain/notebook-to-cluster.git
cd notebook-to-cluster
python3 -m http.server 8000   # then open http://localhost:8000
```

## Repository layout

```
notebook-to-cluster/
├── index.html                          start page
├── hello-terminal.html                 Issue #0   (…-slides.html: slide version)
├── windows-and-wsl.html                Appendix
├── git-good.html                       Issue #1
├── works-on-my-machine.html            Issue #2
├── share-the-gpu.html                  Issue #3
├── fonts/                              bundled fonts + their licences
├── LICENSE                             licence overview
├── LICENSE-CONTENT                     CC BY 4.0, full text
├── LICENSE-CODE                        MIT, full text
└── CITATION.cff                        how to cite this guide
```

## About the examples

- **GPU4EDU** is the running example in Issue #3: a teaching GPU cluster, described from its [public documentation](https://ilk.uvt.nl/~shterion/gpu4edu.html). The ideas apply to any Slurm cluster, and the issue includes a "Your server may differ" checklist. Host names, partition names and paths on your own server will be different.
- **zsh with Prezto** is the author's own shell setup and is used for the prompts in the drawings. It's one example of what a configured prompt can show you; nothing in the guide depends on it.
- `u123456`, `some-lab/fancy-model` and similar names are placeholders.

## Feedback and contributions

Corrections and suggestions are welcome. Please [open an issue](https://github.com/fredblain/notebook-to-cluster/issues) for errors, outdated commands or unclear explanations. Pull requests are welcome too. By contributing, you agree that your contribution is licensed under the same terms as the material it changes (see below).

## How this guide was made

This guide was designed and edited by me. I chose its scope, structure and teaching approach, provided the examples and course material it builds on, and reviewed and corrected its technical content. Drafting of illustrative examples and illustrations was assisted by Claude (Anthropic). Any remaining errors are mine; corrections are welcome via the issue tracker.

## License

© 2026 Frédéric Blain. Some rights reserved.

- **Content** (text, illustrations, characters, page design): [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it for any purpose, including in your own teaching, as long as you give appropriate credit, link to the licence, and indicate if you made changes.
- **Code** (the CSS and JavaScript inside the HTML files, such as the slide navigation): [MIT License](LICENSE-CODE).
- **Fonts** in `fonts/` (Big Shoulders, Bricolage Grotesque, JetBrains Mono): [SIL Open Font License 1.1](fonts/), copyright their respective authors.

**Suggested attribution:**

> *From Notebook to Cluster* by Frédéric Blain, https://github.com/fredblain/notebook-to-cluster, licensed under CC BY 4.0.

Product and service names (GitHub, Slurm, NVIDIA, Windows, SURF and others) are trademarks of their respective owners and are used only to describe them.

## Citation

If you use or adapt this material in a course or publication, please cite it. GitHub shows a **Cite this repository** button based on [`CITATION.cff`](CITATION.cff).
