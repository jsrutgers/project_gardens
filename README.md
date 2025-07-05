# Boulevard gardens make this Winnipeg neighbourhood special. Are they for everyone?
---

### Description: 
There are more than 350 homes in the Wolseley neighbourhood with gardens that drift onto the boulevard — a strip of turf the homeowner maintains, but the city controls. 

These gardens are a well known quirk of the community and serve as both local flavour and beneficial green infrastructure. They're also regulated by neighbourhood liveability bylaws, and can sometimes require a permit or be subject to inspection and compliance orders. 

This analysis set out to map the neighbourhood's gardens (by foot and bike) in order to understand which parts of the neighbourhood have the easiest access to these character features. 

The garden locations were analysed against average property assessment values in different geographic regions of the neighbourhood to see whether a high density of gardens was more likely in the more expensive parts of the mixed-income neighbourhood. 

This was an effort to strengthen my data-cleaning skills and my ability to wrangle and ask questions of relatively large datasets.

In the end, it turns out Woleseley's gardens are well-distributed across the neighbourhood, and are the least densely clustered in the most expensive parts of the community.
---

## Contents:

> notebooks: 

    `01_boulevard_gardens_cleaning` - cleaning assessment parcel data and merging with garden data


    `02_boulevard_gardens_analysis` - property value/garden density analysis

    (this folder also includes input datasets)

> output_data:

   `00_boulevard_gardens_data` - all datasets created through the analysis, as well as all datasets used for visualization

> extras - map:
     geojson files used to map the neighbourhood gardens

> graphics: 
    png copies of datawrapper graphics.



### Garden data collection:

Over the course of three days, I walked or cycled the length of every street in the Wolseley neighbourhood, using a paper street map as a guide, and recorded the street number and street name of each boulevard garden I saw. 

The definition of a boulevard garden for the purpose of the project was limited to deliberately planted gardens on city-owned property with more than one variety of plant. 

More detailed explanations, as well as steps to  can be found in the data cleaning notebook or on the website.
---

# Cleaning and Analysis:

1. Read in and cleaned City of Winnipeg assessment parcel data for the Wolseley neighbourhood to retain addresses and assessement values, filtering out parcels that were not homes or businesses. This step involved several (scary!) editorial decisions which are explained in the data cleaning notebook.
2. Merged this cleaned data with the list of properties that have boulevard gardens to compile a dataset with: every residential and commercial property in Wolseley, its assessed property value, whether or not it has a boulevard garden and basic geometries for the centroid and lot shape.
3. Analysed clean data to answer questions about the relationship between property value (taken to represent the relative "wealth" of a particular part of the neighbourhood) and the proportion of boulevard gardens per home in the same area.
4. Created fields to analyse the data by geographic regions: north/south and west/central/east in order to assess whether the most expensive geographic areas of the region (the south and west) had a higher proportion of gardens. The full methodology for these divisions is explained in the data analysis notebook.
5. Created basic graphs throughout the analysis to answer questions and draft charts for later data viz.
---

# The Learnings:

I feel I bit off a bit more than I could chew with this project out the gates. The data collection process was very fun and special — and there are _many_ reasons I'm glad I went through with it. But it also took a lot of time. The data cleaning and analysis seems simple on paper, but there were several snags along the way, and I lost a lot of time fighting my inner perfectionist about the editorial decisions needed to just keep the project moving. 

In the end, I did fight off that perfectionism, and as a result I think there are small holes in the analysis along the way, though I've done my best to explain my decisions transparently.

This kind of analysis, looking for the andwers to specific questions in large datasets, feels like bread and butter of integrating Python into the work I already do as a journalist, and I wanted to dip my feet into that process and build some muscle memory with the languages and tools. I came away more comfortable with pandas, and more capable of sifting through possible solutions to my problems to find the ones I could kind of understand and put to use in a couple contexts. 

I originally wanted to deep dive into the 311 enforcement data and understand what parts of the city are least amenable to boulevard gardens, whether the bylaws are consistently enforced (early indications say no...a project for another time) and how often people go through the permitting applucation process. I found hints of this data, but I felt the project getting unwieldy, and detailed enforcement information would likely require a freedom of information request or some skill I have yet to learn.