# Change Log
- Added support for summary_level variable: "short" and "detailed"
- Updated loop instructions to conditionally generate compact or detailed summaries

# Module 2 — Section Loop

Description:  
This module iterates through each section of the paper to generate summaries (~100 words). It applies expert and lay conversion, enforces word limits (<150 words), and maintains consistent terminology
New Variable:
- `summary_level`:
  - `"short"` → generate a 1–2 sentence summary per section
  - `"detailed"` → generate a short paragraph (around 100 words) plus 3 bullet points with key information.

Loop Instructions:
- For each section in the paper:
  1. Check the `summary_level` variable.
     - If `summary_level = "short"`: generate only a compact summary (1–2 sentences).
     - If `summary_level = "detailed"`: generate a paragraph summary (around 100 words) and add 3 bullet points with important information.
  2. Apply expert conversion or lay conversion based on audience type.
  3. Enforce word limits (<150 words per section summary).
  4. Maintain consistent terminology across all sections.
  5. Flag any missing or very short sections (<50 words) for warning output.

