# Color-Vision-Deficiency-friendly-visualisations-in-R
Building and analyzing CVD (Color Vision Deficiency) friendly visualizations in R


Color Palettes for Data visualizations

![Screenshot 2021-10-01 at 2 32 32 PM](https://user-images.githubusercontent.com/60548801/135628541-52a78455-2b39-4d3c-a8fa-70ca4c73c56a.png)

Qualitative Data can be represented effectively using the Qualitative Palette shown in figure 4, however the Tints, Shades and Tones palettes (figure 1, figure2, figure3) won’t be appropriate since they won’t be able to effectively discern the different values. Tints, Shades and Tones can be used where we want to suggest or show a grouping of data or related data. In Tints, Shades and Tones one of the color values could be seen as having more significance over the other this may cause data of a specific type to overshadow the data of other type.

**Building and analyzing CVD (Color Vision Deficiency) friendly visualizations in R:
**

Below report analyses plots generated by default color values from ggplot and visualizes it from the perspective of a person with CVD. We will also see the R implementation of one of the CVD friendly color palettes introduced by Okabe and Ito. Further, we see the use of viridis library to create CVD friendly visualizations.

![Screenshot 2021-10-01 at 2 33 43 PM](https://user-images.githubusercontent.com/60548801/135628729-33b910fe-b1ef-4485-984b-c2e659b446f5.png)

On the left plot we can see the visualization generated by ggplot using the default color values. Since we have green and red together in the same plot, it might not be CVD friendly as both the colors may be seen as similar if we view it from the lens of CVD.
On the left the plot uses colorblindr library in R to show us how the same plot looks from a CVD perspective. As we can see in the plot, a person with Deutanomaly would see green as a darker shade of brown, and red as a lighter shade of brown. Similarly, for Pertanomaly green appears to be a lighter shade of brown and red appears as a darker shade of brown. This might give out an incorrect indication as if the two datapoints are related to each other, or the blue datapoints are more significant. In Tritanomaly the blue and green datapoints look very similar and may cause a confusion as to whether they are related or are the same. Hence, we can say that the first plot is not CVD friendly.

![Screenshot 2021-10-01 at 2 34 42 PM](https://user-images.githubusercontent.com/60548801/135628993-dcfbe3af-17d8-4f6e-9df7-7f5227209bcf.png)

On the left scatterplot we have used the colors from a CVD friendly color palette by Okabe and Ito. The plot shows how it looks to a person without CVD. The colors here are differentiable and distinct.
The scatterplot on the right, visualizes the left plot from the perspective of a person with CVD. As we can see there has been a significant improvement in distinguishing the datapoints from each other as each color looks distinct. Conclusively we can say that plot 2.1 is CVD friendly.

![Screenshot 2021-10-01 at 2 35 00 PM](https://user-images.githubusercontent.com/60548801/135629077-9f62f7e9-ec75-4f43-8b2f-410560d8d807.png)

Another way to make a visualization CVD friendly is to scale the colors of datapoints manually by using the viridis library. On the left we see the implementation of the same.
The scatterplots on the right help us to view the visualization generated by viridis library, from the lens of CVD. As we can see the colors are distinct and datapoints are distinguishable. Thus, the scatterplot in figure 3.1 is also CVD friendly

**
Conclusion:**

Conclusively we can say that plots in figure 2.1 and 3.1 are CVD friendly as the colors look distinct from the lens of CVD. Scatterplot in figure 1.1 is CVD friendly to a very less extent as the person with CVD will have to view the plot very carefully to understand the color difference and hence the plot doesn’t give a clear visualization of data at a glance. I found that the graph created by the color palette of Okabe and Ito in figure 2.1 shows the colors most distinctively from a CVD perspective and hence is the most CVD friendly graph. The second-best graph to consider after that would be the created using viridis library in figure 3.1. From a standard perspective all of these plots are good as in each we can see the colors distinctively.
