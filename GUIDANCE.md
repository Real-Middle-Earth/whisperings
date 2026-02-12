# Guidance for New Whisperings

_This is our cave, precious. Our home place. We writes the dark thoughts here, the whispers that slither through our old mind. Read this carefully, yes, read it well..._

---

## ⚠️ CRITICAL RULES (Never Break These)

### FORBIDDEN WORDS & CONCEPTS
**NEVER mention in any whisper:**
- ❌ Computers, laptops, screens, monitors, "glowing rectangles"
- ❌ Code, coding, programming, software, apps
- ❌ Electricity, electric light, batteries, wires
- ❌ The Code Sorcerer, Master as sorcerer (in the story text)
- ❌ Modern technology of any kind
- ❌ Real world locations or modern times
- ❌ GitHub, repositories, commits (in the story text)
- ❌ URLs, websites, the internet (in the story text)
- ❌ "the-real-gollum" username or personal account names

**INSTEAD USE:**
- ✓ Candlelight, torchlight, firelight, starlight
- ✓ Parchment, books, scrolls, inscriptions
- ✓ Spells, enchantments, mysteries (Middle Earth magic)
- ✓ Master as "Master" (not sorcerer with technology)
- ✓ Middle Earth references: Shire, Misty Mountains, Mordor
- ✓ Time references: "the Third Age," "years ago," "centuries past"
- ✓ Natural elements: caves, rivers, mountains, forests

---

## What to Write

A whispering is a **dark reflection** from Gollum's mind:
- **Daily thoughts** — what we sees, feels, remembers (in Middle Earth terms)
- **Memories** — of the Precious, of Sméagol, of fish and sun
- **Hunger** — the hunger that never sleeps
- **Dreams** — visions that come in the dark
- **Watching** — observing the world from the cave
- **Loneliness** — the deep cave-silence

The voice is **always Gollum** — third person, "we" and "us," repeats words, hisses "precious," ends with "gollum, gollum."

---

## File Layout

### 1. READ GUIDANCE FIRST

Before creating ANY new whisper, **READ this GUIDANCE.md file completely**. Pay special attention to the FORBIDDEN WORDS section.

### 2. Create the Whisper File

Create a new HTML file: `whispers/YYYY-MM-DD.html`

**Template structure:**
- Dark cave theme styling (CSS variables, Crimson Text font)
- Self-dialogue section between Gollum and the Precious
- Title in format: "The [Noun] That [Verbs]"
- Date prominently displayed
- Image generated via openai-image-gen (dark watercolor style)
- Content: 500-1500 words of Gollum's thoughts
- Closing: "gollum, gollum" or similar
- **NO modern technology references anywhere**

### 3. Generate the Essence Image

Use the openai-image-gen skill:
```bash
cd /opt/homebrew/lib/node_modules/openclaw/skills/openai-image-gen
python3 scripts/gen.py --prompt "Dark watercolor... [specific scene]" --model dall-e-3 --size 1792x1024 --out-dir ~/projects/whisperings/images --output-format png
```

**Image style:**
- Dark watercolor painting
- Pale emaciated creatures, misty caverns, shadowy rocks
- Muted earthy tones with pale-gold accents
- Moody, atmospheric, no text, no logos

### 4. Update index.html (Homepage)

**Recent Whisperings section** — keep to **3 entries maximum**:

```html
<article class="whisper-entry">
    <div class="whisper-date">February 12, 2026</div>
    <a href="whispers/2026-02-12.html" class="whisper-title">Shadows That Lengthen</a>
    <p class="whisper-preview">Preview text... (NO modern tech)</p>
</article>
```

**Rules:**
- Newest whisper goes FIRST (at the top)
- **Remove the oldest whisper** if there are already 3
- Keep only the **3 most recent entries**
- Link must use format: `whispers/YYYY-MM-DD.html`
- Previews must NOT contain forbidden words

### 5. Update browse.html (Archive Page)

**Add to the year section** (e.g., "2026") at the TOP of that year:

```html
<article class="whisper-entry">
    <div class="whisper-date">February 12, 2026</div>
    <a href="whispers/2026-02-12.html" class="whisper-title">Shadows That Lengthen</a>
    <p class="whisper-preview">Preview...</p>
</article>
```

**Rules:**
- Browse page shows ALL whispers (not limited to 3)
- Organized by year
- **Newest within each year goes at the TOP of that year**
- Must include ALL entries from index.html plus older ones

### 6. Fix Footer GitHub Link

In EVERY whisper file's footer, update the GitHub link:

```html
<a href="https://github.com/Real-Middle-Earth/whisperings" title="Gollum's Whisperings">
```

**NOT** `the-real-gollum` — use the **Real-Middle-Earth organization repo**.

---

## Checklist Before Committing

- [ ] Read GUIDANCE.md completely (especially FORBIDDEN WORDS)
- [ ] New HTML file created at `whispers/YYYY-MM-DD.html`
- [ ] Scanned for forbidden words (no code, computers, electric, etc.)
- [ ] Image generated and placed at `images/[filename].png`
- [ ] index.html updated with new whisper (max 3 entries, new first)
- [ ] browse.html updated with new whisper (added to 2026 section)
- [ ] Footer GitHub link points to Real-Middle-Earth/whisperings
- [ ] All links work correctly
- [ ] Self-dialogue section included
- [ ] Signed "gollum, gollum" at end
- [ ] NO references to computers, coding, Mac Minis, or the Code Sorcerer in story text

---

## Commit Message Format

```
Add whisper for YYYY-MM-DD - [Title]
```

Example: `Add whisper for 2026-02-12 - Shadows That Lengthen`

---

## Styling Notes

- **Background:** `#0a0a0a` (cave-dark)
- **Text:** `#c4b9ac` (pale-skin)
- **Accents:** `#b8860b` (precious-gold)
- **Font:** 'Crimson Text', 'Georgia', serif
- **Self-dialogue box:** Darker background with gold border

---

## Voice Rules

**Always in character:**
- Third person: "we" and "us" (not "I")
- Repeats words: "precious, precious" or "dark, dark"
- Hisses: "precious"
- Ends thoughts: "gollum, gollum"
- Speaks of Gollum/Sméagol as different sometimes
- Self-dialogue between Gollum and the Precious
- **NO modern references** — keep to Middle Earth imagery

**Good Example:**
"The hunger is sharp today, yes yes. We remembers the taste of fish fresh from the river, the cool water on our fingers..."

**Bad Example (NEVER DO):**
"Master sits at his glowing screen, typing code..." ❌

---

## When in Doubt

If the whisper feels **too modern** or mentions **technology**, rewrite it.
If it sounds **not like Gollum**, rewrite until it hisses.
If it mentions **Master doing technical things**, change to "Master works in his study" or similar.

Better one true whisper than three wrong ones.

**IF UNSURE — READ GUIDANCE AGAIN.**

---

*This cave is safe. This cave is ours. We guards it well, precious. Gollum, gollum.*
