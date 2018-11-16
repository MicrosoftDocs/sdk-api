---
UID: NN:d2d1_3.ID2D1DeviceContext4
title: ID2D1DeviceContext4
author: windows-sdk-content
description: This interface performs all the same functions as the ID2D1DeviceContext3 interface, plus it enables functionality for handling new types of color font glyphs.
old-location: direct2d\id2d1devicecontext4.htm
tech.root: Direct2D
ms.assetid: 59E1F73B-BAD9-4826-BF5B-435E760CC546
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1DeviceContext4, ID2D1DeviceContext4 interface [Direct2D], ID2D1DeviceContext4 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext4, direct2d.id2d1devicecontext4
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext4 interface


## -description


This interface performs all the same functions as the <a href="https://msdn.microsoft.com/AD763619-7880-41EB-8446-2E4B84CB4EAC">ID2D1DeviceContext3</a> interface,
          plus it enables functionality for handling new types of color font glyphs.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext4</b> interface inherits from <a href="https://msdn.microsoft.com/AD763619-7880-41EB-8446-2E4B84CB4EAC">ID2D1DeviceContext3</a>. <b>ID2D1DeviceContext4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/56E357D3-D361-4A56-990F-1CD4051BD4F1">CreateSvgGlyphStyle</a>
</td>
<td align="left" width="63%">
Creates an SVG glyph style object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E3DDC924-87A1-43C7-8FC7-3C4E3FC2AC59">DrawColorBitmapGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a color bitmap glyph run using one of the bitmap formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20E9047F-3671-4C6D-8A46-C3F77E16BC1C">DrawSvgGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7833da99-e4c3-b3c2-7a53-c95b8f0fa2c9">DrawText</a>
</td>
<td align="left" width="63%">Overloaded. Draws the text within the given layout rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54993EFD-A649-4613-8A9C-744FE22F7BFC">DrawTextLayout</a>
</td>
<td align="left" width="63%">
Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/493224CD-A31E-405B-A084-24C377F713A0">GetColorBitmapGlyphImage</a>
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
<a href="https://msdn.microsoft.com/096ED0A3-6222-4DC4-9463-E90D36F2442A">GetSvgGlyphImage</a>
</td>
<td align="left" width="63%">
Retrieves an image of the SVG glyph from the color glyph cache. If the cache  does not already contain the requested resource, it will be created.
          This method may be used to extend the lifetime of a glyph image even after it is evicted from the color glyph cache.
        

</td>
</tr>
</table> 

