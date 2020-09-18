---
UID: NN:d2d1_3.ID2D1Ink
title: ID2D1Ink (d2d1_3.h)
description: Represents a single continuous stroke of variable-width ink, as defined by a series of Bezier segments and widths.
helpviewer_keywords: ["ID2D1Ink","ID2D1Ink interface [Direct2D]","ID2D1Ink interface [Direct2D]","described","d2d1_3/ID2D1Ink","direct2d.id2d1ink"]
old-location: direct2d\id2d1ink.htm
tech.root: Direct2D
ms.assetid: 4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A
ms.date: 12/05/2018
ms.keywords: ID2D1Ink, ID2D1Ink interface [Direct2D], ID2D1Ink interface [Direct2D],described, d2d1_3/ID2D1Ink, direct2d.id2d1ink
req.header: d2d1_3.h
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Ink
 - d2d1_3/ID2D1Ink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Ink
---

# ID2D1Ink interface


## -description

Represents a single continuous stroke of variable-width ink, as defined by a series of Bezier segments and widths.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Ink</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Ink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Ink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-addsegments">AddSegments</a>
</td>
<td align="left" width="63%">
Adds the given segments to the end of this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-getbounds">GetBounds</a>
</td>
<td align="left" width="63%">
Retrieve the bounds of the geometry, with an optional applied transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-getsegmentcount">GetSegmentCount</a>
</td>
<td align="left" width="63%">
Returns the number of segments in this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-getsegments">GetSegments</a>
</td>
<td align="left" width="63%">
Retrieves the specified subset of segments stored in this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-getstartpoint">GetStartPoint</a>
</td>
<td align="left" width="63%">
Retrieves the starting point for this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-removesegmentsatend">RemoveSegmentsAtEnd</a>
</td>
<td align="left" width="63%">
Removes the given number of segments from the end of this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-setsegmentatend">SetSegmentAtEnd</a>
</td>
<td align="left" width="63%">Overloaded. Updates the last segment in this ink object with new control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1ink-setsegments">SetSegments</a>
</td>
<td align="left" width="63%">
Updates the specified segments in this ink object with new control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Direct2D/id2d1ink-setstartpoint-overload">SetStartPoint</a>
</td>
<td align="left" width="63%">Overloaded. Sets the starting point for this ink object. This determines where this ink object will start rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Direct2D/id2d1ink-streamasgeometry-overload">StreamAsGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a geometric representation of this ink object.

</td>
</tr>
</table>