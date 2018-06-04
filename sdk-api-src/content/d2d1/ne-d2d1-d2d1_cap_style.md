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

# D2D1_CAP_STYLE enumeration


## -description


Describes the shape at the end of a line or segment.


## -enum-fields




### -field D2D1_CAP_STYLE_FLAT

A cap that does not extend past the last point of the line. Comparable to cap used for objects other than lines. 


### -field D2D1_CAP_STYLE_SQUARE

Half of a square that has a length equal to the line thickness.


### -field D2D1_CAP_STYLE_ROUND

A semicircle that has a diameter equal to the line thickness.


### -field D2D1_CAP_STYLE_TRIANGLE

An isosceles right triangle whose hypotenuse is equal in length to the thickness of the line.


### -field D2D1_CAP_STYLE_FORCE_DWORD




## -remarks




The following illustration shows the available cap styles for lines or segments. The red portion of the line shows the extra area added by the line cap setting.



<img alt="Illustration of four cap styles" src="images/linecaps.png"/>


