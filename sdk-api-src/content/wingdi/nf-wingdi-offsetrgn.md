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

# OffsetRgn function


## -description


The <b>OffsetRgn</b> function moves a region by the specified offsets.


## -parameters




### -param hrgn [in]

Handle to the region to be moved.


### -param x

TBD


### -param y

TBD




#### - nXOffset [in]

Specifies the number of logical units to move left or right.


#### - nYOffset [in]

Specifies the number of logical units to move up or down.


## -returns



The return value specifies the new region's complexity. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region is a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>An error occurred; region is unaffected.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

