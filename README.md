# Visualizing Gap in College Degrees between Men and Women

[View here!](https://nbviewer.jupyter.org/github/epatter1/visualizing_college_earnings/blob/master/Visualizing%20Gap%20in%20College%20Degrees%20between%20Men%20and%20Women.ipynb
) :eyes:
> ### Goal: Utilize Matplotlib and Seaborn to visualize the gender gap across college degrees. Generate line charts to compare across various STEM degree categories.

On the outset, the immediate issue that stuck out is the titles of some line charts overlapping with the x-axis labels for the line chart above it. In removing the titles for each line chart, the viewer won't know what degree each line chart refers to. Instead, I removed the x-axis labels for every line chart in a column except for the bottom-most one using ***Axes.tick_params()*** and setting the ***labelbottom*** parameter to off.
 
Removing the x-axis labels for all but the bottommost plots solved the issue I noticed with the overlapping text with an added plus of making the plots cleaner and more readable. The trade-off I made is that it's now more difficult for the viewer to discern approximately which years some interesting changes in trends may have happened. This is fine because I'm primarily interested in enabling the viewer to quickly get a high level understanding of which degrees are prone to gender imbalance and how that has changed over time.

In the vein of reducing clutter, I simplifyied the y-axis labels as well. Originally, all seventeen plots had six y-axis labels and even though they are consistent across the plots, they still added to the visual clutter. By keeping just the starting and ending labels (0 and 100), I kept some of the benefits of having the y-axis labels to begin with. I used the ***Axes.set_yticks()*** method to specify which labels I wanted displayed.

While removing most of the y-axis labels definitely reduced clutter, it also made it hard to understand which degrees have close to **50-50** gender breakdown. While keeping all of the y-axis labels would have made it easier, I can actually do one better and use a horizontal line across all of the line charts where the y-axis label 50 would have been. So I generated a horizontal line across an entire subplot using the ***Axes.axhline()*** method.


