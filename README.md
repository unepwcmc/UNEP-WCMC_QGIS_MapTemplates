# UNEP-WCMC map templates for QGIS

## Connect QGIS to portal using oauth2 authentication

*Original source based on https://north-road.com/2022/09/16/securely-accessing-arcgis-online-agol-and-enterprise-arcgis-portal-sites-through-qgis-2022-update/*

### 1. Download files from GitHub

 - Click on the green 'Code' button and click 'Download ZIP' (if you are a GitHub user you can alternatively choose to oprn with GitHub Desktop)
- Save the Zip file to a folder on your computer. 
- Navigate to the folder and unzip the file.
- In here you will find the files from this repository.

### 2. Copy the QGIS portal authorisation file to the QGIS profiles folder
- In a windows explorer window copy the downloaded file to your QGIS profiles folder located in AppData
*(Note: if you can’t see the folder you may need to tell your windows explorer to be able to see hidden folder by going to View >>>show hidden items)*
e.g. your QGIS profile folder should be in your user AppData folder i.e.  C:\Users\Corinnar\AppData\Roaming\QGIS\QGIS3\profiles\default

![image1](media/image1.png)

### 3. Set up the portal connection in QGIS

- Open QGIS
- Navigate to **Layers>>Data Source Manager**

![image2](media/image2.png)

- Fill out the following parameters
**Name:** UNEP-WCMC portal
**URL:** https://data-gis.unep-wcmc.org/server/rest/services/
**Community endpoint URL:** https://data-gis.unep-wcmc.org/portal/sharing/rest/community/
**Content endpoint URL:** https://data-gis.unep-wcmc.org/portal/sharing/rest/content/
- In the new window enter the following parameter
**Name:** UNEP-WCMC portal
**Resource:** https://data-gis.unep-wcmc.org/portal/sharing/rest/
- In the box underneath resource pick **Oauth2 authentication**
- In the row labelled grant flow Click the blue down arrow button and navigate to the gis profile folder where you placed the authentication file and select the file.
i.e. C:\Users\Corinnar\AppData\Roaming\QGIS\QGIS3\profiles\default\QGIS_oauth2_UNEP_WCMC.json

