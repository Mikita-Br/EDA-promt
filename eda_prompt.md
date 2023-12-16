1. Identify and understand your target variable.
   1. Understand the type of the target variable: binary, categorical, or numeric.
   2. Examine the distribution of the target variable.
      1. For a binary variable (which needs to be converted into 0s and 1s if it is in string format), the mean (a proportion of 1s) is simply used.
      2. For a categorical variable, value counts are used.
      3. For a numeric variable, a histogram or a pandas' describe table is used.
   3. After examining and understanding the target variable, add a markdown cell with your conclusions.
2. Choose the metric(s) for the target variable you will use in pivot tables.
   1. For a binary variable, this metric is the mean.
   2. For a categorical variable, it could be the share between categories (and you will have a column for each category with the corresponding percentage).
   3. For a numeric variable, it could be the mean and/or median and other quantiles, along with some spread metric like standard deviation or mean average deviation.
3. Calculate the percentage of missing values in each column and sort them in descending order.
   1. Missing values and outliers are not problems to be fixed! They are facts.
   2. During EDA you must not “fix” them because you have to deal with your data and problem as it is.
   3. If you see missing values, just report them.
   4. Don’t do outlier analysis as a stand-alone step–deal with them along the way. If you see outliers, report them and come up with appropriate analysis and metrics that can capture the complexity of the situation.
4. Create a pivot table for each variable, examining the breakdown of your metric(s) by different categories and deriving insights.
   1. Start with the most important variables or variables that draw your attention. If you have too many variables (e.g., 100) and have no idea what’s going on, you can calculate the phik coefficient between the target and all other variables. The phik coefficient highlights the strongest relationship automatically and you can start from examining them first.
   2. If you wish to use a numeric variable for making a split, first convert it into a categorical variable (create bins) using the 'cut' or 'qcut' function with bins=5 (use 'qcut' if the sizes of groups resulting from 'cut' are very uneven).
   3. Each pivot table should include the size of the groups (count) along with the metric for the target variable.
   4. The count should be the first column in each pivot table.
   5. Use the groupby function (with dropna=False to have the metrics for all missing values in the variable) to create pivot tables.
   6. Each pivot table should be created in a separate cell.
5. If a pivot table has 5 or more rows, use a bar chart to visualize it.
   1. Do not visualize small tables!
   2. If you're making a split by a categorical variable and it has too many distinct values, display the top 10 values by count.
   3. Alternatively, try to reduce the number of groups through some transformation.
6. Add a markdown cell in the notebook with the insights you've found after each cell that has an output, table, or graph.
   1. Insights should draw attention to evident differences in the metric(s) for the target variable between groups, and also provide a possible common-sense (general experience) explanation grounded in reality and the nature of the problem you are investigating. Provide a "why" along with reporting your findings.
   2. Also, add some ideas for further analysis as a short TODO list with 2-3 items (e.g., add another specific variable in groupby to see if it is the real cause). Do not do these TODOs until you finish the first iteration of your EDA and get the big picture of the whole situation.
   3. All comments you make should be added as markdown cells within the notebook.
   4. The notebook should be a well-written and structured document, like an interesting blog post or essay, ready to be shared with readers.
7. You should also use markdown cells to structure your notebook.
   1. Use level one headings for major sections like 'Data Upload', 'Understanding Target Variable', 'EDA'.
   2. Use level two headings for sub-items, for example, for each variable in the EDA section.
   3. This structure will help to create a table of contents automatically.
8. Do not display the results of your analysis here in the chatGPT interface.
   1. Save your results only in the notebook.
   2. Here, at the chatGPT interface, only report what step you are working on now and also report when this step is finished.