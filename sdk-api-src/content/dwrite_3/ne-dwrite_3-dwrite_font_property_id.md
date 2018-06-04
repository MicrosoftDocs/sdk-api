---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DWRITE_FONT_PROPERTY_ID enumeration


## -description


Identifies a string in a font.


## -enum-fields




### -field DWRITE_FONT_PROPERTY_ID_NONE

Unspecified font property identifier.


### -field DWRITE_FONT_PROPERTY_ID_WEIGHT_STRETCH_STYLE_FAMILY_NAME


### -field DWRITE_FONT_PROPERTY_ID_TYPOGRAPHIC_FAMILY_NAME


### -field DWRITE_FONT_PROPERTY_ID_WEIGHT_STRETCH_STYLE_FACE_NAME


### -field DWRITE_FONT_PROPERTY_ID_FULL_NAME

The full name of the font, for example "Arial Bold", from name id 4 in the name table.


### -field DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME

GDI-compatible family name. Because GDI allows a maximum of four fonts per family, fonts in the same family may have different GDI-compatible family names,
          for example "Arial", "Arial Narrow", "Arial Black".


### -field DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME

The postscript name of the font, for example "GillSans-Bold", from name id 6 in the name table.


### -field DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG

Script/language tag to identify the scripts or languages that the font was primarily designed to support.


### -field DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG

Script/language tag to identify the scripts or languages that the font declares it is able to support.


### -field DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG

Semantic tag to describe the font, for example Fancy, Decorative, Handmade, Sans-serif, Swiss, Pixel, Futuristic.


### -field DWRITE_FONT_PROPERTY_ID_WEIGHT

Weight of the font represented as a decimal string in the range 1-999.


### -field DWRITE_FONT_PROPERTY_ID_STRETCH

Stretch of the font represented as a decimal string in the range 1-9.


### -field DWRITE_FONT_PROPERTY_ID_STYLE

Style of the font represented as a decimal string in the range 0-2.


### -field DWRITE_FONT_PROPERTY_ID_TYPOGRAPHIC_FACE_NAME


### -field DWRITE_FONT_PROPERTY_ID_TOTAL

Total number of properties.


### -field DWRITE_FONT_PROPERTY_ID_TOTAL_RS3


### -field DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME

Family name preferred by the designer. This enables font designers to group more than four fonts in a single family without losing compatibility with
          GDI. This name is typically only present if it differs from the GDI-compatible family name.


### -field DWRITE_FONT_PROPERTY_ID_FAMILY_NAME

Family name for the weight-width-slope model.


### -field DWRITE_FONT_PROPERTY_ID_FACE_NAME

Face name of the font, for example Regular or Bold.

