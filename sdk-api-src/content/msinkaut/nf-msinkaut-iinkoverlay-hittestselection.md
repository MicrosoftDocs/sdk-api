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

# IInkOverlay::HitTestSelection


## -description



Determines what portion of the selection was hit during a hit test.




## -parameters




### -param x [in]

The x-position, in pixels, of the hit test.


### -param y [in]

The y-position, in pixels, of the hit test.


### -param SelArea [out]

The value from the <a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult</a> enumeration,which specifies which part of a selection, if any, was hit during a hit test.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>East</b></dt>
</dl>
</td>
<td width="60%">
 The east side sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>None</b></dt>
</dl>
</td>
<td width="60%">
 No part of the selection was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>North</b></dt>
</dl>
</td>
<td width="60%">
The north side sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Northeast</b></dt>
</dl>
</td>
<td width="60%">
The northeast corner sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Northwest</b></dt>
</dl>
</td>
<td width="60%">
The northwest corner sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Selection</b></dt>
</dl>
</td>
<td width="60%">
 The selection itself was hit (no selection handle was hit).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>South</b></dt>
</dl>
</td>
<td width="60%">
The south side sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Southeast</b></dt>
</dl>
</td>
<td width="60%">
The southeast corner sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Southwest</b></dt>
</dl>
</td>
<td width="60%">
The southwest corner sizing handle was hit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>West</b></dt>
</dl>
</td>
<td width="60%">
The west side sizing handle was hit.

</td>
</tr>
</table>
 




## -see-also




<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult Enumeration</a>
 

 

