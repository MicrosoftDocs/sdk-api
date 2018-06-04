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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0007 enumeration


## -description


Describes the joint made by two intersecting line segments.


## -enum-fields




### -field XPS_LINE_JOIN_MITER

Produces a sharp or clipped corner, depending on whether the length of the miter exceeds the miter limit. 


### -field XPS_LINE_JOIN_BEVEL

Produces a diagonal corner. 


### -field XPS_LINE_JOIN_ROUND

Produces a smooth, circular arc between the lines. 


## -remarks



In the illustration that follows, the shaded area at the vertex of the line segments in each  example shows how the joint fill is determined by the value of <b>XPS_LINE_JOIN</b>.

<img alt="A diagram that shows examples of the different XPS_LINE_JOIN values" src="../images/XPS_LINE_JOIN.png"/>



## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

