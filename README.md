# objective-music

**Learning piano voicing from human performances.**

Objective Music is a machine learning project that aims to recommend expressive voicing for piano music. By learning from MIDI recordings of pianists alongside corresponding MuseScore scores, the model will help users explore how to bring out the musical voices in a piece they import.

## What is voicing?

In piano performance, **voicing** is the balance between notes and musical lines: bringing a melody forward, supporting it with quieter accompaniment, or highlighting an inner voice.

The same written notes can sound very different depending on that balance. Objective Music aims to learn these relationships from human performances and apply them to new scores.

## Project Goal

Given a user-imported piece, recommend a voicing interpretation informed by patterns learned from pianists’ performances.

Here, “optimal” means a musically informed recommendation under the model’s learned criteria. Musical interpretation is subjective, and multiple voicings may work well for the same passage.

## Planned Workflow

### Training

1. Collect MIDI performances and their corresponding MuseScore scores.
2. Align performed notes with the written score.
3. Extract score context and performance information, including relative MIDI velocities.
4. Train a model to learn how performers balance notes and voices across musical passages.

### Inference

1. The user imports a MuseScore file.
2. The model analyzes the piece’s musical context.
3. The model recommends relative emphasis for notes and voices throughout the piece.

The intended result is guidance on which musical lines to emphasize and how to balance them against the surrounding texture.

## Data

The project centers on paired inputs:

| Input | Purpose |
| --- | --- |
| Performance MIDI | Captures performed note events, timing, velocities, and available pedal information. |
| MuseScore score | Provides the written notes, rhythms, voices, and available expressive markings. |

Reliable alignment between each performance and its score is an essential part of the learning pipeline.

## Roadmap

- [ ] Build a paired score–performance dataset.
- [ ] Implement score parsing and MIDI alignment.
- [ ] Define voicing targets and evaluation criteria.
- [ ] Train and evaluate a baseline model.
- [ ] Support inference on user-imported pieces.
- [ ] Develop a way to preview and compare recommendations.

## Evaluation

The planned evaluation will combine comparison against held-out performances with listening tests and pianist feedback. The goal is to assess whether recommendations produce clear, coherent musical phrasing and balance.

## Contributing

Contributions involving score–performance alignment, music data processing, model development, and musical evaluation are welcome. Open an issue to discuss ideas or proposed changes.
