## EECS 731 Project 7: Visualization by Matthew Taylor

### Overview

This project is meant to serve as an introduction to various visualization techniques. Information will be extracted from a single dataset in various ways to tell a number of stories visually. A main takeaway from this project is that conveying information visually is sometimes more effective than conveying it strictly numerically.

### Approach

I began by downloading [this dataset](https://www.kaggle.com/felixzhao/productdemandforecasting), which was used in the time series forecasting project. This dataset contains information about product demands over many years. With five features and over one million observations of highly numerical data (including timestamps), I believed this dataset to be the best for creating visualizations. For my three visualizations, I decided to include a line graph showing the overall demand of all products from each of the warehouses over five years, a pie chart showing the percentage of overall demand for a given product by warehouse, and a line graph showing seasonal trends of a few products.

### How to Run

This project was written in a Jupyter Notebook running Python 3.7.2. This project relies on a small number of modules, which can be installed by running this command:
```
pip3 install -r requirements.txt
```

Once the requirements are installed, each of the cells in the Jupyter Notebook can be executed. However, this is not required as each cell has already been executed and the results are shown.

### Results

This first plot shows the overall demand of all products from each warehouse over five years.
![](https://i.imgur.com/4gLczvd.png)

We can quickly and clearly see that Warehouse J has a much higher demand than every other warehouse, while Warehouse A has a relatively low demand comparatively. Furthermore, one may notice that the overall demand of products from Warehouse C has historically been lower than the overall demand of products from Warehouse S. However, beginning in early 2016, this trend has been broken.

This next visualization shows a breakdown of the total demand for a single product by warehouse.
![](https://i.imgur.com/8DSGk73.png)

This simple visualization may tell the seller various things about their product. A chart like this, in conjunction with the locations of the warehouses may help identify geographic demand trends that can be used to allocate advertising funds more appropriately or help schedule deliveries.

Finally, this last graph shows seasonal trends of a few products.
![](https://i.imgur.com/qhWHV8l.png)

These products illustrate seasonal trends quite well. The products represented by the red and green lines have drastic spikes in demand in April compared to the rest of the year. Meanwhile, the product represented by the yellow line is in much higher demand during the summer than any other time. The demand of the product represented by the blue line is relatively high specifically in November. This information can be used to increase production and promote products whose demands are reaching their seasonal peaks.

### Future Work and Optimizations

Given more time to work on this project, I would have utilized tools other than matplotlib. Services like Tableau have interactive visualizations that can illustrate a point much more effectively. Next, I would have found a more interesting dataset. While this dataset did have a large number of possible illustration ideas, each of the illustrations was rather lackluster. When compared to some [rather simple but incredibly powerful visualizations](https://apps.washingtonpost.com/g/page/world/the-depth-of-the-problem/931/), the ones shown here can't help but fall a little flat. Finally, the last idea I would implement would be to rework the data behind the third visualization. I believe the way I current have it implemented, it is vulnerable to skewing by a single anomaly. In other words, one month of unusually high sales for a product may cause a spike during that month. Even though this spike may not be consistently seen in that month during other years, a spike is shown in the visualization during that month.
