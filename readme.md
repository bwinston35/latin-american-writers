# Original data
This data comes from the [Archives of Latin American Writers and Intellectuals in Special Collections: Literary Archives LibGuide](https://libguides.princeton.edu/latinammss) that Fernando Acosta-Rodríguez created. The guide is a list of collections at Princeton University that hold the correspondence, manuscripts, and other writings of Latin American authors and intellectuals.

The extraction of the data from this list occurred March 25, 2024. There is a chance that the guide has been updated since this data was extracted.

# Transformation of data
The dataset was transformed with the tool OpenRefine and by leveraging its reconcilliation method to access the Wikidata API. It's primary purpose is for instructional purposes in workshops and iterative project design. Therefore some of the transformation choices made to develop a useable dataset has excluded some of the original information contained in the above mentioned LibGuide.

Below is a sketch of the changes made to the original list as well as the information added to prepare this dataset for mapping and other visualizations.

## Edits and removals
- An author column was addedd so taht author names could be extracted from collection lists.
- An organizer column was added to represent other names listed in a collection title. This column was determined by additional wording in collection such as Joe Smith’s correspondence with Latin American Writers. If unclear but papers include Spanish surname that defaulted to author rather than organizer.
- If a collection had more than one author listed in its title, a new row was added and the collection title was duplicated in relation to an additional author.
- If an author appears more than once throughout the list, only one mention is retained. Therefore the dataset only represents unique mentions of an author. The primary purpose of this dataset is represent demographic information about authors and intellectuals within Princeton collections.
- If the OpenRefine reconciliation method did not easily match an author's name to the external Wikidata database, that author was excluded from the dataset. There is hope that additional research and manual editing will result in the incorporation of these authors in a future iteration of the project.
- If a collection did not clearly identify author(s) contained in the collection, that collection (and author's potentially present in that collection) are not included in the dataset.

## Additions
Information was added to the dataset with the assistance of the OpenRefine reconciliation method and its use of the Wikidata API. When necessary, some information was added manually (such as location coordinates of a city that was not include in the Wikidata database). The additional information includes:

- place of birth
- place of death
- coordinates at the city/town level
- country of birth
- country of death
- country of citizenship
- sex or gender
- spouse

Not every corresponding author entry on Wikidata included all of the above additional information, so if it was not easily findable, that cell was left blank in the dataset.

# Current state of dataset
The transformed dataset remains in the state listed above. I have also created simplified spreadsheets with some of the information above to produce maps and other visualizations that are part of a ArcGIS StoryMaps project.

_last updated 2015-04-15_