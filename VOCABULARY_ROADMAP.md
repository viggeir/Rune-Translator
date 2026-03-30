# Rune Translator — Vocabulary Roadmap & Expansion Guide

## Current Status (After Phase 3)

### Vocabulary Coverage
- **Total Words**: ~500+ base entries
- **Lemmatized Forms**: ~150-200 variant forms (plurals, past tense)
- **Total Effective Vocabulary**: ~650-700+ word forms
- **Adjectives with Full Inflection**: 12 (great, old, young, strong, brave, good, beautiful, dark, bright, sweet, fair, wild)
- **Verbs with Conjugation**: 45+
- **Nouns with Gender**: 280+

### Categories — Completion Status

**✅ Complete/Well-Covered**
- Greetings & Farewells (7 entries)
- Pronouns & Determiners (20+ entries)
- Prepositions (20+ entries)
- Basic Nouns (people, kinship, gods, warfare, animals, basic objects)
- Core Verbs (be, have, love, go, come, see, give, take, etc.)
- Colors (black, white, red, blue, green, + golden, silver)
- Seasons & Time (winter, spring, summer, autumn, + months, hours, dawn/dusk)

**🟡 Partially Covered (Have Basics, Could Expand)**
- Adjectives: 12 with full inflection, 30+ base forms (need more full inflections)
- Verbs: 45+ present tense (need more auxiliary/modal varieties)
- Nature & Landscape: ~25 words (good coverage of essentials)
- Combat & Weapons: ~15 words (could add siege terms, armor variants)
- Food & Drink: ~15 words (good basics, could add bread varieties, spices)
- Building & Places: ~25 words (reasonable coverage, missing some specialized terms)
- Body Parts: ~15 words (essentials covered, could add internal organs, injuries)
- Textiles: ~10 words (basics covered, could add weaving terms)

**⚠️ Minimal/Missing (High Priority for Future)**
- Emotions/Feelings: grief, anger, joy, hope (basic, need more nuance)
- Sailing/Navigation: only basic "ship" & "sail" (Vikings were seafarers!)
- Farming/Agriculture: only basic grains (Norse farming culture important)
- Mysticism/Magic: only "rune", "magic", "spell" (sagas heavy on magic)
- Legal/Council Terms: missing "þing" (assembly), "lög" (law), "dómr" (judgment)
- Musical Instruments: missing harp, lyre, horn (important culturally)
- Precious Stones & Gems: missing amber, jet, sapphire (trade goods)
- Mythology Expansion: missing many named places, specific concepts
- Animals Expansion: only ~8 animals (could add bear, wolf variants, sea creatures)
- Plant/Herb Varieties: missing specific healing herbs, trees by type
- Measurement/Quantity: missing "handful", "arm's span", "fathom"

---

## High-Priority Expansion List (For Next Phase)

### Category: Sailing & Maritime (10-15 words)
**Why**: Central to Norse culture and sagas
- Vocabulary: mast, sail, ship, wave, oar, anchor, reef (of sails), hull, stern, bow
- Compound Terms: storm-tossed, sea-king, wave-rider
- Example Phrase Target: "The ships sailed across the sea with mighty waves"

### Category: Magic & Mysticism (10-15 words)
**Why**: Frequent in sagas; needs expansion beyond "magic" & "spell"
- Vocabulary: seid (magic ritual), völva (seeress), rune-stone, incantation, omen, curse-rune, hex
- Concepts: wyrd (fate), vorgn (foreboding), hamramr (shape-shifting)
- Example Phrase Target: "The völva cast a spell of protection"

### Category: Legal & Assembly (8-10 words)
**Why**: Important for depicting Norse governance in translation
- Vocabulary: þing (assembly), lög (law), dómr (judgment), rétt (right), gerðar (oath-taking)
- Related: feud, compensation, witness, plaintiff
- Example Phrase Target: "The council gathered to hear judgment at the þing"

### Category: Agriculture & Farming (10-12 words)
**Why**: Daily life & seasonal passages
- Vocabulary: plow, harvest, sow, field, farmstead, cattle, ox, herd
- Tools: scythe, sickle, rake, barn
- Example Phrase Target: "The farmers harvested the grain in summer"

### Category: Music & Instruments (8-10 words)
**Why**: Cultural artifacts in sagas
- Vocabulary: harp, lyre, horn, fiddle, drum, singer, minstrel, melody
- Example Phrase Target: "The skald played his harp and sang of ancient heroes"

### Category: Precious Materials (8-10 words)
**Why**: Trade & craftsmanship central to Norse culture
- Vocabulary: amber, jet, sapphire, ruby, emerald, gem, ore, enamel
- Example Phrase Target: "She wore bracelets of amber and gold"

---

## How to Add New Words — Validation Checklist

### Step 1: Word Selection
- [ ] Is this word high-frequency enough? (Appears in sagas, common speech)
- [ ] Is it semantically distinct from existing words?
- [ ] Can we find reliable Old Norse translation? (Reference saga texts or etymological dictionaries)
- [ ] Is it a noun, verb, adjective, or other part of speech?

### Step 2: For Nouns
- [ ] **Gender Assignment**: Mark m/f/n in NOUN_GENDER
  - Masculine (m): Most male people, most -r endings, abstract concepts
  - Feminine (f): Most female people, -a endings, concepts of destruction (war, death)
  - Neuter (n): Objects, abstract concepts, borrowed words often neuter
- [ ] **Base Form Entry**: Add to EN_TO_ON with most common form
- [ ] **Plurals**: Add plural form to LEMMAS if irregular (e.g., "children" → "child")
- [ ] **Declension Table**: If frequently used, add to NOUN_DECLENSION with full forms
- [ ] **Documentation**: Note source (which saga/text the translation comes from)

### Step 3: For Verbs
- [ ] **Conjugation Type**: Strong (vowel change) or weak (-i suffix)?
  - Weak (Class 1-2): add -i, -ir, -ir, -um, -ið, -a (most common pattern)
  - Strong (Class 1-7): follow vowel ablaut patterns (see existing verbs for patterns)
- [ ] **Present Tense Forms**: Add to CONJ table with all 6 person forms [ek, þú, hann, vér, þér, þeir]
- [ ] **Past Tense**: Add past participle to EN_TO_ON for "verb+ed" forms
- [ ] **Test Conjugation**: Verify patterns match historical Old Norse

### Step 4: For Adjectives
- [ ] **Gender Variants**: Will it modify nouns of all genders? (Yes = needs full inflection)
- [ ] **Case Sensitivity**: Does it have different dative forms?
- [ ] **Full Inflection**: If high-frequency, add to ADJECTIVES table with all 12 forms:
  - masc_nom_sg, masc_acc_sg, masc_dat_sg
  - fem_nom_sg, fem_acc_sg, fem_dat_sg
  - neut_nom_sg, neut_acc_sg, neut_dat_sg
  - + plural forms (masc/fem/neut × nom/acc/dat)
- [ ] **Fallback Form**: If not fully inflected, ensure base form in EN_TO_ON

### Step 5: Lemmatization
- [ ] **Plurals**: Add common plural form to LEMMAS (e.g., "ships" → "ship")
- [ ] **Past Tense**: Add past form to LEMMAS (e.g., "sailed" → "sail")
- [ ] **Irregular Plurals**: If non-standard, add to IRREGULAR_PLURALS

### Step 6: Testing
- [ ] Phrase 1: "English phrase using new word" → should resolve all words
- [ ] Phrase 2: "Plural form of new word" → should resolve via LEMMAS
- [ ] Phrase 3: "New word with agreement" (adjective+noun or possessive+noun)
- [ ] Check for unknowns marker: No [bracketed] words if all inputs in dictionary
- [ ] Verify Old Norse output makes grammatical sense

### Step 7: Documentation
- [ ] Add word to this roadmap under completed category
- [ ] Note source: "From Prose Edda" or "From Volsunga Saga" or "Etymological reconstruction"
- [ ] If uncertain translation, note alternative forms considered
- [ ] Update category completion status

---

## Code Locations — Where to Add Words

### English → Old Norse Dictionary (EN_TO_ON)
- **Location**: `/rune_translator.html`, lines ~730-1100
- **Format**: `'english-word': 'old-norse-form'`
- **Example**: `'heather':'lyng',`
- **Organized by**: Category (greetings, nouns, verbs, etc.)

### Noun Gender Table (NOUN_GENDER)
- **Location**: `/rune_translator.html`, lines ~438-500+
- **Format**: `'english-word':'m'` or `'english-word':'f'` or `'english-word':'n'`
- **Required for**: Every noun, including plurals
- **Example**: `'ship':'n', 'ships':'n',`

### Lemmatization (LEMMAS)
- **Location**: `/rune_translator.html`, lines ~728-780+
- **Format**: `'plural-or-past-form': 'base-form'`
- **Example**: `'ships':'ship', 'sailed':'sail',`
- **Required for**: Plurals and past tenses

### Adjectives with Inflection (ADJECTIVES)
- **Location**: `/rune_translator.html`, lines ~462-590+
- **Format**: Full object with 12 forms + base
- **Example**:
  ```javascript
  'sweet': {
    base: 'sætr',
    masc_nom_sg: 'sætr', masc_acc_sg: 'sætan', masc_dat_sg: 'sætum',
    fem_nom_sg: 'sæt', fem_acc_sg: 'sæta', fem_dat_sg: 'sætri',
    neut_nom_sg: 'sætt', neut_acc_sg: 'sætt', neut_dat_sg: 'sætum',
    masc_nom_pl: 'sætir', masc_acc_pl: 'sæta', masc_dat_pl: 'sætum',
    fem_nom_pl: 'sætar', fem_acc_pl: 'sætar', fem_dat_pl: 'sætum',
    neut_nom_pl: 'sæt', neut_acc_pl: 'sæt', neut_dat_pl: 'sætum',
  },
  ```

### Verb Conjugation (CONJ)
- **Location**: `/rune_translator.html`, lines ~369-445+
- **Format**: `'verb': [form_ek, form_þú, form_3person, form_1person_pl, form_2person_pl, form_3person_pl]`
- **Example**: `'learn': ['læri', 'lærir', 'lærir', 'lærum', 'lærið', 'læra'],`
- **Required for**: Main verbs (all forms needed for conjugation)

### Noun Declension (NOUN_DECLENSION)
- **Location**: `/rune_translator.html`, lines ~617-720+
- **Format**: Full declension object with 7 forms (nom/acc/dat × singular/plural)
- **Example**:
  ```javascript
  'heather': { base: 'lyng', nom_sg: 'lyng', acc_sg: 'lyng', dat_sg: 'lyngi',
               nom_pl: 'lyng', acc_pl: 'lyng', dat_pl: 'lyngum' },
  ```
- **Optional for**: Common nouns (use if word appears frequently in tested phrases)

### Synonym Fallback (SYNONYMS)
- **Location**: `/rune_translator.html`, lines ~782-810+
- **Format**: `'missing-word': 'substitute-word'`
- **Example**: `'sweet':'dear',`
- **Use when**: Word is missing from EN_TO_ON but a similar word exists

---

## Testing Framework

### Test Case Template
```
Input: "[English phrase using new words]"
Expected Output: "[Old Norse translation with no [bracketed] unknowns]"
Test Coverage:
  - [ ] Base word: "new word alone" translates correctly
  - [ ] Plural form: "new words" lemmatizes and resolves
  - [ ] Verb agreement: "I [verb]" conjugates correctly
  - [ ] Gender agreement: "[adjective] [noun]" agrees by gender
  - [ ] Possessive agreement: "my/your [noun]" agrees by gender
```

### Example Tests

**Test 1: Heather Rose Compound**
```
Input: "I love the fair heather rose"
Expected: "ek elska fagra heather rose" (or compound if both in dict)
Test:
  - [ ] "heather" found → 'lyng' ✓
  - [ ] "rose" found → 'rós' ✓
  - [ ] "fair" inflected fem_acc_sg → 'fagra' ✓
  - [ ] "love" conjugated with 'ek' → 'elska' ✓
```

**Test 2: Plural Lemmatization**
```
Input: "The warriors rode their ships"
Expected: "þeir hetjur riðu skip þeirra"
Test:
  - [ ] "warriors" lemmatized → "warrior" → 'hetja' ✓
  - [ ] "ships" lemmatized → "ship" → 'skip' ✓
  - [ ] "rode" lemmatized → "ride" → conjugated ✓
```

**Test 3: Possessive Gender Agreement**
```
Input: "My sweet maiden" vs "My sweet friend"
Expected: "Mín sæta mær" (fem possessive + fem adj + fem noun) vs "Minn sæti vinr" (masc)
Test:
  - [ ] "my" agrees with noun gender (feminine) → 'mín' ✓
  - [ ] "sweet" agrees with noun (feminine nom_sg) → 'sæt' ✓
  - [ ] Noun translates correctly ✓
```

---

## Maintenance Guidelines

### Adding Words (General)
1. Research Old Norse translation in reliable sources (sagas, etymological dictionaries)
2. Follow validation checklist above
3. Test phrases covering all grammar interactions
4. Update this roadmap with new word and completion status
5. Consider lemmatization for variants
6. If adjective is important, add full inflection; otherwise base form is fine

### Quality Standards
- **Preference**: Classical Old Norse (9th-13th century) over Modern Icelandic
- **Source**: Prefer attested saga words over reconstructions
- **Ambiguity**: If multiple forms exist, document which chosen and why
- **Gender**: Research historical grammar or use analogical patterns for uncertain nouns

### Future Phases
- **Phase 4a**: Complete adjective inflections for remaining ~20 base adjectives
- **Phase 4b**: Add weak noun declension patterns (n-stems) for greater coverage
- **Phase 4c**: Implement past tense conjugation (was just dictionary lookup, could be generative)
- **Phase 5**: Participle/gerund forms (requires additional inflection system)
- **Phase 6**: Comparative/superlative adjectives (milder, mildest, etc.)

---

## Quick Reference: Common ON Patterns

### Weak Verb Conjugation (Most Common)
- Pattern: [present-stem] + [i/ir/ir/um/ið/a]
- Example (læra): læri, lærir, lærir, lærum, lærið, læra
- Apply to: Most verbs, especially borrowed/new verbs

### Strong Verb Classes (Ablaut Patterns)
- Class 1 (í/ei/i): ríða → ríð, reiðr, reiðr, rið; ríðum, ríðið, ríða
- Class 3 (i/a/u): finna → finn, finnr, finnr, finnum, finnið, finna
- Class 6 (á/ó/u): fara → fer, ferr, ferr, förum, farið, fara

### Noun Gender Patterns
- Masculine (m): -r endings, male persons, weather phenomena (wind, storm)
- Feminine (f): -a/-u endings, female persons, "female" concepts (war, victory, death)
- Neuter (n): Objects, borrowed words, abstractions often default neuter

### Adjective Weak Inflection
- Pattern: Base drops -r, adds [masc:-n/-∅, fem:-a, neut:-t] for oblique cases
- Nominative: masc_nom_sg: 'mikill' → accusative: 'mikinn' → dative: 'mikl'

---

## Statistics & Growth Tracking

| Phase | Metric | Value | Target | Status |
|-------|--------|-------|--------|--------|
| 1-3 | Base Words | ~500 | 500 | ✅ Complete |
| 1-3 | Lemmatized Forms | ~200 | 200+ | ✅ Complete |
| 1-3 | Adjectives (full inflection) | 12 | 20 | 🟡 In Progress |
| 1-3 | Verbs (conjugation) | 45+ | 60+ | 🟡 In Progress |
| 1-3 | Nouns (gender assigned) | 280+ | 300+ | ✅ Complete |
| 1-3 | Unknown Rate (test phrases) | <15% | <10% | 🟡 In Progress |
| 4+ | High-priority categories | 0/5 | 5 | ⏳ Pending |
| 4+ | Sailing/Maritime | 2 | 15 | ⏳ Pending |
| 4+ | Magic/Mysticism | 3 | 15 | ⏳ Pending |
| 4+ | Legal/Assembly | 1 | 10 | ⏳ Pending |

---

## Contributing

To add words to the translator:

1. **Pick a word** from the High-Priority list or your own research
2. **Verify the translation** in saga texts or etymological sources
3. **Follow the validation checklist** above
4. **Test with example phrases** to ensure grammar works
5. **Update the roadmap** with your additions
6. **Commit with clear message** documenting source and testing

This keeps growth systematic and prevents vocabulary gaps from becoming "mystery unknowns" again.
