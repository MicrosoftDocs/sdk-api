---
UID: NN:d2d1_3.ID2D1SvgGlyphStyle
title: ID2D1SvgGlyphStyle (d2d1_3.h)
author: windows-sdk-content
description: This object supplies the values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.
old-location: direct2d\id2d1svgglyphstyle.htm
tech.root: Direct2D
ms.assetid: FE01771A-D82A-4610-8014-E0C0C0C5402E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgGlyphStyle, ID2D1SvgGlyphStyle interface [Direct2D], ID2D1SvgGlyphStyle interface [Direct2D],described, d2d1_3/ID2D1SvgGlyphStyle, direct2d.id2d1svgglyphstyle
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
ms.custom: 19H1
---

# ID2D1SvgGlyphStyle interface


## -description


This object supplies the values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgGlyphStyle</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1SvgGlyphStyle</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1svgglyphstyle-getfill">GetFill</a>
</td>
<td align="left" width="63%">
Returns the requested fill parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1svgglyphstyle-getstroke">GetStroke</a>
</td>
<td align="left" width="63%">
Returns the requested stroke parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1svgglyphstyle-getstrokedashescount">GetStrokeDashesCount</a>
</td>
<td align="left" width="63%">
Returns the number of dashes in the dash array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1svgglyphstyle-setfill">SetFill</a>
</td>
<td align="left" width="63%">
Provides values to an SVG glyph for fill.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1svgglyphstyle-setstroke">SetStroke</a>
</td>
<td align="left" width="63%">
Provides values to an SVG glyph for stroke properties. The brush with opacity
        set to 1 is used as the 'context-stroke'. The opacity of the brush is used as
        the 'context-stroke-opacity' value.

</td>
</tr>
</table> 

