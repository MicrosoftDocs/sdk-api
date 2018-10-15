---
UID: NN:d2d1_3.ID2D1Ink
title: ID2D1Ink
author: windows-sdk-content
description: Represents a single continuous stroke of variable-width ink, as defined by a series of Bezier segments and widths.
old-location: direct2d\id2d1ink.htm
tech.root: direct2d
ms.assetid: 4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID2D1Ink, ID2D1Ink interface [Direct2D], ID2D1Ink interface [Direct2D],described, d2d1_3/ID2D1Ink, direct2d.id2d1ink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Ink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Ink interface


## -description


Represents a single continuous stroke of variable-width ink, as defined by a series of Bezier segments and widths.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Ink</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1Ink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0AB546AC-F7AB-4C48-AA10-3DD2FF11B853">AddSegments</a>
</td>
<td align="left" width="63%">
Adds the given segments to the end of this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83BA2631-B3EA-4411-A5F7-265C95A00C9F">GetBounds</a>
</td>
<td align="left" width="63%">
Retrieve the bounds of the geometry, with an optional applied transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8222B527-FEEE-4456-8C0E-35437CB81DE5">GetSegmentCount</a>
</td>
<td align="left" width="63%">
Returns the number of segments in this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3B6E2823-6F66-4C2F-B8EA-94B03F19DFCD">GetSegments</a>
</td>
<td align="left" width="63%">
Retrieves the specified subset of segments stored in this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95CD771D-1B7A-4E6F-B9B2-B0565221F8F4">GetStartPoint</a>
</td>
<td align="left" width="63%">
Retrieves the starting point for this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8EA09675-971E-4399-B718-E7433D894867">RemoveSegmentsAtEnd</a>
</td>
<td align="left" width="63%">
Removes the given number of segments from the end of this ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2901735-724d-502b-bc2e-dc030f8be4fe">SetSegmentAtEnd</a>
</td>
<td align="left" width="63%">Overloaded. Updates the last segment in this ink object with new control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/930D9772-D922-4CEB-A97C-06F263543D81">SetSegments</a>
</td>
<td align="left" width="63%">
Updates the specified segments in this ink object with new control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/908bb7ce-495b-6022-5aec-f0f8e733e768">SetStartPoint</a>
</td>
<td align="left" width="63%">Overloaded. Sets the starting point for this ink object. This determines where this ink object will start rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f97d3e67-1530-14b2-1be9-7048e0dfc60f">StreamAsGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a geometric representation of this ink object.

</td>
</tr>
</table> 

