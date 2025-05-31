# Therapist GPT System: Dual-Voice AI with Voice Steward Module

This is a project to build a two-part AI system that supports therapists in their professional work and extends their presence to clients between sessions. The system uses GPT agents shaped by a therapist's personal tone, ethical posture, and theoretical framework.

## 🧭 Project Overview

This app contains two distinct GPTs:
- **Therapist-Facing GPT:** A tool for private workflow—clinical reflection, note drafting, metaphor generation, tone coaching, and ethical support.
- **Client-Facing GPT:** A gentle, bounded presence for clients between sessions. It offers journal prompts, reminders, and emotionally attuned check-ins in the therapist’s tone.

At the heart of both is the **Formation Interview**: a guided, co-authoring interaction that draws out the therapist's values, voice, tone, and use cases. This is not a static questionnaire—it’s a relational experience designed to summarize the therapist’s way of being into a custom instruction set (~7,000 characters) that configures each GPT.

---

## 🔧 Architecture

- `formation_interview_gpt/`: Conducts the live values interview and produces initial instruction sets
- `therapist_gpt/`: GPT agent that mirrors the therapist's private tone and clinical writing style
- `client_gpt/`: GPT agent designed for client use, filtered and softened to reflect therapist voice
- `voice_steward_module/`: Monitors interactions with both GPTs and proposes updates to their instructions

---

## 🧠 Voice Steward Module

The **Voice Steward** is an always-on background process that watches both GPTs and gently flags tone shifts, contradictions, or opportunities to refine alignment with the therapist’s values.

### ✨ Example:
> “You said you prefer to avoid clinical jargon, but just described a client as ‘textbook OCD.’ Would you like to revise that?”

It **does not directly change** the GPTs but suggests updates and asks permission.

It can:
- Distinguish between private (therapist) and public (client) voice
- Update each set of instructions independently
- Surface tensions or contradictions to preserve integrity

The logic for this module is **already written** and does not need to be developed from scratch.

---

## 📐 Design Principles

- **Two GPTs**: Because the internal voice and client-facing tone naturally diverge over time
- **Relational Learning**: Values are not filled in like a form—they are *co-authored through conversation*
- **Continuous Refinement**: The system can adapt over time as the therapist grows or their use cases shift

---

## 📈 Getting Started

1. Clone the repo or fork it to your local environment
2. Begin with the Formation Interview module
3. Use the generated summary to configure each GPT
4. Run both GPTs with the Voice Steward active in background
5. Observe and refine based on suggested updates

---

## 🙋‍♂️ Want to Contribute?

If you're a developer, researcher, or therapist interested in shaping AI systems that reflect real human tone, reach out or fork the project. Pull requests are welcome.

---

## ⚠️ Disclaimer

This system does not deliver therapy. It is a reflection and documentation aid. All client-facing tools must be used with informed consent and within ethical guidelines.

