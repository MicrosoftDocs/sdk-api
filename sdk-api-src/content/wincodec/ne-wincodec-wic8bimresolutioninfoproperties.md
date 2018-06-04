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

# WIC8BIMResolutionInfoProperties enumeration


## -description


Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block.


## -enum-fields




### -field WIC8BIMResolutionInfoPString

[VT_LPSTR] A name that identifies the 8BIM block.


### -field WIC8BIMResolutionInfoHResolution

[VT_UI4] The horizontal resolution of the image.


### -field WIC8BIMResolutionInfoHResolutionUnit

[VT_UI2] The units that the horizontal resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.


### -field WIC8BIMResolutionInfoWidthUnit

[VT_UI2] The units that the image width is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.


### -field WIC8BIMResolutionInfoVResolution

[VT_UI4] The vertical resolution of the image.


### -field WIC8BIMResolutionInfoVResolutionUnit

[VT_UI2] The units that the vertical resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.


### -field WIC8BIMResolutionInfoHeightUnit

[VT_UI2] The units that the image height is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.


### -field WIC8BIMResolutionInfoProperties_FORCE_DWORD



