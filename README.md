# What Happens After You Choose a Program?

## An analysis of earnings, AI exposure, and employment outcomes across U.S. college programs

This is my **first data science project**, and I'm excited to share it! I wanted to dig into a question a lot of prospective (and current) college students ask themselves: does the program you study matter more than the school you attend? I used a public dataset covering earnings, debt, jobs, and AI exposure across college majors to try to find out.

## The Questions I Set Out to Answer

**Earnings**
- Does going to a more selective school lead to higher post-graduate earnings — both overall and within specific programs?
- What is the tuition-to-earnings ratio for each program, and which programs give the most "bang for your buck"?
- How does each program's 4-year earnings compare to the median 4-year earnings of a typical bachelor's degree holder?
- What does a graduate's earnings trajectory look like over the course of a career, by program?

**Artificial Intelligence**
- What share of a program's linked occupations already involve working alongside AI tools?
- What share of a program's linked occupations are exposed to "expert-system" technology (AI that's replacing/automating tasks)?

**Employment**
- Which programs have the highest share of graduates who are not working?
- What is the most common job graduates of each program actually end up in?

## Data Source

This project uses the **"College Majors 2026: Earnings, Debt, Jobs, AI"** dataset from Kaggle, created by M. Lab.
Source: https://www.kaggle.com/datasets/kylefengkfeng209/college-majors-2026-earnings-debt-jobs-ai

## What's in This Repo

- `college_outcomes_analytics.ipynb` — the Jupyter Notebook where I cleaned and prepared the raw dataset with Python and pandas.
- `program_outcomes_statistics_deck.pptx` — a PowerPoint deck that presents the findings visually, with a chart and takeaway for each question above.

## Methodology

1. **Data cleaning (in the notebook):** I loaded the raw CSV with pandas, trimmed it down to only the columns relevant to my questions, filtered the data to Bachelor's degree records only, fixed data types (e.g., tuition values that needed to be converted to floats), investigated and removed bad/impossible records (like a school with a 0% admission rate), and handled missing data — either by dropping rows or filling in gaps with the median value for that region.
2. **Analysis and visualization:** Using the cleaned data, I built out charts and visuals answering each of the questions above. To be transparent: **I did not personally write the code that generated the graphs.** I used Claude and ChatGPT to help build the visualizations (ChatGPT specifically for the final chart), since my focus for this first project was on the data cleaning, framing the right questions, and presenting the results clearly.
3. **Presentation:** All final visuals and takeaways are compiled in the PowerPoint deck, organized by theme (Earnings, AI, Employment) with an appendix covering definitions, methodology, and limitations.

## Key Takeaways

- School selectivity has only a weak overall relationship with earnings, but it matters a lot more in some programs (like Math & Statistics, History, and Computer/Information Sciences) than others
- Technical and applied programs (Engineering, Computer Science, skilled trades) tend to offer the strongest tuition-to-earnings return.
- AI and expert-system exposure is heavily concentrated in Computer Science and a handful of STEM-adjacent fields. Most other programs see minimal AI exposure in their linked occupations
- People-facing and service-oriented programs show more "not working" activity after graduation, while technical and hard-science programs show less.
- **Bottom line:** program choice seems to matter more than institution selectivity alone. Earnings, AI exposure, and employment stability vary more by field of study than by how selective the school is

## Limitations

- Correlation does not imply causation. Selectivity and earnings may both be driven by other underlying factors.
- Occupation linkage reflects common national outcomes for a program, not any individual graduate's actual job.
- Earnings vary by geography, experience, industry, and the broader economy. These findings are just a snapshot, not a guarantee.

## What I Learned

This was my first real data science project, and I learned a lot along the way, including:
- Basic data cleaning: filtering irrelevant columns, fixing data types, identifying and removing invalid records, and handling missing values (both by dropping and by imputing medians)
- How to work with a real-world, messy dataset instead of a "clean" tutorial dataset
- How to use AI tools (Claude and ChatGPT) as collaborators to help build visualizations, while still owning the data prep, question design, and interpretation myself
- How to communicate data findings clearly to a non-technical audience through a presentation deck

## Tools Used

- Python (pandas) for data cleaning, in a Jupyter Notebook
- PowerPoint for the final presentation of findings
- Claude and ChatGPT to help generate the data visualizations