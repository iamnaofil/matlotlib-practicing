

Matplotlib
=======================================
Welcome to the Matplotlib README! This guide aims to provide an overview of essential Matplotlib topics, functions, and their use cases for data visualization in Python.
```
Matplotlib is like a magical toolbox for creating awesome pictures with numbers.
📊 It's used by smart people to show data in cool ways.

Here are some cool things about it:

Control Freak: You can change everything about your picture –
colors, shapes, and even how things are drawn. It's like drawing your own masterpiece!

Make It Yours: You can make your picture look exactly how you want it.
Imagine dressing up your favorite toy in different outfits!

Friends with Everyone: It's best friends with other Python tools like NumPy and Pandas.
They work together like superheroes in a team!

Lots of Help: Loads of people use it, so if you get stuck, you can find help and examples everywhere.

So, Matplotlib is your artsy friend who helps you show your data in a way that everyone understands. 🎨📈
Remember, you're the artist, and Matplotlib is your colorful palette! 🖌️
```

**Table of Contents**

Introduction

Installation

Basics of Matplotlib

Line Plots

Scatter Plots

Bar Charts

Histograms

Pie Charts

Customization and Styling

Saving Figures

Conclusion

**1. Introduction**

Matplotlib is a powerful Python library for creating static, animated, and interactive visualizations. 

It's widely used in data analysis, scientific research, and data presentation.

The choice of the right plot depends on the specific data and the story you want to convey.

Always consider the data type, distribution, 
and the message you want to communicate when selecting a plot for your analysis or presentation.


**2. Installation**
To get started with Matplotlib, you can install it using pip:
```
pip install matplotlib
```

**3. Basics of Matplotlib**
Importing Matplotlib: Import the library and its submodules.

```
import matplotlib.pyplot as plt
```

We have also give this line to show the graphs, ---

```%matplotlib inline```
Creating Figures and Axes: Understand the concept of figures and axes to create plots.
plt.plot('any sequence or array for X axis','any sequence or array for Y axis')

fig, ax = plt.subplots()

**4. Line Plots**
Usage: Line plots are ideal for showing trends and relationships in data over a continuous range.

Scenarios: Use line plots for time series data, stock market trends, or any data with a continuous x-axis.
```
import matplotlib.pyplot as plt #Use these two line in every code I am skiping here
%matplotlib inline
# Sample data :this can be any type of sequence mutable (list,) or Tuple or Numpy Array
x = [1, 2, 3, 4, 5]
y = [10, 15, 13, 18, 22]

# Creating a line plot with just two data 
plt.plot(x, y)

# Customizing the plot
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Line Plot Example')
plt.grid(True)

# Displaying the plot
plt.show()
```
plt.plot(x, y): Creates a line plot with x and y data.

plt.xlabel, plt.ylabel: Sets labels for the x and y axes.

plt.title: Sets the plot title.

plt.grid(True): Adds a grid to the plot.

**5. Scatter Plots**
Usage: Scatter plots are useful for visualizing individual data points.

Scenarios: Employ scatter plots to explore relationships between two variables, identify outliers, or show clusters in data.

```
# Sample data
x = [1, 2, 3, 4, 5]
y = [10, 15, 13, 18, 22]

# Creating a scatter plot
plt.scatter(x, y, label='Data Points', color='blue', marker='o', s=100)

# Customizing the plot
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Scatter Plot Example')
plt.legend()

# Displaying the plot
plt.show()
```

plt.scatter(x, y): Creates a scatter plot with x and y data.

label: Adds a label to the data points.

color: Sets the color of data points.

marker: Specifies the marker style (e.g., 'o' for circles).

s: Controls the marker size.

Use Case:
Scatter plots are useful for visualizing relationships between two numerical variables, identifying outliers, or showing clusters in data.


**6. Bar Charts**
Usage: Bar charts represent data with rectangular bars.

Scenarios: Use bar charts for comparing discrete categories, displaying survey results, or visualizing categorical data.
```categories = ['A', 'B', 'C', 'D', 'E']
values = [20, 35, 25, 30, 15]

# Creating a bar chart
plt.bar(categories, values, color='green')

# Customizing the plot
plt.xlabel('Categories')
plt.ylabel('Values')
plt.title('Bar Chart Example')
# Displaying the plot
plt.show()
```
plt.bar(categories, values): Creates a vertical bar chart.
color: Sets the color of the bars.
Use Case:

Bar charts are used to compare numerical values across different categories or to visualize categorical data.


**7. Histograms**
Usage: Histograms display the distribution of data in bins or intervals.

Scenarios: Employ histograms to understand data distribution, identify data skewness, or analyze frequency distributions.
```data = np.random.randn(1000)

# Creating a histogram
plt.hist(data, bins=30, color='purple', alpha=0.5)

# Customizing the plot
plt.xlabel('Values')
plt.ylabel('Frequency')
plt.title('Histogram Example')

# Displaying the plot
plt.show()
```
plt.hist(data, bins=30): Creates a histogram with data.
bins: Specifies the number of bins or intervals.
alpha: Controls the transparency of bars.
Use Case:

Histograms are used to visualize the distribution of numerical data, especially for univariate analysis.


**8. Pie Charts**
Usage: Pie charts show data composition as slices of a circle.

Scenarios: Use pie charts for displaying parts-of-a-whole relationships or visualizing categorical data percentages.

```categories = ['A', 'B', 'C', 'D']
sizes = [15, 30, 45, 10]

# Creating a pie chart
plt.pie(sizes, labels=categories, autopct='%1.1f%%', startangle=90, colors=['red', 'green', 'blue', 'yellow'])

# Customizing the plot
plt.title('Pie Chart Example')

# Displaying the plot
plt.show()
```
plt.pie(sizes, labels=categories): Creates a pie chart with sizes and labels.

autopct: Displays percentage values on the chart.

startangle: Specifies the starting angle for the first slice.

colors: Sets colors for the pie chart slices.

Use Case:

Pie charts are used to represent parts-of-a-whole relationships or the distribution of categorical data.


**9. Customization and Styling**
Usage: Customize plots with various attributes like colors, line styles, markers, and labels.

Scenarios: Tailor visualizations to your preferences and make them more informative and aesthetically pleasing.

Adding Labels and Title

```plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Title of the Plot')
```
Adding Legends
```
plt.plot(x1, y1, label='Data Series 1')
plt.plot(x2, y2, label='Data Series 2')
plt.legend()
```

Changing color and Style
```
plt.plot(x, y, color='red', linestyle='--', marker='o')


```


linestyle Values:
'-' (or 'solid'): This is the default value and creates a solid line.

'--' (or 'dashed'): This creates a dashed line.

':' (or 'dotted'): This creates a dotted line.

'-.' (or 'dashdot'): This creates a dash-dot line.

'None' (or ' ', ''): This creates no line, which is often used when you want to plot markers only.

marker Values:
Markers are used to indicate data points on the line plot.

'o': Circular markers.

's': Square markers.

'D': Diamond markers.

'+': Plus markers.

'*': Star markers.

'x': X markers.

'.': Point markers.

',': Pixel markers.

'1', '2', '3', '4': Triangular markers pointing in different directions.

'|', '_': Vertical and horizontal line markers, respectively.

None (or ' ' or ''): No markers.




```
# List available styles
print(plt.style.available)
```

```plt.style.use('ggplot')

# Your plot code here
plt.plot([1, 2, 3, 4, 5], [10, 15, 13, 18, 22])

# Display the plot
plt.show()
```

**10. Saving Figures**
Usage: Save your Matplotlib figures as image files.

Scenarios: Save visualizations as PNG, JPEG, or other formats for use in reports, presentations, or publications.

```
#You can just simply write this to save a chart / graph
plt.savefig('sample.png')

#More parameter
plt.savefig(
    'sample_plot.png',                 # File name and format (e.g., .png, .jpg, .pdf)
    dpi=300,                           # Resolution (dots per inch)
    bbox_inches='tight',               # Trim the white space around the plot
    transparent=True,                  # Make the background transparent
    format='png',                      # Specify the format explicitly (optional)
    quality=95                         # JPEG compression quality (for JPEG format)
)

```

'sample_plot.png': Specifies the file name and format for saving the figure.

dpi=300: Sets the resolution to 300 dots per inch.

bbox_inches='tight': Trims the white space around the plot to make it more compact.

transparent=True: Makes the background of the saved image transparent (useful for certain use cases like overlaying the plot on other images).

format='png' (optional): Specifies the format explicitly; in this case, it's a PNG image.

quality=95 (optional): Applies JPEG compression with a quality level of 95 (only applicable if you're saving in JPEG format).

**11. Conclusion**
Matplotlib is a versatile library that allows you to create a wide range of visualizations for diverse data analysis tasks. 
This README provides a starting point for understanding its key functions and their applications.
