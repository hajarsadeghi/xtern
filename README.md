# xtern
Xtern Internship Data Science


In this Project, I made use of the Google Maps APIs for locations.
First, I found out Indianapolis, Downtown longitude and latitude; then using that information along with other information such as a list of types (the locations I was looking for such as amusement_park, aquarium, etc.), I used Google's nearbysearch API, and search those locations in a 4000 metere radius of Downtown.
I received a number of results, then saved each location's place_id (Google assigns a unique id to each location) in an array to use for place detail search after that.
Using each location's place_id, I used place/details api call, and as parameteres I passed the result I was looking for such as name, reviews, rating, etc.
Then, I droped any results that did not contain a rating because I only wanted top locations to put in my Tour.
Saved all the different locations that I got into an excel file called output, uploaded here as well.
Converted that data into dataframe
Then made a limited result list that categorized locations, and only saved the information I needed.

## Making a plan
In order for me to make a plan, I chose June's first Monday which will be 06.11.2023 as the visiting day
So, I first checked if that location is open on the day and time of visit, and if it will remain open until the time of visit is over.
If that was the case, it would go to the plan.
Furthermore, I used Google APIs distance matrix to find out how much it will take us to get from location A to location B. I chose "driving" as the means of transit for that day; however, if we choose "transit" it will take us longer to get to places, and our plan will change accordingly.

At the end, I save the related data into two spreadsheets called Data.excel and Plan.excel. I have uploaded both here.
Also, I visualized a simple linear plan plot that has the time of visit on the x axis and the locations on the y axis.


## NOTES
If I had more time, I did like to make different plans for interns with different interests, and that's why I got the data for different locations such as stadium, church, etc.

Moreover, we could visualize a more complicated plot that contains a map with different destinations and routes; but again, my time was limited.

Also, Google does not share the visiting time or busy time details for locations in their APIs, and that's why I used constants as visiting times; but if other APIs are available we could add that to the code, and the plan could change.
