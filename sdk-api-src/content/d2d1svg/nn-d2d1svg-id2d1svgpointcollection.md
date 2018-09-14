---
UID: NN:d2d1svg.ID2D1SvgPointCollection
title: ID2D1SvgPointCollection
author: windows-sdk-content
description: Interface describing an SVG points value in a polyline or polygon element.
old-location: direct2d\id2d1svgpointcollection.htm
tech.root: Direct2D
ms.assetid: 6033F923-35E1-400F-965F-2FBED95B260A
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1SvgPointCollection, ID2D1SvgPointCollection interface [Direct2D], ID2D1SvgPointCollection interface [Direct2D],described, d2d1svg/ID2D1SvgPointCollection, direct2d.id2d1svgpointcollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPointCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPointCollection interface


## -description


Interface describing an SVG points value in a polyline or polygon element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPointCollection</b> interface inherits from <a href="https://msdn.microsoft.com/7B11D05C-6CD5-4609-B76A-719B92437314">ID2D1SvgAttribute</a>. <b>ID2D1SvgPointCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgPointCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/886039FB-0640-4B20-84E2-4B3EC2AFA234">GetPoints</a>
</td>
<td align="left" width="63%">
Gets points from the points array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57D125F0-F2CF-411C-93DA-13E13234E13E">GetPointsCount</a>
</td>
<td align="left" width="63%">
Gets the number of points in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F15DAC71-647D-466C-B754-6553122EC5A7">RemovePointsAtEnd</a>
</td>
<td align="left" width="63%">
Removes points from the end of the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1DE682E-FFB1-4090-BE2A-FED41C1E7170">UpdatePoints</a>
</td>
<td align="left" width="63%">
Updates the points array. Existing points not updated by this method are preserved. The array is resized larger if necessary to accomodate the new points.

</td>
</tr>
</table> 

