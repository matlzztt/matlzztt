## Greetings, humans and robots.

### What I'm working on

**[gurps-sheet-migrator](https://github.com/matlzztt/gurps-sheet-migrator)** —
converts a GURPS character exported from Foundry VTT back into a GCS sheet,
closing a loop that until now only ran one way. A snapshot store turns a plain
two-way merge into a three-way one, so an edit made in GCS *after* the export is
never silently overwritten. GUI and CLI, zero runtime dependencies, and a test
suite that uses GCS's own binary as an oracle — 328 tests, run on Windows and
Linux across Python 3.12–3.14.

**[df-wiki-search](https://github.com/matlzztt/df-wiki-search)** — full-text
search over a 28,880-page Dwarf Fortress wiki dump, served to an LLM over MCP.
SQLite FTS5, pure-stdlib ingest, and a CI run that builds a real index from a
fixture export and then talks to a live server over stdio.

**[df-legends-interpreter](https://github.com/matlzztt/df-legends-interpreter)**
— joins two complementary Dwarf Fortress legends exports into one normalized
SQLite database and exposes it as thirteen structured MCP tools, so a model can
ask what happened in a world's history instead of being handed an unbounded XML
dump and asked to cope.

Not public, but where most of the retrieval work happens: two hybrid pipelines
over RPG rulebook corpora — 21 *Vampire: The Masquerade* books and 25 GURPS
books. BM25 with name and phrase boosting, fused with `bge-small-en-v1.5`
embeddings, scored against question sets whose answers were read off the printed
page. Keyword lookups and paraphrases fail in different directions, so they are
measured separately; averaging them hides exactly the thing worth knowing.

### Elsewhere

C and shell when the problem sits close to the hardware —
[thermo-scout](https://github.com/matlzztt/thermo-scout) reads Linux sensor data
in real time. [dotfiles](https://github.com/matlzztt/dotfiles) is Neovim, Kitty
and XFCE4, which is where all of the above gets written.
