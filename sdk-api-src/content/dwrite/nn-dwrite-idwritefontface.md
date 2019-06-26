---
UID: NN:dwrite.IDWriteFontFace
title: IDWriteFontFace (dwrite.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face which contains font face type, appropriate file references, face identification data and various font data such as metrics, names and glyph outlines.
old-location: directwrite\IDWriteFontFace.htm
tech.root: DirectWrite
ms.assetid: 1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace, IDWriteFontFace interface [Direct Write], IDWriteFontFace interface [Direct Write],described, directwrite.IDWriteFontFace, dwrite/IDWriteFontFace
ms.topic: interface
f1_keywords: 
 - "dwrite/IDWriteFontFace"
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace interface


## -description


Represents an absolute reference to a font face which contains font face type, appropriate file references,  face identification data and various font data such as metrics, names and glyph outlines. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics">GetDesignGlyphMetrics</a>
</td>
<td align="left" width="63%">
 Obtains ideal (resolution-independent) glyph metrics in font design units. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getfiles">GetFiles</a>
</td>
<td align="left" width="63%">
 Obtains the font files representing a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritefontface-getgdicompatibleglyphmetrics">GetGdiCompatibleGlyphMetrics</a>
</td>
<td align="left" width="63%">
Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritefontface-getgdicompatiblemetrics">GetGdiCompatibleMetrics</a>
</td>
<td align="left" width="63%">
Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getglyphcount">GetGlyphCount</a>
</td>
<td align="left" width="63%">
 Obtains the number of glyphs in the font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getglyphindices">GetGlyphIndices</a>
</td>
<td align="left" width="63%">
 Returns the nominal mapping of UCS4 Unicode code points to glyph indices as defined by the font 'CMAP' table.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline">GetGlyphRunOutline</a>
</td>
<td align="left" width="63%">
 Computes the outline of a run of glyphs by calling back to the outline sink interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getindex">GetIndex</a>
</td>
<td align="left" width="63%">
 Obtains the index of a font face in the context of its font files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getsimulations">GetSimulations</a>
</td>
<td align="left" width="63%">
 Obtains the algorithmic style simulation flags of a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-gettype">GetType</a>
</td>
<td align="left" width="63%">
 Obtains the file format type of a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-issymbolfont">IsSymbolFont</a>
</td>
<td align="left" width="63%">
 Determines whether the font is a symbol font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-releasefonttable">ReleaseFontTable</a>
</td>
<td align="left" width="63%">
 Releases the table obtained earlier from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-trygetfonttable">TryGetFontTable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-trygetfonttable">TryGetFontTable</a>
</td>
<td align="left" width="63%">
 Finds the specified OpenType font table if it exists and returns a pointer to it.
     The function accesses the underlying font data through the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a> interface
     implemented by the font file loader.

</td>
</tr>
</table> 

