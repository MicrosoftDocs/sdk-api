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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPaint interface


## -description


Interface describing an SVG fill or stroke value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPaint</b> interface inherits from <a href="https://msdn.microsoft.com/7B11D05C-6CD5-4609-B76A-719B92437314">ID2D1SvgAttribute</a>. <b>ID2D1SvgPaint</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/17B4A208-9658-4BD3-AFC3-33D25CD58B6F">GetColor</a>
</td>
<td align="left" width="63%">
Gets the paint color that is used if the paint type is D2D1_SVG_PAINT_TYPE_COLOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50701C5C-03F8-4DCD-A29A-2DF57846ED78">GetId</a>
</td>
<td align="left" width="63%">
Gets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/063B4258-1D96-4807-B3E4-652D5C1D2298">GetIdLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1EAF1119-BCBC-40B2-B1D6-60B72AEC79DF">GetPaintType</a>
</td>
<td align="left" width="63%">
Gets the paint type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74e1b0ac-27d3-8ca0-1b81-d29474c0f148">SetColor</a>
</td>
<td align="left" width="63%">Overloaded. Sets the paint color that is used if the paint type is D2D1_SVG_PAINT_TYPE_COLOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E9888C0D-6C71-4C41-ACD5-41BA8D6C04EE">SetId</a>
</td>
<td align="left" width="63%">
Sets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6F1D646-2ADD-4F1A-940E-8D20DFBBBAC1">SetPaintType</a>
</td>
<td align="left" width="63%">
Sets the paint type.

</td>
</tr>
</table> 

