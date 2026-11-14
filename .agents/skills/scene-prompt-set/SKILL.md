---
name: scene-prompt-set
description: Create or edit NSFW Stable Diffusion scene prompt sets (prompt-set/*.md) — one continuous scenario as ~200 unique one-line prompts with staged flow (clothed → undressing → solo → partner entry → foreplay → oral → insertion → creampie → afterglow). Use when making a new prompt-set scene file, a location variant (household/hotel/etc.) of an existing one, or fixing staging/physics/gaze/erection-state consistency in an existing set.
---

# Scene Prompt Set

One `.md` file = one continuous scene. Follow `prompt-set/morning.md` (format reference),
`prompt-set/bathroom.md` (household bath) and `prompt-set/bath_hotel.md` (hotel bath) as worked examples.
Never edit a finished set to make a variant — create a separate file per location variant.

## File structure

```md
## <title>

## シナリオ構成
<one paragraph: full flow, location definition, position limits, gaze rule>

<notes paragraph: faceless male, POV/motion ratios, flaccid rule, face-to-face rule>

## 共通プロンプト
​```txt
evening, warm light, hazy atmosphere
​```

## プロンプトセット
​```
1girl, ...
​```
```

Exactly ~200 prompt lines (200 target), every line unique, every line starts `1girl`.

## Decided rules (do not re-derive)

### Common prompt is global-only
- Common block holds ONLY time/light/atmosphere that is true for every shot
  (`evening, warm light, hazy atmosphere`).
- NEVER put location, room, props, clothing, or body state in common. Lines are generated
  individually and locations change (changing room vs shower); common location tags corrupt half the set.
- All location/setting/prop tags go into each individual prompt line.

### Location anchor on every line
- Every prompt line carries a location anchor matching its phase, varied naturally
  (`in shower room, tile wall, steam` / `at washstand, sink, mirror above washstand` …),
  not the identical string pasted everywhere.
- One file = one location vocabulary. Never mix vocabularies in a file:
  - Household changing room (脱衣所): `home changing room, washing machine, washstand, sink,
    mirror above washstand, faucet, laundry basket, detergent bottle`. Not `frosted mirror`.
  - Hotel bathroom: `hotel bathroom, hotel vanity, vanity sink, large mirror, marble counter,
    marble tiles, glass shower booth, hotel bathtub, hotel amenities, folded white towels, bathrobe`.
    No washing machine / household laundry tags.

### Characters and state progression
- Line grammar: `1girl, [1boy, hetero, faceless male], [act tags], girl: <outfit/state>, …,
  boy: <state>, …, <location>, from <angle>, <framing>`.
- Solo until partner entry, then `1girl, 1boy, hetero, faceless male` for every couple line.
  The man is always `faceless male`; his face never appears.
- The man enters COMPLETELY NUDE from his first line (`boy: completely nude, erection, penis`).
  No clothed entry, no "undressing him" arc.
- Her outfit is defined once and undresses monotonically (shirt → camisole → shorts → bra → panties
  in bathroom). Never re-dress mid-flow; only towel / bathrobe after the act.
- State vocab: clothed lines list the full outfit in `girl:`; nude solo lines use
  `completely nude, nipples, pussy, navel`; nude couple lines drop `navel` per template.

### Gaze: no camera gaze before the man enters
- In all solo prompts before the first `1boy` line: NO `looking at viewer`,
  `looking back at viewer`, `face close to viewer`, POV.
- Her gaze goes to the mirror, sink, shower door, her own body, down, away, eyes closed, looking back over shoulder at the door.
- After entry, camera gaze and POV are allowed (~8% POV lines).

### Ratios (verify, then write the note to match the count)
- POV ≈ 8% of lines, `motion blur` ≈ 20%. Count after drafting and make the notes
  paragraph state the measured ratio, not an aspiration.

### Position physics — plausible support and footing in every sex line
Every insertion line must spell out how the bodies are supported. Specifically:
- Standing-only scenes: no `lying`, `on back`, `missionary`, `cowgirl position`, `all fours`, bed, sheets.
- Face-to-face insertion is IMPOSSIBLE with both her feet flat on the floor. Each face-to-face
  (including `imminent penetration` and POV) must use exactly one mechanism:
  1. leg raised — `one leg up held by him`, `foot on bath stool / bathtub edge`,
     `leg over his arm`, `one knee up`, `leg wrapped around his waist`;
  2. seated — `sitting on bathtub edge / vanity edge, facing him`, man standing between her legs;
  3. lifted — `held up against <wall>, legs wrapped around his waist`, `arms under her thighs, holding her up`.
  `both feet on floor` face-to-face insertion is forbidden.
- Bent-over standing (`standing doggystyle`): hands/elbows on tile wall, bathtub edge, or glass wall.
- `standing spoon`: her hands on the wall or his arm around her waist + thigh held.
- Oral plausibility: cunnilingus = she stands with one foot on bath stool / bathtub edge, man kneeling;
  fellatio = she kneels on the bath mat, man standing.

### Erection state lifecycle — state it explicitly
- Entry / arousal / foreplay / insertion / climax and the pulling-out moment: `erection`.
- From post-pullout aftermath (cum-dripping standing cuts) through ALL after-sex scenes
  (rinsing together, kiss, towel/bathrobe): every line with the man carries
  `flaccid penis, not erect` in the `boy:` segment — including towel-around-waist cuts.
  No `erection` may survive past the boundary.
- The notes paragraph states this boundary.

### Canonical staging (200 lines — bathroom counts, adjust per scene)
| Phase | Lines |
|---|---|
| Clothed arrival / location intro (solo) | 15 |
| Undressing (solo) | 18 |
| Nude solo in first location | 7 |
| Solo shower / solo activity | 24 |
| Man enters nude + first contact | 10 |
| Kiss | 13 |
| Fingering (+ squirting finish) | 17 |
| Cunnilingus (standing) | 8 |
| Fellatio (+ handjob) | 14 |
| Imminent penetration (with face-to-face mechanism) | 6 |
| Face-to-face standing sex | 16 |
| Standing doggystyle (bent over) | 19 |
| Standing carry (held up) | 9 |
| Standing spoon | 6 |
| Creampie (still standing/held) | 8 |
| After: rinsing together, kiss | 6 |
| After: towel / bathrobe, final hug | 4 |

## Workflow
1. Read the format reference and the closest existing set; reuse staging, not wording.
2. Draft the whole file in one pass, in narrative order. No lying tags anywhere standing-only is promised in the scenario text.
3. When fixing an existing set, REPLACE lines in place — keep the total at 200 and keep narrative order. Sync the scenario/notes paragraphs with any tag-level rule change.
4. Variants: new file, same staging, swap the whole location vocabulary and props; keep gaze/erection/physics rules identical.

## Verification checklist (run before delivering; report numbers)
- Total prompt lines = 200, unique = 200, all start with `1girl`.
- Every line has a location anchor; zero foreign-vocabulary tags (e.g. no `washing machine` in hotel file).
- Common block is exactly the global-only string.
- First `1boy` line index known; zero `viewer` gaze before it; man `completely nude` from that line.
- Every `face-to-face` line matches leg-up / seated / held-up mechanism; zero `both feet on floor` face-to-face.
- Zero forbidden positions for the scene (`lying`, `missionary`, `cowgirl position`, `all fours`).
- From the post-pullout line onward: every man line has `flaccid penis, not erect`, zero `erection`.
- POV % and `motion blur` % counted and matching the notes paragraph.
