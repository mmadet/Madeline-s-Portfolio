<div align = 'right'>
Nicholas Alonzo - 998455301 <br>
Ethan Bell - <br>
Hanxiaoxin Wang - 913459751 <br>
Madeline Ye - 998108849<br>
</div>

# <center> UFO Sightings and Natural Disasters: A Coincidence? </center>

In this analysis, we'll be looking at two data sets, UFO sightings in the United States and natural disasters from the years 1965 to 2013. We'll first be exploring the data sets indivdually before investigating whether sightings coincide with natural disaters. The UFO sightings data was scraped from the <a href='http://www.nuforc.org/webreports.html'>National UFO Reporting Center Database</a> and uploaded to <a href='https://www.kaggle.com/NUFORC/ufo-sightings'>Kaggle</a> for download. The download came with 2 files (complete and scrubbed); We'll be working with the scrubbed version which has complete reports. The natural disasters data was downloaded from the  <a href='https://www.fema.gov/openfema-dataset-disaster-declarations-summaries-v1'>Federal Emergency Management Agency (FEMA)</a> and has full documenation.

# Data Description:

<u> UFO Sightings </u> <br>
__datetime__: date/timestamp of UFO seen <br>
__city__: city in a US state <br>
__state__: state in the US <br>
__country__: US <br>
__shape__: shape of UFO reported <br>
__duration (seconds)__: how many seconds UFO was reported seen <br>
__duration (hours/min)__: how many hours/min UFO was reported seen <br>
__comments__: comments from person who reported the incident <br>
__date posted__: the date/timestamp posted on the NUFORC page <br>
__latitude__: latitdude of the sighting <br>
__longitude__: longitude of the sighting <br>

<u> Natural Disasters </u> <br>
__state__: string	The name or phrase describing the U.S. state, district, or territory. <br>
__declarationDate__: Date the disaster was declared. <br>
__disasterType__: Two character code that defines if this is a major disaster, fire management or emergency declaration. For more information on the disaster process, please visit: www.fema.gov <br>
__incidentType__: Type of incident such as fire or flood. The incident type will affect the types of assistance available. For more information on incident types, please visit: www.fema.gov <br>
__title__: Title for the disaster. <br>
__incidentBeginDate__: Date the incident itself began. <br>
__incidentEndDate__: Date the incident itself ended. <br>
__placeCode__: The area's FIPS area code. <br>
__declaredCountyArea__: The name or phrase describing the U.S. county that was included in the declaration. <br>


# Goal:

First clean both data sets and explore them individually then TRY and combine both data sets together to explore by county. To match the UFO Sightings to the data from the Natural Disasters data set we can use FIPs codes. This might be a good resource for the <a href='https://www.census.gov/geo/reference/codes/cou.html'>FIPs</a>. Since there's 4 of us, it may be ideal for us to do 2 questions each for a total of 8 questions or do about 6 questions and some that are fairly difficult. The first steps is the pre-processing of the data, and then we can start looking into different packages that will allow us to do some EDA. It's good practice to document a resource you use by adding the link you got help from.


### Pre-Processing: UFO Sightings
Get the row indices as datetime
Select US from 1949 to 2013

### Pre-Processing: Natural Disasters
Get the row indicies as declaration date
Select from 1949 to 2013
Select only natural disasters
Get a latitude and longitude for the counties, use some geocode API or package

### Pre-Processing: Combining Data Sets
Use another resource (download/site) for getting the FIPs for each city in the UFO sightings data set. This way it can be mapped to the Natural Disasters data set.

### Potental Questions To Answer

#### UFO Sightings
- Plot the UFO sightings on the US by state using color intensity
- During what month do more UFO sightings appear?
- What days of the week were most UFOs seen?
- How quickly does a UFO sighting get posted relative it to being seen?
- What are the top 10 places in CA where most UFOs are seen?
- Is there a difference between the UFO shapes seen in the different regions of the US?
- How many people reported being scared?
- What are the top 5 sightings that were reported by multiple people and where were they reported?

#### Natural Disasters
- Plot natural disasters by state using color intensity
- During what month do more natural disasters happen?
- Plot the number of natural disasters from 1949 to 2013 by month
- How many natural disasters happened by state?
- How many natural disasters by cateogory happened in the US?
- What year had the most natural disasters and which states contributed the most to it?

#### UFO Sightings and Natural Disasters
- Is there a similiar increase of UFO sightinigs when there are more Natural Disasters, by month?
- For the top county with the highest count of natural disasters, are there similar counts of reported UFO sightings?
- Is there some association with a UFO shape and the type of natural disasters that happen?
- Do UFOs appear more during natural disasters that last a day VS that last longer than a day, by a count/state?


