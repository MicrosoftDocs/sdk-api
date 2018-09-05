---
UID: NF:msinkaut.IInkOverlay.HitTestSelection
title: IInkOverlay::HitTestSelection
author: windows-sdk-content
description: Determines what portion of the selection was hit during a hit test.
old-location: tablet\inkoverlay_hittestselection.htm
old-project: tablet
ms.assetid: 289589fa-84da-40b3-b60e-551ef0114279
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 289589fa-84da-40b3-b60e-551ef0114279, HitTestSelection, HitTestSelection method [Tablet PC], HitTestSelection method [Tablet PC],IInkOverlay interface, IInkOverlay, IInkOverlay interface [Tablet PC],HitTestSelection method, IInkOverlay.HitTestSelection, IInkOverlay::HitTestSelection, msinkaut/IInkOverlay::HitTestSelection, tablet.inkoverlay_hittestselection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.HitTestSelection
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult Enumeration</a>
 

 

