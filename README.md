# Interactive Belly Button Biodiversity


An interactive dashboard was created to explore the Belly Button Biodiversity DataSet.



![Bacteria by filterforge.com](Images/bacteria_by_filterforgedotcom.jpg)

In this assignment, you will build an interactive dashboard to explore the [Belly Button Biodiversity DataSet](http://robdunnlab.com/projects/belly-button-biodiversity/).

## Plotly.js Set Up

Used Plotly.js to build interactive charts for the dashboard.

Used the route /names to populate a dropdown select element with the list of sample names.

Used document.getElementById, document.createElement and append to populate the create option elements and append them to the dropdown selector.

Used the following HTML tag for the dropdown selector

<select id="selDataset" onchange="optionChanged(this.value)"></select>
Created a function called optionChanged to handle the change event when a new sample is selected (i.e. fetch data for the newly selected sample).
Created a PIE chart that uses data from the routes /samples/<id> and /otu to display the top 10 samples.

Used the Sample Value as the values for the PIE chart

Used the OTU ID as the labels for the pie chart

Used the OTU Description as the hovertext for the chart

Used Plotly.restyle to update the chart whenever a new sample is selected

Created a Bubble Chart that uses data from the routes /samples/<id> and /otu to plot the Sample Value vs the OTU ID for the selected sample.

Used the OTU IDs for the x values

Used the Sample Values for the y values

Used the Sample Values for the marker size

Used the OTU IDs for the marker colors

Used the OTU Description Data for the text values

Used Plotly.restyle to update the chart whenever a new sample is selected

Displayed the sample metadata from the route /metadata/<id>

Displayed each key/value pair from the metadata JSON object somewhere on the page

Updated the metadata for each sample that is selected

Finally, deployed the Flask app to Heroku.


  ![PIE Chart](Images/pie_chart.png)

*  (`/samples/<sample>`) 

  * Use `otu_ids` for the x values

  * Use `sample_values` for the y values

  * Use `sample_values` for the marker size

  * Use `otu_ids` for the marker colors

  * Use `otu_labels` for the text values

  ![Bubble Chart](Images/bubble_chart.png)

* `/metadata/<sample>`

 
![Example Dashboard Page](Images/dashboard_part1.png)
![Example Dashboard Page](Images/dashboard_part2.png)

## Heroku Set Up

Finally, deployed the Flask app to Heroku.


## Flask API Set Up

Flask API Set Up
Used Flask to design an API for the dataset and to serve the HTML and JavaScript required for the dashboard page. Sqlite database file and SQLAlchemy inside of the Flask application code was used for the database as JSON file format.

Created a template called index.html for the dashboard landing page. Used the Bootstrap grid system to create the structure of the dashboard page.
