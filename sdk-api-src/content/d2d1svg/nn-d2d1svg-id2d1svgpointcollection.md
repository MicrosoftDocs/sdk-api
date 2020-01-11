---
UID: NN:d2d1svg.ID2D1SvgPointCollection
title: ID2D1SvgPointCollection (d2d1svg.h)
description: Interface describing an SVG points value in a polyline or polygon element.
old-location: direct2d\id2d1svgpointcollection.htm
tech.root: Direct2D
ms.assetid: 6033F923-35E1-400F-965F-2FBED95B260A
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPointCollection, ID2D1SvgPointCollection interface [Direct2D], ID2D1SvgPointCollection interface [Direct2D],described, d2d1svg/ID2D1SvgPointCollection, direct2d.id2d1svgpointcollection
f1_keywords:
- d2d1svg/ID2D1SvgPointCollection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgPointCollection interface


## -description


Interface describing an SVG points value in a polyline or polygon element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPointCollection</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgattribute">ID2D1SvgAttribute</a>. <b>ID2D1SvgPointCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpointcollection-getpoints">GetPoints</a>
</td>
<td align="left" width="63%">
Gets points from the points array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpointcollection-getpointscount">GetPointsCount</a>
</td>
<td align="left" width="63%">
Gets the number of points in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpointcollection-removepointsatend">RemovePointsAtEnd</a>
</td>
<td align="left" width="63%">
Removes points from the end of the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpointcollection-updatepoints">UpdatePoints</a>
</td>
<td align="left" width="63%">
Updates the points array. Existing points not updated by this method are preserved. The array is resized larger if necessary to accomodate the new points.

</td>
</tr>
</table> 

