---
# Do not edit the text between these lines!
layout: default
---

# COMP110 Data Analysis: Does Prior Experience Affect Perceived Pace and Difficulty?

<!-- This is a comment. Below, you'll see code for inserting an image. To make this image appear, update <custom-path>. To add an image, save it inside the imgs folder of this repository. -->
<img src="<custom-path>/static/imgs/logo.png" alt="Image of Comp110 rainbow logo. "  width="500"/>

## Summary

For this project, I analyzed survey data collected from COMP110 students across two sections to explore whether students with less prior programming experience perceive the course pace and difficulty as higher than students with more experience. My hypothesis was that if this pattern exists in the data, it would support the idea that adjusting early-semester pacing could create value for the majority of students in the course.

I loaded and combined two CSV survey files using `read_csv_rows` and `columnar`, then narrowed the data down to three relevant columns, `prior_exp`, `pace`, and `difficulty`, using `select`. After filtering out incomplete responses with a custom `filter_valid_rows` helper function, I was left with 764 valid responses to analyze.

## Visualizations
#### Distribution of Prior Programming Experience 
<img src="/classpace/static/imgs/bar_chart.png" alt="Bar chart showing distribution of prior programming experience" width="700"/>

The bar chart shows that the vast majority of COMP110 students (roughly 475 out of 764) have little to no prior programming experience. This means any pacing issue in the early weeks would affect the largest group in the class.

#### Perceived Pace by Prior Experience
<img src="/classpace/static/imgs/pace_box.png" alt="Box plot of pace ratings grouped by prior experience" width="700"/>

The box plot shows that students with less experience tended to rate the course pace as higher compared to students with more prior experience. The median for the "None to less than one month!" group leaned toward the higher end of the scale relative to the "1-2 years" and "Over 2 years" groups.

#### Perceived Difficulty by Prior Experience
<img src="/classpace/static/imgs/difficulty_box.png" alt="Box plot of difficulty ratings grouped by prior experience" width="700"/>

Similarly, students with less experience rated the course as more difficult. This pattern alongside the pace findings supports the hypothesis that early pacing disproportionately burdens beginners.

#### Pace vs. Difficulty by Prior Experience
<img src="/classpace/static/imgs/scatter.png" alt="Scatter plot of pace vs difficulty colored by prior experience" width="700"/>

The scatter plot reinforces the box plot findings. High pace and high difficulty ratings were more concentrated among inexperienced students, while experienced students were more spread toward the lower end of both axes.

## Conclusion

The bar chart made it immediately clear that the overwhelming majority of COMP110 students (roughly 475 out of 764 valid responses) have little to no prior programming experience. This means any pacing issue in the early weeks would affect the largest group in the class, making it an important problem to address.

The box plots for pace and difficulty showed that students with less experience tended to rate both the pace and difficulty of the course as higher compared to students with more prior experience. The medians of difficulty scale and the range of our pace scale for the "None to less than one month!" group leaned toward the higher end of the scale relative to the "1-2 years" and "Over 2 years" groups, which supports our hypothesis that early pacing disproportionately burdens beginners. The scatter plot reinforced this. It shows that high pace and high difficulty ratings were more concentrated among inexperienced students, while experienced students were more spread toward the lower end of both axes.

Overall, the data supports the idea that adjusting early semester pacing would create value for the largest portion of the student population. A reasonable recommendation would be to add optional scaffolding resources in the first few weeks, such as gentler warm-up exercises or review sessions targeted at students with no prior programming background.

A potential extension of this idea would be to cross this analysis with the understanding column. A student might feel the pace is fast but still report understanding the material, which would weaken the urgency of restructuring. Tracking these ratings across multiple survey checkpoints throughout a semester would also reveal whether the gap between experience groups narrows over time or persists.

The main trade-off to consider is that slowing early pacing could under-challenge students who already have experience, potentially causing them to disengage. Instructors and course designers would need to balance both groups, perhaps through tiered optional content, which adds design and grading complexity for TAs and course staff.