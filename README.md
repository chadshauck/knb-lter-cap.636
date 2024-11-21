## knb-lter-cap.636

### CAP LTER 10-m towers at Lost Dutchman State Park and the Desert Botanical Garden

This repository features the workflow for publishing the 10-m tower data, documentation relating to tower equipment and operation, and a log of equipment maintenance (mostly sensor calibration or replacement).

- data processing and upload: the workflow for processing and uploading tower data to the database has been moved from this repository to the [capmicromet](https://gitlab.com/caplter/capmicromet) R package.
- database details are in the [capmicromet-database](https://gitlab.com/caplter/capmicromet-database) repository
- CAP LTER technicians should please annotate the `maintenance_log.csv` file in this repository with all maintenance activities relating to this project


#### knb-lter-cap.636.15

- fix data foramtting error identified in version 14
- add checks to (help) ensure that data are in wide format

#### knb-lter-cap.636.14

- long format data published to EDI; immediately corrected in version 15
- data refresh

#### knb-lter-cap.636.13

- data refresh
- whereas pervious versions used `capeml::harvest_dataTable` to harvest metadata for older (2006..., 2011...) data so as not to have to download and manage data prior to 2020, this version does download all data and builds the EML from raw data downloads. This was in response to a problem that in fact turned out to be an AWS issue so, going forward, we could continue this approach or go back to harvesting metadata so as to limit the download, processing, and uploading.

#### knb-lter-cap.636.12

- data refresh
- Rmd to qmd
- add capeml::update_attributes() function to workflow for new data
- new datasource for personnel metadata


#### knb-lter-cap.636.10

- split observations into approximately decadal intervals to address the large and increasingly unwieldy file size resulting from encapsulating all data into a single file
- added disturbance to keyword list


#### knb-lter-cap.636.9

- data refresh
- as part of this refresh, we noticed that the logger at the DBG site is not recording data in the evening hours
