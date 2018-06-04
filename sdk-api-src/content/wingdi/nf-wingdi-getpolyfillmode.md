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

# GetPolyFillMode function


## -description


The <b>GetPolyFillMode</b> function retrieves the current polygon fill mode.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value specifies the polygon fill mode, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ALTERNATE</td>
<td>Selects alternate mode (fills area between odd-numbered and even-numbered polygon sides on each scan line).</td>
</tr>
<tr>
<td>WINDING</td>
<td>Selects winding mode (fills any region with a nonzero winding value).</td>
</tr>
</table>
 

If an error occurs, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>
 

 

