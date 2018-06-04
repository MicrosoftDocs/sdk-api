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

# D2D1_PATH_SEGMENT enumeration


## -description


Indicates whether a segment should be stroked and whether the join between this segment and the previous one should be smooth. This enumeration allows a bitwise combination of its member values. 


## -enum-fields




### -field D2D1_PATH_SEGMENT_NONE

The segment is joined  as specified by the <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> interface, and it is stroked. 


### -field D2D1_PATH_SEGMENT_FORCE_UNSTROKED

The segment is not stroked.


### -field D2D1_PATH_SEGMENT_FORCE_ROUND_LINE_JOIN

The segment is always joined with the one preceding it using a round line join, regardless of which <a href="https://msdn.microsoft.com/4368e93e-af69-4555-ac2b-c9c576c81372">D2D1_LINE_JOIN</a>enumeration is specified by the <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> interface. If this segment is the first segment and the figure is closed, a round line join is used to connect the closing segment with the first segment. If the figure is not closed, this setting has no effect on the first segment of the figure. If <a href="https://msdn.microsoft.com/e1162564-a39b-4c16-887e-ec06dd37301c">ID2D1SimplifiedGeometrySink::SetSegmentFlags</a> is called just before <a href="https://msdn.microsoft.com/31f6aeba-2e81-4b8d-b734-0c501eae331f">ID2D1SimplifiedGeometrySink::EndFigure</a>, the join between the closing segment and the last explicitly specified segment is affected.


### -field D2D1_PATH_SEGMENT_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/e1162564-a39b-4c16-887e-ec06dd37301c">ID2D1SimplifiedGeometrySink::SetSegmentFlags</a>



<a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>
 

 

