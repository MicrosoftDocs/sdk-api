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

# GetArcDirection function


## -description


The <b>GetArcDirection</b> function retrieves the current arc direction for the specified device context. Arc and rectangle functions use the arc direction.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



The return value specifies the current arc direction; it can be any one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>AD_COUNTERCLOCKWISE</td>
<td>Arcs and rectangles are drawn counterclockwise.</td>
</tr>
<tr>
<td>AD_CLOCKWISE</td>
<td>Arcs and rectangles are drawn clockwise.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/cec31eb2-cc9d-4384-b973-dd4339b96ed0">SetArcDirection</a>
 

 

