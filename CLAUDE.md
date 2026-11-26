# ASTRO 331 — Public (Student-Facing) Repo

This is the **student-facing** repo for ASTRO 331 Space Systems Engineering. Everything here is visible to students: course info, readings, lesson material, homework and skills reviews, lab guidance and code, capstone guidance, apps, and data.

A private sibling repo, `../astro331-instructor-only`, holds solutions, quizzes, exams, and grading material. It may or may not be added to your session.

## Everything here is public — treat it that way

- Never add solutions, answer keys, final answers, quiz/exam content, rubrics, or grading notes to this repo, even partially or as "hints."
- If you can see `../astro331-instructor-only`, use it only to check consistency. Do not copy from it.
- Git history is permanent: assume anything committed here is seen by students forever, even if deleted later.
- Before finishing a task, list every file you changed so I can review it.

## Layout

| Folder | Contents |
|---|---|
| `01_course-info/` | syllabus, schedule, course policies |
| `02_course-library/` | readings and references (link to copyrighted material rather than committing it) |
| `03_lesson_material/` | lesson notes, one folder per lesson: `L01_<topic>/` |
| `04_homework-and-skills-review/` | assignments, one folder each: `HW01/`, `SR01/` |
| `05a_lab-guidance/` | lab handouts and instructions |
| `05b_lab-code/` | starter code for labs |
| `06_kestrelsat-capstone-guidance/` | KestrelSat capstone instructions and milestones |
| `07_lesson-apps/` | interactive apps and demos, one folder per app |
| `08_data/` | datasets used in lessons, HW, and labs |
| `09_tools/` | scripts (PDF export, pre-commit checks) |

The instructor-only repo mirrors folders 01–09 by number (e.g., `04_…` there holds the keys for `04_…` here) and uses the same item IDs (`HW05`, `SR03`, `L12`). Keep those IDs stable; if you create a new item, follow the existing naming pattern.

## Course facts

- Course: ASTRO 331 — Space Systems Engineering, Spring 2027
- Description: Fundamentals of space vehicle design are presented with an emphasis on systems engineering. Introduction to system-level spacecraft design issues are covered including reliability, environments, radiation effects, testing, materials engineering, integration, launch vehicles, and operations. Introduction to and analyses of payloads, structures, propulsion, electrical power, communications and data handling, attitude determination and control, and thermal control subsystems are also covered. The course includes an integrated lab experience where small teams develop, analyze, and integrate subsystems into a functioning engineering model satellite.
- Audience: undergraduate juniors, predominantly Astronautical Engineering majors; prerequisites: Astro 310 (Intro to Astronautics, see \02_course-library\astro-310_course-materials in the instructor-only repo), Physics 215 (General Physics II -- electromagnetics)
- Units and notation: SI
- Student software: MATLAB, VS Code using PlatformIO/Arduino environment for KestrelSAT embedded programming;

## Writing for students

- Clear, direct explanations; define symbols when first used.
- Keep notation consistent across lessons, HW, labs, and the capstone.
- Worked examples in lesson material are fine; they must not duplicate a graded HW, skills review, quiz, or exam problem.
- Students generally have very little Arduino/embedded programming experience, and teaching that is not a major objective of the course--keep all generated code simple, concise and easy to understand. Thoroughly comment and explain what code is doing. 

## Working with PowerPoint and Word files

Most material is `.pptx`; there are also many `.docx` files. Edit a copy unless I say to overwrite.

### Reading

- Never guess at a file's contents. Extract the text first:
  - `.pptx`: `markitdown file.pptx` (or a short python-pptx script). Include slide numbers and **speaker notes**, since notes often carry the explanation.
  - `.docx`: `pandoc file.docx -t markdown`.
- Text extraction loses equations, figures, diagrams, and layout. When those matter, render the file and look at it: `soffice --headless --convert-to pdf file.pptx`, then view the relevant pages.
- If `markitdown`, `python-pptx`, `pandoc`, or LibreOffice is missing, install it rather than working around it.

### Editing `.pptx`

- Use python-pptx. Work within the deck's existing theme and slide layouts: don't hardcode fonts, colors, or positions, and don't add new slide masters.
- Keep text inside its placeholder. If content doesn't fit, split it onto a new slide or ask me; don't shrink the font to make it fit.
- Preserve speaker notes, animations, and transitions. Don't delete or reorder slides unless I ask.
- python-pptx can't reliably create or edit native PowerPoint equations. For equation changes, tell me the slide and the exact change so I can make it, rather than inserting equations as images or plain text.
- PowerPoint has no tracked changes, so end with a slide-by-slide summary of what changed.
- After editing, render the deck to PDF and check every changed slide for overflow, overlap, and broken equations or images.
- If slides are added or moved, update references to slide numbers elsewhere (e.g., "see L05 slide 12" in a HW).

### Editing `.docx`

- Use tracked changes where practical. Preserve formatting, styles, and equation objects.
- Keep equation and figure numbering and cross-references consistent.

Students get PDFs alongside the `.pptx`/`.docx` where practical.

## Git

- Never commit files from `../astro331-instructor-only`, or anything with `solution`, `key`, `rubric`, `quiz`, or `exam` in its name.
- `.gitignore` should exclude Office lock files (`~$*.docx`, `~$*.xlsx`, `~$*.pptx`).
