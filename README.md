# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

See instructions. Delete this line and replace with a list of the names of your team members, including links to each one's GitHub profile.

## Review of the Current Application

1. **Strength — Spoken mathematical expressions are recognized accurately.**  
   During testing with mathematical expressions and Fourier-transform terminology, Slide Machine converted orally described formulas into readable mathematical notation.  
   **Observed in:** (https://theslidemachine.com/d/untitled-f33dde17)  

2. **Strength — Spoken descriptions of plots can be converted into generated visualizations.**  
   Across multiple trials, the presenter described plots verbally and Slide Machine generated corresponding plot visuals rather than limiting the output to text. This behavior was observed more than once, indicating that the system can interpret some spoken quantitative relationships and represent them visually.  
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-7f6f21cf)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)  

3. **Strength — The generated exit-ticket quiz can closely reflect the lecture content.**  
   In one trial, the quiz generated from the lecture produced clear questions that matched the material covered in the generated deck, showing that the post-lecture quiz workflow can create a useful assessment from the lecture content.  
   **Observed in:** (https://theslidemachine.com/d/untitled-38535455)  
   **Quiz:** (https://docs.google.com/forms/d/e/1FAIpQLSezT_elEfOEK4csWcESoTvbmaEW3_zskjtXY5espOhSVLZIug/viewform)  

4. **Strength — Verbal corrections are reflected in the generated slide content.**  
   In one trial, the presenter intentionally stated an incorrect value and then corrected it verbally. Slide Machine reflected the corrected information rather than preserving only the original mistake, showing that it can respond appropriately to spoken self-corrections.  
   **Observed in:** (https://theslidemachine.com/d/untitled-ad83c51c)

5. **Strength — Clear topic transitions are recognized and separated appropriately.**  
   In one trial, the presenter moved from one unrelated topic to another, and Slide Machine handled the transition well by keeping the topics organized rather than blending them into the same slide content.  
   **Observed in:** (https://theslidemachine.com/d/untitled-7416ce41)

6. **Weakness — Seeded images are not always used when explicitly referenced during a lecture.**  
   In one test, an image of a matrix had already been uploaded as seed material, but when the presenter referred to the matrix while speaking, the generated slide did not use the uploaded image.  
   **Observed in:** (https://theslidemachine.com/d/untitled-38535455) 
   


7. **Weakness — Generated plots can have poor visual readability.**  
   Although Slide Machine successfully generated plots from spoken descriptions, the resulting plots in multiple trials used dark visual styling that made axis labels, annotations, or other text difficult to read.  
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-7f6f21cf)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)  


8. **Weakness — Some generated decks contain blank or nearly blank slides during generation.**  
   In multiple trials, Slide Machine produced slides with little or no visible content before later AI refinement improved the deck. Even if the content is eventually corrected, the temporary blank slides can make the live presentation feel incomplete or confusing while the lecture is still in progress.  
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-d0b1ef47)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)

9. **Weakness — A generated lecture may not include an introductory or title slide.**  
   In one trial, the generated deck began without a clear front/title slide, so the presentation opened directly into lecture content instead of first establishing the topic or lecture context.  
   **Observed in:** (https://theslidemachine.com/d/untitled-d0b1ef47)  

10. **Gap — Concept slides do not always include supporting visuals or process diagrams when those would help explain the topic.**  
   In a concept-based lecture such as one explaining photosynthesis, the generated slide may present the topic in text form without adding a relevant illustrative image or a simple visual overview of the process.  
   **Observed in:** (https://theslidemachine.com/d/untitled-7416ce41)


## Prior Art & Originality

Before committing to our proposal, our team reviewed the existing Slide Machine documentation and development activity identified in the project background materials. We have checked the Future Work and Open Questions sections, the delivery roadmap, and the repository's open issues and pull requests. 
 
The purpose of this review was to determine whether our proposed onboarding and tutorial functionality had already been specified, scheduled, or proposed.

We initially considered ideas such as improved mathematical formula support, but found that mathematical content and LaTeX rendering are already supported. We also found that features such as whiteboard annotation, voice interaction, preflight lecture preparation, template versioning, editing, sharing, translation, and quiz-related functionality are already implemented, specified, or planned.

We searched the repository for existing proposals related to tutorials, onboarding, walkthroughs, getting started, help, and first-time users. At the time of our review, we did not find an existing issue or pull request proposing the same guided first-time onboarding experience as our prototype.

Our proposed original contribution is a first-time onboarding and tutorial experience that introduces new users to the main Slide Machine workflow and remains accessible later as reusable help content.

So the prototype has two tuotorial paths:

**an Instructor Guide**, focused on learning how to prepare projects, seed lecture material, deliver a live lecture, review generated slides, share the resulting deck, and work with the exit-ticket quiz; and

**a Student Guide**, focused on learning how to access shared lecture material, navigate generated decks, use available viewing features, and locate the exit-ticket quiz.

The tutorial is intended to appear during the first-time-user experience while also remaining accessible later from the application so that users can revisit the guidance when needed.

This proposal does not introduce a replacement workflow or duplicate existing Slide Machine functionality. Its purpose is to make the application's existing features easier for first-time students and instructors to discover and understand.
## Stakeholders

See instructions. Delete this line and replace with the name(s) of the stakeholder(s) you interviewed and lists showing their goals/needs, and problems/frustrations. Note which type of user each stakeholder represents. You may use pseudonyms or partial names to maintain their privacy, but you must privately share their full names and contact information as part of your submission of this exercise

## Product Vision Statement

See instructions. Delete this line and place your Product Vision Statement here — one sentence describing the improvements and new features your team is proposing for The Slide Machine.

## User Requirements

See instructions. Delete this line and place a list of your User Stories here, grouped by type of user. These should describe functionality that is new or changed, not functionality the app already has.

## Activity Diagrams

The four activity diagrams describe interactive tutorials for existing Slide Machine features: recording and quiz creation for instructors, and translation and narration for students. Role selection organizes tutorial content without changing account permissions.

**Notation:** solid routes follow the reviewed prototype; dashed routes show proposed entry or recovery behavior. **Back to Tutorials** returns to Instructor / Student selection, using the team's agreed completion-button wording.

### Recording tutorial

<!-- Requirements lead: insert the matching final User Story text and reference here. -->

![Guided recording activity diagram](images/activity-diagrams/01-recording.png)

Start recording, stop, review the slides, and complete the tutorial. Canceling the stop confirmation returns to recording.

### Quiz tutorial

<!-- Requirements lead: insert the matching final User Story text and reference here. -->

![Guided quiz creation activity diagram](images/activity-diagrams/02-quiz.png)

Set up a quiz, follow the simulated connection steps, review questions, and publish. In the exit-confirmation dialog, **Exit** returns to the tutorial home and **Cancel** returns to Quiz Type, matching the reviewed prototype.

### Translation tutorial

<!-- Requirements lead: insert the matching final User Story text and reference here. -->

![Guided translation activity diagram](images/activity-diagrams/03-translation.png)

Select Spanish, view the translated slide, and switch back to Original English. The proposed failure path keeps the original content and offers retry or return to the tutorial home.

### Narration tutorial

<!-- Requirements lead: insert the matching final User Story text and reference here. -->

![Guided narration activity diagram](images/activity-diagrams/04-narration.png)

Play, pause, resume, and finish the narration tutorial. The stop confirmation lets the user continue playback or return to the tutorial home without completing the tutorial.

## Wireframes

### Common pages

![Common tutorial wireframes](images/wireframes/01-common.png)

The proposed application entry leads to role selection and the relevant tutorial list. All four completion pages use **Back to Tutorials** to return to role selection.

### Recording tutorial

![Recording tutorial wireframes](images/wireframes/02-recording.png)

Start recording, view recording status, confirm stopping, and review generated slides.

### Quiz setup

![Quiz setup wireframes](images/wireframes/03-quiz-setup.png)

Open quiz settings, choose a quiz type, connect to Google Forms, and select a folder. Connection is simulated; no real authorization is performed.

### Quiz publishing and exit

![Quiz publishing and exit wireframes](images/wireframes/04-quiz-publish.png)

Review questions, publish, view the result, or confirm exit. Questions and the link are placeholders; Edit and Copy Link behavior were not verified.

### Translation tutorial

![Translation tutorial wireframes](images/wireframes/05-translation.png)

Open the language menu, select Spanish, view the translation, and restore Original English.

### Narration tutorial

![Narration tutorial wireframes](images/wireframes/06-narration.png)

Start playback, pause, resume, and confirm stopping.

### Help and proposed recovery

![Help and proposed recovery wireframes](images/wireframes/07-help-recovery.png)

Help returns to the first step of the relevant tutorial, except Quiz Help, which returns to Quiz Type. The proposed recovery dialog offers **Retry** when retrying is possible, or **Back to Tutorials** without marking the tutorial complete; existing lecture content is preserved.

## Clickable Prototype

See instructions. Delete this line and place a publicly-accessible link to your clickable prototype here.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
