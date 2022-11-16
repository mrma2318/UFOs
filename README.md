# UFOs

## Overview of Project: Use HTML to create a webpage for UFO signtings, and utilize Javascript to create a table to organize UFO data into a list. Then by using Bootstrap, within my table, I will create several functioning filters to allow users to interact with the table on the webpage.

### The purpose of this analysis is to provide an in-depth analysis of UFO sightings and allow users to filter for certain criteria at the same time.

## Analysis
- For this analysis, I created a folder to hold my CSS file, a folder to store images, and a folder to hold my Javascripts. In addition, I created an [index.html](https://github.com/mrma2318/UFOs/blob/5e153bee2cc9b62a4b66caac32db6d104b6d656b/index.html) file for the final HTML page for the project. 

- Before I started coding to generate the webpage to store the UFO sighting list into a table, I needed to create a storyboard to provide the layout of the webpage. By creating a storyboard for the webpage, it provides a visual reference to outline all the elements including the article title, summary, and the table. This way when I start writing the Javascript code for the table, I'll know which HTML components I'm connecting the table to. 

- Since I created my storyboard, I can start creating my webpage. First, I need to import the data and point the data to the HTML table using d3 by referencing the tbody. Now I can build the table to sort and store the data. To do so, I need to create a new function, which I named buildTable, and pass in the data. To make sure I am creating a fresh table, I also used a code to clear any existing data. This way, I am not reinserting data that already exists, creating duplicates.

- Now I can start adding rows of data to the table by using a forEach function that loops through our data array. Then I created a variable that will append a row to the table body. Then I wanted to make sure that I specified that each sighting goes onto its own row of data. Next, I appended each value of the object to a cell in the table.

- Since there are hundreds of rows of sighting in the table, the next item to add filters to more effectively review and study the data by using the d3 function to help accomplish this task. First, I created a variable to keep track of all the filters. Then, I created a function to update the filters, called updateFilters.

- Within the updateFilters function that I created, I needed created additional variables that would save the element's that were changed, saves the value of the changed element's property, and create a variable that saves the attribute of the changed element's id. Then I also needed to create an if else statement that checked if a value was changed. If a value was changed then the element's id would be added as the property and the value that was changed was added to the filters. Next, I wanted to call the function to apply all filters and rebuild the table. 

- Then I needed to write a another function, called filterTable, to filter the table based on the user input that is stored in the filters variable. Now I can create a variable for the filtered data that is equal to the data that builds the table. Within the filterTable function, I created a loop through the filters object and stored the data that matches the filter values in the variable created. Now I can rebuild the table with the filtered data by passing the variable created. 

## Results
- The UFO webpage can be found by clicking on [UFO Finder](https://mrma2318.github.io/UFOs/). When you go to the webpage, you can see the article title, summary, the UFO data underneith the summary, and the filter categories on the left hand side of the page. With the filter categories you can filter through the data by date, city, state, country, and shape (Image 1). 

### Image 1: Filter Search Menu

![Filter Search](https://github.com/mrma2318/UFOs/blob/442d7d115b8b358b638444af80ab5fa42f255f8f/Resources/Screen%20Shot%202022-11-15%20at%206.45.56%20PM.png)

- For example, if you wanted to see all the UFO sightings that happened on 1/13/2010, you can put that date in the "Date" filter and press enter on your keyboard. The table will then show you all the UFO sightings that happened on 1/13/2010, Image 2. 

### Image 2: UFO Sightings on 1/13/2010

![UFO Sightings on 1/13/2010](https://github.com/mrma2318/UFOs/blob/442d7d115b8b358b638444af80ab5fa42f255f8f/Resources/Screen%20Shot%202022-11-15%20at%206.46.29%20PM.png)

- You can also filter using more than one of the categories. For example, if you wanted to see all the UFO sightings that happened in Flordia on January 11, 2010, you can filter by "Date" 1/11/2010, and "State", fl. The table will then filter to show you all the UFO sightings that happened on 1/11/2010 in Flordia, Image 3. 

### Image 3: UFO Signtings on 1/11/2010 in Flordia

![UFO Sightings in Flordia on 1/11/2010](https://github.com/mrma2318/UFOs/blob/442d7d115b8b358b638444af80ab5fa42f255f8f/Resources/Screen%20Shot%202022-11-15%20at%206.47.05%20PM.png)

## Summary
- A drawback to the UFO webpage though is that you can't sort by the categories, you can only filter by category. For example, the signhtings are organized by date, however, if I wanted to sort by city while still seeing all the data. Being able to sort by city for example, allows one to see overall how many sightings one state might have had over the others. Then if they wanted to filter by that state, they could look at that state's sightings in more depth.  

- However, there are a few additional recommendations for further development of the webpage. One recommendation would be to include a clear all button for the filters. In order to remove all the filters, you have to individually go into each filter and clear it. 

- Another recommendation for further development is to further clean the data. For example, the cities and states are all lowercase. Capitalizing those categories appropriately would present a more professional and clean webpage. Some of the comments in the data also have numerical values that could be removed to provide a more cleaner comment section when reviewing the data, Image 4. 

### Image 4

![Comment](https://github.com/mrma2318/UFOs/blob/442d7d115b8b358b638444af80ab5fa42f255f8f/Resources/Screen%20Shot%202022-11-15%20at%207.05.03%20PM.png)