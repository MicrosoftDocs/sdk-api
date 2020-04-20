---
UID: NN:d2d1_3.ID2D1DeviceContext4
title: ID2D1DeviceContext4 (d2d1_3.h)
description: This interface performs all the same functions as the ID2D1DeviceContext3 interface, plus it enables functionality for handling new types of color font glyphs.helpviewer_keywords: ["ID2D1DeviceContext4","ID2D1DeviceContext4 interface [Direct2D]","ID2D1DeviceContext4 interface [Direct2D]","described","d2d1_3/ID2D1DeviceContext4","direct2d.id2d1devicecontext4"]
old-location: direct2d\id2d1devicecontext4.htm
tech.root: Direct2D
ms.assetid: 59E1F73B-BAD9-4826-BF5B-435E760CC546
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext4, ID2D1DeviceContext4 interface [Direct2D], ID2D1DeviceContext4 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext4, direct2d.id2d1devicecontext4
f1_keywords:
- d2d1_3/ID2D1DeviceContext4
dev_langs:
- c++
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
- ID2D1DeviceContext4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext4 interface


## -description


This interface performs all the same functions as the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext3">ID2D1DeviceContext3</a> interface,
          plus it enables functionality for handling new types of color font glyphs.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext3">ID2D1DeviceContext3</a>. <b>ID2D1DeviceContext4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-createsvgglyphstyle">CreateSvgGlyphStyle</a>
</td>
<td align="left" width="63%">
Creates an SVG glyph style object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun">DrawColorBitmapGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a color bitmap glyph run using one of the bitmap formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun">DrawSvgGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext4-drawtext-overload">DrawText</a>
</td>
<td align="left" width="63%">Overloaded. Draws the text within the given layout rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout">DrawTextLayout</a>
</td>
<td align="left" width="63%">
Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-getcolorbitmapglyphimage">GetColorBitmapGlyphImage</a>
</td>
<td align="left" width="63%">
Retrieves an image of the color bitmap glyph from the color glyph cache. If the
          cache does not already contain the requested resource, it will be created. This
          method may be used to extend the lifetime of a glyph image even after it is
          evicted from the color glyph cache.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-getsvgglyphimage">GetSvgGlyphImage</a>
</td>
<td align="left" width="63%">
Retrieves an image of the SVG glyph from the color glyph cache. If the cache  does not already contain the requested resource, it will be created.
          This method may be used to extend the lifetime of a glyph image even after it is evicted from the color glyph cache.
        

</td>
</tr>
</table> 

