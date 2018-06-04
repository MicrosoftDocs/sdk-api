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

# SetArcDirection function


## -description


The <b>SetArcDirection</b> sets the drawing direction to be used for arc and rectangle functions.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param dir

TBD




#### - ArcDirection [in]

The new arc direction. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AD_COUNTERCLOCKWISE"></a><a id="ad_counterclockwise"></a><dl>
<dt><b>AD_COUNTERCLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn counterclockwise.

</td>
</tr>
<tr>
<td width="40%"><a id="AD_CLOCKWISE"></a><a id="ad_clockwise"></a><dl>
<dt><b>AD_CLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn clockwise.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value specifies the old arc direction.

If the function fails, the return value is zero.




## -remarks



The default direction is counterclockwise.

The <b>SetArcDirection</b> function specifies the direction in which the following functions draw:

<ul>
<li>
<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">Arc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">ArcTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d6752c47-96a5-4fac-a1bb-0611a91f03f9">Chord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5">Ellipse</a>
</li>
<li>
<a href="https://msdn.microsoft.com/86daa936-b483-4432-aa32-0b9328ff76f9">Pie</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed6b9824-1edc-4510-b9da-a4287845aa83">Rectangle</a>
</li>
<li>
<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">RoundRect</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>
 

 

