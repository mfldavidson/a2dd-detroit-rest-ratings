# A2 Data Dive Detroit Restaurant Ratings and Violations
As a part of the 2019 A2 Data Dive, we compared Yelp ratings with health code violations of restaurants in the City of Detroit to see if there is correlation between the two. Our hypothesis was that a lower Yelp rating is correlated with a higher number of health code violations. Restaurant owners know how important a high Yelp rating is to having a successful business, so if we could show that restaurants with higher violations tend to have lower Yelp ratings, this could be used as an incentive for restaurants to comply with the health code. Furthermore, low ratings on Yelp could be used by the City of Detroit to prioritize restaurant inspections.

_Null hypothesis:_ There is no correlation between the Yelp rating and the number of health code violations for a restaurant
_Alternate hypothesis:_ There is correlation between the Yelp rating and the number of health code violations for a restaurant

The people who worked on this project and their contributions are:
- [Joshua Walker](https://github.com/joshwalk/) - Yelp API calls
- [Bryan Romas](https://github.com/bcromas/) - analysis
- [Maggie Davidson](https://github.com/mfldavidson/) - documentation and planning
- [Yuan Li](https://github.com/yuanli/) - visualization
- [Taika](https://github.com/taikaa/)

## Step 1: Restaurant Establishments
We started by working off of the [Establishments dataset](https://docs.google.com/spreadsheets/d/1W1EAY48Mm0h7zrBHhMnKbPozyxzG-ZdhGVla8nHwhrI/edit#gid=213667838) provided by the A2 Data Dive.

## Step 2: Yelp API
We wanted to get the Yelp Rating (out of 5) for each establishment in the Establishments dataset. We used Python to make requests to the [Yelp API business search endpoint](https://www.yelp.com/developers/documentation/v3/business_search) with [Geoffrey Fairchild's yelpapi package.](https://github.com/gfairchild/yelpapi) We used the fields Name, Address, and Zip Code to find the business and return a dictionary with data about the business, including the rating.

## Step 3: Count Violations
