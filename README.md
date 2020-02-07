# routemapping_josmconfig

This repository contains the necessary files to make it easier for you to actually concentrate on mapping (bus) routes via JOSM. It is a project for Trufi Association.

![](img/routemapping-look.png)

# Good to know

This repository contains the necessary files needed to make bus route mapping in JOSM even better. It does not contain JOSM itself but you can download JOSM for Linux, Mac or Windows from [here](https://josm.openstreetmap.de).

> **What is JOSM?**
> 
> JOSM is an extensible editor for [OpenStreetMap](https://welcome.openstreetmap.org/what-is-openstreetmap/). OpenStreetMap itself is a project to create a free and editable map for anyone by anyone. JOSM is a highly advantage tool to actually contribute to OSM by letting you add objects that represent real world objects to the database.

The documentation does not explain how to [set up JOSM](https://github.com/ValorNaram/trufi_documentation/blob/master/installing-josm-on-linux/installing-josm-linux.md) nor to [link it to your OSM account](https://github.com/ValorNaram/trufi_documentation/blob/master/oauth-josm/oauth-josm.md) but it explains how to tweak JOSM to make it easier to [add bus routes to OSM](https://github.com/ValorNaram/trufi_documentation/blob/master/mapping-routes/mapping-routes.md). JOSM itself is complicated enough so we decided to simplify it for our purpose. Our guidelines will show how do you tweak our tool to suit your needs.

## Prequesites

We recommend you to have a (basic) understanding of OpenStreetMap and its tagging schematics. It does not matter, if you ever worked with JOSM - the editor - or not. We have also set up a [documentation on how to set up JOSM and how to actually map bus routes](https://github.com/ValorNaram/trufi_documentation/blob/master/README.md) via JOSM.

# Changing our tool to suit your needs

Before you even start to distribute our tool to your community you need to tweak it to suit the needs of your community.

## Prepare your workplace

1. Juat concentrate on our tutorial. Don't listen to music and do not another unrelevant stuff.

2. Fork this repository

3. Clone this repository onto your computer

4. Change into the newly created folder

## Editing `trufi_presets.xml`

This is actually the really important part which will also take the most time.

1. Open XML file `trufi_presets.xml`.

2. The file is documented. You should understand it. But here are some aspects good to know. The following three images show you the schematics of UI creation in preset means. It shows you which part of the preset code does which part of the UI. Study the images carefully:
   
   ![](img/WYSIWYG-01.png)![](img/WYSIWYG-02.png)![](img/WYSIWYG-03.png)
   
   ## Preparing preset for production use.
   
   1. Compress the XML file `trufi_presets.xml` into a zip archive.
      
      - Structur of the zip archive:
        
        - `trufi_presets.zip` (or another name)
          
          - `trufi_presets.xml`
   
   2. Upload the zip file to the repository on GitHub.
   
   3. Go to GitHub
   
   4. Go to the online repository.
   
   5. Click on the file you uploaded in step 2.
   
   6. Copy the hotlink of the file into your clipboard.

## Editing `josmconfig-trufi-routes.xml`

The XML contains the configuration for JOSM and the plugins to be installed. Editing it is pretty easy because we've done the most work for you.

1. Open XML file `josmconfig-trufi-routes.xml` .

2. Search for the line that looks like:
   
   ```xml
   <tag key="url" value="https://github.com/SamuelRioTz/Trufi-Presets/releases/download/v1.0.5/trufi.zip"/>
   ```

3. Change the value `https://github.com/SamuelRioTz/Trufi-Presets/releases/download/v1.0.5/trufi.zip` to the url pointing to the zip file you uploaded into your repository on GitHub by inserting the new value from your clipboard.

4. Save your work and close your text editor.

## Finalization

Upload all your changes to GitHub and follow the tutorial [here](https://github.com/ValorNaram/trufi_documentation/blob/master/installing-mapping-tool/install-bus-routes-mapping-tool.md) in order to activate your customized version of our tool in JOSM. Distribute the file `josmconfig-trufi-routes.xml` and nothing else to your community. Point them also to the tutorial on [how to install your customized version of our tool for mapping bus routes in JOSM](https://github.com/ValorNaram/trufi_documentation/blob/master/installing-mapping-tool/install-bus-routes-mapping-tool.md) so they know what do you. You should also consider pointing them to [our comprehensive guide on using JOSM for mapping bus routes](https://github.com/ValorNaram/trufi_documentation/blob/master/README.md).


