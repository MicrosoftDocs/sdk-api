---
UID: NN:d2d1svg.ID2D1SvgPaint
title: ID2D1SvgPaint (d2d1svg.h)
author: windows-sdk-content
description: Interface describing an SVG fill or stroke value.
old-location: direct2d\id2d1svgpaint.htm
tech.root: Direct2D
ms.assetid: 80FE02F1-D83B-4AA1-94F1-B754106CB19D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPaint, ID2D1SvgPaint interface [Direct2D], ID2D1SvgPaint interface [Direct2D],described, d2d1svg/ID2D1SvgPaint, direct2d.id2d1svgpaint
ms.topic: interface
f1_keywords: 
 - "d2d1svg/ID2D1SvgPaint"
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
 - ID2D1SvgPaint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgPaint interface


## -description


Interface describing an SVG fill or stroke value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPaint</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgattribute">ID2D1SvgAttribute</a>. <b>ID2D1SvgPaint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgPaint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-getcolor">GetColor</a>
</td>
<td align="left" width="63%">
Gets the paint color that is used if the paint type is D2D1_SVG_PAINT_TYPE_COLOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-getidlength">GetIdLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-getpainttype">GetPaintType</a>
</td>
<td align="left" width="63%">
Gets the paint type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1svgpaint-setcolor-overload">SetColor</a>
</td>
<td align="left" width="63%">Overloaded. Sets the paint color that is used if the paint type is D2D1_SVG_PAINT_TYPE_COLOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-setid">SetId</a>
</td>
<td align="left" width="63%">
Sets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpaint-setpainttype">SetPaintType</a>
</td>
<td align="left" width="63%">
Sets the paint type.

</td>
</tr>
</table> 

