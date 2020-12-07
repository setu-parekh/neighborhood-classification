# Kuala Lumpur Neighborhood Classifier
Neighborhood classification in the city of Kuala Lumpur for opening a new restaurant.

## Summary
* [Introduction & General Information](#introduction--general-information)
* [Objectives](#objectives)
* [Data Used](#data-used)
* [Approach & Methodology](#approach--methodology)
* [Run Locally](#run-locally)
* [Observations](#observations)
* [Recommendations](#recommendations)

## Introduction & General Information
(source: https://www.wikiwand.com/en/Kuala_Lumpur)
- Kuala Lumpur, officially the Federal Territory of Kuala Lumpur and colloquially referred to as KL, is a federal territory and the capital city of Malaysia.
- It is the largest city in Malaysia, covering an area of 243 sq km (94 sq mi) with an estimated population of 1.73 million as of 2016.
- Greater Kuala Lumpur, also known as the Klang Valley, is an urban agglomeration of 7.564 million people as of 2018.
It is among the fastest growing metropolitan regions in Southeast Asia, in both population and economic development.

## Objectives
- Selection of a prime location while opening a new restaurant business is one of the most important decision, having a profound impact on the business's success or failure.
- If the restaurant is opened in an area where there is already a very high competition and established businesses of the same kind, the new restaurant might not be as successful. On the other hand, if it is opened in an area where there is very less competition, the new business might get established in very short period and start earning good profits.
- This project is aimed at analyzing the data and using different machine learning techniques to determine the best possible cluster of neighborhoods where a new restaurant will have the highest possible chance at success.

## Data Used
- In this project, the neighborhood data is collected from Wikipedia pages by scrapping and post-processing.
- In addition to that, [Foursquare API](https://developer.foursquare.com/docs/) is used to explore different venues within the neighborhoods, based on different restaurant categories.

## Approach & Methodology
- Perform web scrapping and post-processing of wikipedia pages to obtain information on different neighborhoods of Kuala Lumpur.
- Get latitude and longitude of above neighborhoods using [Geocoder Package](https://geocoder.readthedocs.io/).
- Use [Foursquare API](https://developer.foursquare.com/docs/) to get data of different venues within the neighborhoods.
- Group the venue data by neighborhood and calculate the mean frequency of each restaurant category within the venues.
- Filter the resulting venue categories by restaurants.
- Apply K-means Clustering to generate different clusters from above data.
- Visualize the generated clusters in a map of Kuala Lumpur using [Folium](https://python-visualization.github.io/folium/).
- Analyze the results.

## Run Locally
* Make sure Python 3 is installed. Reference to install: [Download and Install Python 3](https://www.python.org/downloads/)
* Clone the project: `git clone https://github.com/setu-parekh/neighborhood-classification.git`
* Route to the cloned project: `cd neighborhood-classification`
* Install necessary packages: `pip install -r requirements.txt`
* Run Jupyter Notebook: `jupyter notebook`
* Select the notebook to open: `neighborhood_classification.ipynb`

## Observations
- Most of the restaurants are concentrated in the central area of Kuala Lumpur city, with the highest number in cluster 2 (shown in mint green color) and moderate number in cluster 1 (shown in red color).
- On the other hand, cluster 0 (shown in purple color) has comparatively very less number of restaurants in the neighborhoods.
- This represents a great opportunity and high potential areas to open new restaurant as there is very little competition from the existing ones.
- Meanwhile, restaurants in cluster 2 are most likely suffering from intense competition due to high concentration of restaurant options available.

![Neighborhood Clusters](https://github.com/setu-parekh/neighborhood-classification/blob/main/neighborhood_clusters.png)

## Recommendations
- Investors are recommended to capitalize on these findings and open new restaurant in neighborhoods in cluster 0 (shown in purple color) with little competition.
- Investors with unique cuisine propositions to stand out from the competition can also open new restaurant in neighborhoods in cluster 1 (shown in red color) with moderate competition.
- Lastly, investors are advised to avoid neighborhoods in cluster 2 (shown in mint green color) which already have high concentration of restaurants and suffering from intense competition.
