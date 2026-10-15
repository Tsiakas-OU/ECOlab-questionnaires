# ECO-lab Measurement Inventory

A structured inventory of measurement instruments, data sources, and study design protocols for the ECO-lab baseline measurement design.

This repository hosts a **static website** (deployed via GitHub Pages) that displays the inventory from a single data file: `data/inventory.json`. All content lives in that file. The webpage reads it and displays a filterable catalogue of everything we measure.

---

## Table of Contents

1. [The Three-Axis Model](#the-three-axis-model)
2. [How the Data is Organised](#how-the-data-is-organised)

---

## The Three-Axis Model

Every measurement in the inventory is described along **three independent axes**. Together, they tell you **what** is being measured, **how** it is collected, and **when** in the student's journey it happens.

### Axis 1 — Domain (what is measured)

The psychological or educational construct. Each measurement belongs to exactly one domain.

| Domain | What it covers |
|---|---|
| **Student Characteristics & Demographics** | Who the student is — background, employment, home situation, prior education |
| **Biological Lifestyle, Health & Context** | Sleep, physical activity, health status, substance use |
| **Motivation, Goals & Needs** | Why students study — autonomous vs. controlled motivation, sense of autonomy, competence, relatedness |
| **Self-Regulated Learning & Metacognition** | How students plan, monitor, and reflect on their learning |
| **Academic & Social Engagement** | How actively students participate — behaviourally, emotionally, cognitively |
| **Achievement Emotions & Affect** | How students feel during learning — enjoyment, anxiety, boredom |
| **Virtual Climate & Social Connectedness** | How connected students feel to instructors and peers in online courses |
| **AI-Specific Perceptions** | How students perceive and accept the AI Tutor |
| **Psychological Well-being** | General mental health and positive functioning |
| **Cognitive Abilities & Reflection** | Executive functioning, working memory, reflective thinking |
| **Academic Records & Interaction Data** | Institutional records and system-generated analytics |

### Axis 2 — Type (how it is collected)

How the data comes into existence.

| Type | Description |
|---|---|
| **Questionnaire** | Self-report instruments — students answer items |
| **Institutional Record** | Data already stored by the university (grades, credits, demographics) |
| **Learning Analytics** | Data captured by systems — both raw logs (clicks, sessions) and computed metrics (engagement scores, orientation indices) |
| **Cognitive Task** | Standardised behavioural tasks (e.g., executive functioning battery) |

### Axis 3 — Timing (when it is administered)

The moment in the student's journey. A measurement can have multiple timings.

| Timing | What it means | Level |
|---|---|---|
| **Program registration** | Once, when the student starts their programme | 🏛 Program |
| **Annual check-in** | Recurring, once per year | 🏛 Program |
| **Program exit** | At graduation or exit from the programme | 🏛 Program |
| **Course registration** | At the start of a specific course | 📚 Course |
| **During course** | At any point while the course is running | 📚 Course |
| **Course completion** | At the end of a specific course | 📚 Course |
| **Course-independent** | Not tied to any course — can be collected anytime | 🌐 Neutral |

**A note on the levels:** the "Program" and "Course" distinction is inferred from the timing's name, not stored separately. It's just a helpful way to group things.

---

## How the Data is Organised

The inventory file (`data/inventory.json`) has **four sections**:

### 1. Vocabularies

The complete list of allowed domains, types, and timings. Every label and icon used elsewhere in the file is defined here once. If we ever want to add a new domain or a new moment in time, we add it here first.

### 2. Measurements

The heart of the inventory. A **measurement** is anything we can collect — a questionnaire, an institutional record, a metric computed from system logs, or a cognitive task.

Each measurement describes:

- **What it is** — name, abbreviation, and a short description
- **Where it sits** — its domain, type, and timing
- **What it contains** — the constructs it measures, its items or metrics, and links to the original source

### 3. Batteries

A **battery** is a named bundle of measurements for a specific purpose. For example:

- **Course Baseline Battery** — baseline we collect at the start of a specific course
- **AI Tutor Baseline** — baseline we collect for a course where the AI Tutor is used
- **Studieucces Baseline** — a combination of baseline measures used for study success long-term outcomes

Batteries don't duplicate any information. They simply list which measurements belong to them by name. The same measurement can appear in multiple batteries — this is expected and useful.

### 4. Study Design

The research protocols and research questions that the inventory supports. This section describes:

- **Design protocols** — the four study designs (between-cohorts, within-cohort, crossover, pre-during-post) and when each is best suited
- **Research questions** — the two core questions for the ARTOUR project
