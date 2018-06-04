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

# PdfRenderParams function


## -description


Populates a <a href="https://msdn.microsoft.com/1B2F12FB-E053-4B79-B71D-E66D7A6E5054">PDF_RENDER_PARAMS</a> stucture. A PDF_RENDER_PARAMS structure represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.


## -parameters




### -param srcRect [in]

The rectangular portion of the original page, as defined by the D2D_RECT_F structure's upper-left and lower-right corner x- and y-coordinates. The default value is 0.f for all coordinates.


### -param destinationWidth [in]

The specified width of the page. The default is 0.f.



### -param destinationHeight [in]

The specified height of the page. The default is 0.f.


### -param bkColor [in]

The specified background color of the page. The default is {1.f, 1.f, 1.f, 1.f}, which represents the values 1.0 for red, green, blue, and alpha channel, respectively. These values, taken together, represent white at full opacity.


### -param ignoreHighContrast [in]

False to use the system's high contrast display settings; otherwise true. The default is true.


## -returns



Represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.




