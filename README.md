# Python Notebook Pills (Bootstrap-Inspired)

This project explores using **Python inside Jupyter notebooks** together
with **selectively extracted Bootstrap 5.3 CSS** to render clean,
semantic **status pills** (for example: *Success*, *Danger*, *Warning*)
directly in notebook outputs.

Rather than importing the full Bootstrap framework, this approach embeds
only the **minimal CSS required for pills**, keeping notebooks
lightweight, portable, and easy to share.

------------------------------------------------------------------------

## What this project does

-   Uses Python logic to evaluate conditions (`True / False`,
    thresholds, validations).
-   Dynamically generates HTML from Python.
-   Styles that HTML using a **small subset of Bootstrap CSS** (badges,
    subtle backgrounds, emphasis text).
-   Renders results inline using `IPython.display.HTML`.

The outcome is a notebook that reads more like a **report or dashboard**
than a script.

------------------------------------------------------------------------

## Why partial Bootstrap

Bootstrap 5.3 relies heavily on **CSS variables**, which makes it
possible to extract only the pieces needed for:

-   Subtle background colors (`bg-*-subtle`)
-   Emphasis text (`text-*-emphasis`)
-   Rounded pill shapes (`rounded-pill`)

This preserves visual consistency and readability without pulling in
JavaScript or unrelated layout styles.

------------------------------------------------------------------------

## Example usage

``` python
display(HTML(status_badge(validation_passed, "Validation 1:")))
```

Which renders as:

**Validation 1:** Success\
or\
**Validation 1:** Fail

All logic lives in Python.\
All presentation lives in HTML + CSS.

------------------------------------------------------------------------

## First experiment

The first experiment was building a **mini dashboard** that:

-   Reads the contents of a table (e.g., a Pandas DataFrame)
-   Applies validation rules to each row or metric
-   Generates labeled status pills dynamically
-   Displays the results as a compact, human-readable summary

This provides a lightweight alternative to heavier dashboard frameworks
for exploratory analysis and validation workflows.

------------------------------------------------------------------------

## Future ideas

-   **Table-driven dashboards**\
    Automatically generate pills for rows or metrics based on
    thresholds for KPIs.

-   **Multi-state pills**\
    Extend beyond Success / Danger to include Warning, Info, or custom
    states.

-   **Experiment summaries**\
    Summarize A/B tests, data quality checks, or pipeline health at a
    glance.

-   **Reusable notebook components**\
    Centralize CSS and helper functions for consistent visuals across
    notebooks.

-   **Export-friendly reports**\
    Ensure pills render correctly in exported HTML or PDF reports.

------------------------------------------------------------------------

## Disclaimer
This README file was created with the assistance of **ChatGPT**.
