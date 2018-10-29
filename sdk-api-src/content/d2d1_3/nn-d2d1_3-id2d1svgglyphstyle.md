---
UID: NN:d2d1_3.ID2D1SvgGlyphStyle
title: ID2D1SvgGlyphStyle
author: windows-sdk-content
description: This object supplies the values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.
old-location: direct2d\id2d1svgglyphstyle.htm
tech.root: Direct2D
ms.assetid: FE01771A-D82A-4610-8014-E0C0C0C5402E
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1SvgGlyphStyle, ID2D1SvgGlyphStyle interface [Direct2D], ID2D1SvgGlyphStyle interface [Direct2D],described, d2d1_3/ID2D1SvgGlyphStyle, direct2d.id2d1svgglyphstyle
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SvgGlyphStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgGlyphStyle interface


## -description


This object supplies the values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgGlyphStyle</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1SvgGlyphStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgGlyphStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F57178E-87F7-43C7-9DCD-643E1A6B3B4D">GetFill</a>
</td>
<td align="left" width="63%">
Returns the requested fill parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5EC78516-E0E2-4758-9C36-47F951D1BCAE">GetStroke</a>
</td>
<td align="left" width="63%">
Returns the requested stroke parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99CCB20B-B7E2-4D53-BB0C-A1996874F0B2">GetStrokeDashesCount</a>
</td>
<td align="left" width="63%">
Returns the number of dashes in the dash array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F8D423C-6A3A-4240-87E9-515F5FE29C1D">SetFill</a>
</td>
<td align="left" width="63%">
Provides values to an SVG glyph for fill.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C7734DF-3EA6-43A8-8913-8D174ABAAA56">SetStroke</a>
</td>
<td align="left" width="63%">
Provides values to an SVG glyph for stroke properties. The brush with opacity
        set to 1 is used as the 'context-stroke'. The opacity of the brush is used as
        the 'context-stroke-opacity' value.

</td>
</tr>
</table> 

