# Analysis of Google Play store and Apple App Store datasets in Power BI

### PBI File Download Link: https://1drv.ms/f/s!AkoBr2G6O_RZkvUyy1ZdBPE3xyv-xw?e=6aMjIE
### Data sets:
- Google: https://www.kaggle.com/datasets/gauthamp10/google-playstore-apps
- Apple: https://www.kaggle.com/datasets/gauthamp10/apple-appstore-apps

## Objectives:

The main purpose of this project was to conduct exploratory data analysis of the dataset using Power BI in order to achieve the following:

  1. Identify the share of paid and free apps.
  2. Determine the most popular categories of apps.
  3. Analyze the most popular apps in the most popular category.
  4. Acertain app abandoment rate and average length of support.
  5. Assess the number of installations per category.
  6. Calculate the mean price per category.
  7. Explore the distribution of app ratings.
  8. Explore the relationship between ratings and price of apps.


## Methodology

### Data Cleaning and Preprocessing:

- Ensured data integrity by cleaning and preprocessing the dataset.
- Loaded data from a CSV file.
- Handled missing values by dropping corresponding entries.
- Performed data type conversions where needed.
- For the play store, apps that contained "Google" or "Android" were filtered out as they represented either system apps or apps downloaded by default during activation, thus skewing the numbers.

### Exploratory Data Analysis (EDA):

- Conducted EDA to understand the dataset.
- Created various visualizations:
    - Bar charts: used to compare categorical data.
    - Pie charts: represented proportions or percentages.
    - Histograms: displayed distribution of continuous variables.
    - Box plots: Showed data spread and helped identify outliers.
    - Scatter plots: Revealed relationships between two variables.

## Findings

### Android:

- App store consists of 98% free apps and 2% paid apps.
- Top 10 free categories are dominated by tools, communication and entertainment related apps.
- Top 10 paid categories are entertainment/gaming related with a smaller footprint of tools in the mix.
- Developers of paid apps publish less frequently but support the apps for longer periods of time.
- Top 3 app categories by average price are: dating, medical and business.
- Top 3 most supported app categories are: dating, finance and shopping.
- Top 3 least supported app categories are: events, arcade and libraries & demo.
- Paid apps are supported on average 2x as long as free apps.
- Distribution of ratings is left skewed with an average of 4.2 and median of 4.20.
- Ratings increase over time while app abandonment decreases.
- Apps that are paid, have no ads and have in app purchases are supported the longest.
- Apps that are free, with ads and have no in app purchases are supported the least.
- 50% of apps are priced between $0.99 and $1.99, the remaining 50% ranges between $2 and $8.
- The correlation between app price and rating is very weak.

### Apple:

- App store consists of 91.7% free apps and 8.3% paid apps.
- Top 10 free categories are dominated by games, business, productivity and entertainment related apps towards the end.
- Top 10 paid categories follow the same trend as the free ones but with a higher emphasis on education.
- Developers of paid apps publish more frequently and support the apps for twice as long.
- Top 3 app categories by average price are: graphic design, business, medical.
- Top 3 most supported app categories are: finance, shopping, graphic design.
- Top 3 least supported app categories are: stickers, games, photo/video.
- Distribution of ratings is left skewed with an average of 4 and median of 4.52.
- Ratings increase over time while app abandonment decreases.
- Paid apps enjoy longer support but have lower ratings.
- 50% of apps are priced between $0.99 and $1.99, the remaining 50% ranges between $2 and $10.99.
- The correlation between app price and rating is very weak.

## Notes

  1. The apple app store does not contain install data, so the number of released apps by category was used instead. The reasoning behind this was that in the play store detaset the rankings of categories by no. of released matched the rankings by no. of installs.
  2. An abandoned app was defined as an app that had it's last update date more than 12 month before the latest date of update of the dataset.
  3. The boxplots have the outliers already filtered out. Those have been determined by using a distance of 1.5 x IQR.
  4. The above findings are just a short summary. More details can be found in the analysis alongside a visual comparison between the 2 app stores.
  5. If one desires to use power query to make further modifications to the data, the location within the M code for the 2 datasets will need to be updated with the address where the "Base data" folder from the download link has been placed.
