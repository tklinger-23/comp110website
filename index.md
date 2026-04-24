---
# Do not edit the text between these lines!
layout: default
---

# EX09 Website
<img src="static/imgs/logo.png" alt="comp110logo. " width="500"/>
<!-- This is a comment. Below, you'll see code for inserting an image. To make this image appear, update <custom-path>. To add an image, save it inside the imgs folder of this repository. -->
<!-- EXAMPLE -->

## Difficulty and Livestream Preference Relationship
<br>
<img src="static/imgs/difficulty.png" alt="difficulty. " width="500"/>
<br>
The histogram highlights the number of respondents who either agreed or disagreed with the prospect of having a livestream on a scale of 1 to 7.
<br>

## Livestream Count
<img src="static/imgs/livestream_preference.png" alt="livestreamcount. " width="500"/>
<br>
This graph shows the correlation between the class difficulty and the preference of having a livestream
<br>

## Class Pace and Livestream Preference Relationship
<img src="static/imgs/pace.png" alt="pace. " width="500"/>
<br>
This graph shows the correlation between class pace and the preference of having a livestream.
<br>


## Summary of Analysis and Conclusion

Summary of the Analysis
<br>
The analysis reads survey data and focuses on three key variables: add_livestream (preference for adding a livestream option), difficulty (perceived class difficulty), and pace (perceived class pace).
Data was loaded using a custom read_csv_rows() function, which reads the CSV into a list of row dictionaries. It was then transformed into columns using columnar(), making it easier to select on individual variables. Relevant columns were extracted using the select() function. The convert_columns_to_int() helper function was used to convert the columns from strings to integers for numerical analysis, and a custom filter() function was applied to remove responses above the valid difficulty threshold.The count() function tallied the frequency of each add_livestream response value, and get_keys() was used alongside head() to preview the structure of the dataset before analysis. Three charts were generated using Python's built-in plotting capabilities through seaborn. The first uses displot to create a histogram of the add_livestream column, binned into 7 bars to match the 1–7 scale. This shows how many respondents selected each rating and collates them into the bars of a histogram. The second and third use relplot with kind="line" to plot livestream preference against difficulty and pace in each of their cases respectively. The axis are created with “x=” and “y=” for organizational work. It appears that the mean and confidence interval at each x-value are built into the programming, producing the shaded line plots shown. All three charts draw from the same analysis_int dataframe, which stores survey responses as integers. As integers, they are easier to place. Responses are stored in dictionaries as keys to then pull from the values as keys.

<br>
Conclusion:
<br>
The data presents a compelling case for implementing a livestreaming option in COMP110. With 73% of respondents rating their support between 5 and 7 on the agreement scale, the demand for this feature reflects a clear and decisive majority. It must not go unnoticed.

It is recommended that the livestream start next semester, as a vast number of respondents who favored the livestream felt that the class had a fast pace with measurable difficulty. This confounding variable likely means that the students who find the class most unmanageable want the ability to slow the pace of lectures, rewind, or watch them back.

The class can implement a livestream for students who feel overwhelmed, are ill, or have emergencies arise. Flexibility is important, and with hard classes like COMP110, the overwhelming demand is to have a livestream for support.

An extension of this study could evaluate the grades of the students in total. It would be interesting to see a correlation between grade averages and the opinion of the livestream. The opinion is likely not grade correlated since 73% of respondents supported the action, but it may be worth evaluating if there is a confounding factor at play. A grade-correlated analysis could help identify whether struggling students are disproportionately driving demand or whether the appeal is broad.