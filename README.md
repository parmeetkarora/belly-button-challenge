# belly-button-challenge

Belly Button Biodiversity Dashboard
In this assignment, you will build an interactive dashboard to explore the Belly Button Biodiversity dataset. This dataset catalogs the microbial species that inhabit human navels, offering a fascinating glimpse into the diverse community of microbes that live on and inside us.
Dataset Context
The dataset in question contains valuable information about various microbes, also known as operational taxonomic units (OTUs), that are commonly found in human belly buttons. Analysis of this dataset reveals a notable pattern: a small subset of microbial species is highly prevalent, being present in more than 70% of people. Conversely, the majority of microbial species are relatively rare and are found in only a few individuals. This distribution highlights the prominence of certain bacterial species in the human population while underscoring the vast diversity of less common microbes.
Interactive Dashboard Features
The dashboard you will create serves as an interactive tool for visualizing and exploring the Belly Button Biodiversity dataset. It provides two key components:
1.	Metadata Panel:
Purpose: This panel displays demographic information about the selected test subject.
Details Included: Data such as age, gender, ethnicity, and other relevant attributes will be presented.
2.	Charts:
	Bar Chart:
	Purpose: This chart shows the top 10 most abundant bacteria cultures found in the selected sample.
	Title: "Top 10 Bacteria Cultures Found."
	Description: It displays the number of bacteria (sample values) against their operational taxonomic units (OTU IDs), providing insight into which bacteria are most prevalent in the sample.
	Bubble Chart:
	Purpose: This chart visualizes the relationship between the number of bacteria and their OTU IDs across the sample.
	Title: "Bacteria Cultures Per Sample."
	Description: It represents each OTU as a bubble, where the size of the bubble corresponds to the number of bacteria present and the color reflects different OTUs. This allows for an immediate visual understanding of the distribution and abundance of various bacterial species.
Interactive Features
•	Dropdown Menu:
o	Allows users to select different test subjects to view their specific data.
o	Automatically updates the metadata panel and the charts based on the selected sample.
•	Real-Time Data Visualization:
o	The dashboard updates the bar and bubble charts dynamically to reflect the data of the selected test subject, enabling users to easily compare different samples and explore the biodiversity of bacteria in various individuals.
By creating this interactive dashboard, you will not only practice data visualization techniques but also gain insights into the microbial communities that thrive on human bodies, enhancing your understanding of both the data and the broader implications of microbial diversity.
EXPLAINATION OF CODE

1.	Function to Build the Metadata Panel (buildMetadata):
o	This function reads the samples.json file using D3 and extracts the metadata information.
o	It filters the metadata based on the selected sample ID.
o	It selects the #sample-metadata element and clears any existing metadata.
o	It then iterates through the key-value pairs of the sample metadata and appends them as h6 elements to the panel.
2.	Function to Build the Charts (buildCharts):
o	This function also reads the samples.json file using D3 and extracts the sample data.
o	It prepares the data required for the Bubble Chart and Bar Chart.
o	For the Bubble Chart, it defines the layout and data for the chart, including the OTU IDs, sample values, and labels. It then creates the Bubble Chart using Plotly.
o	For the Bar Chart, it selects the top 10 OTUs, prepares the data for the chart, and creates the Bar Chart using Plotly.
3.	Function to Initialize the Dashboard (init):
o	This function initializes the dashboard by reading the samples.json file using D3 and extracting the sample names.
o	It populates the dropdown menu with the sample names.
o	It selects the first sample from the list, builds the charts, and displays the metadata for that sample.
4.	Function to Update Charts/Metadata when a New Sample is Selected (optionChanged):
o	This function is called when a new sample is selected from the dropdown menu.
o	It updates the metadata panel and rebuilds the charts for the newly selected sample.
5.	Initialize the Dashboard:
o	The init function is called to set up the dashboard when the page loads. It populates the dropdown menu, builds the initial charts, and displays the metadata for the first sample.

=======
>>>>>>> 95e93516a71131e833ad1be82ba0c884b087cb8a
