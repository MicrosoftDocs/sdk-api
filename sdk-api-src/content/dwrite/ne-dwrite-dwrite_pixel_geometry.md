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

# DWRITE_PIXEL_GEOMETRY enumeration


## -description



      
      Represents the internal structure of a device pixel (that is, the physical arrangement of red,
 green, and blue color components) that is assumed for purposes of rendering text.



## -enum-fields




### -field DWRITE_PIXEL_GEOMETRY_FLAT

The red, green, and blue color components of each pixel are assumed to occupy the same point.


### -field DWRITE_PIXEL_GEOMETRY_RGB

Each pixel is composed of three vertical stripes, with red on the left, green in the center, and 
     blue on the right. This is the most common pixel geometry for LCD monitors.	  
	  


### -field DWRITE_PIXEL_GEOMETRY_BGR

Each pixel is composed of three vertical stripes, with blue on the left, green in the center, and 
	  red on the right.

