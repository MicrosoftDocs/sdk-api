---
UID: NN:dwrite_1.IDWriteFontFace1
title: IDWriteFontFace1 (dwrite_1.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face.
old-location: directwrite\idwritefontface1.htm
tech.root: DirectWrite
ms.assetid: 1DB7156F-0578-46A0-8C96-E1E34FF4E49E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace1, IDWriteFontFace1 interface [Direct Write], IDWriteFontFace1 interface [Direct Write],described, directwrite.idwritefontface1, dwrite_1/IDWriteFontFace1
ms.topic: interface
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteFontFace1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace1 interface


## -description


Represents an absolute reference to a font face.  

This interface contains the font face type, appropriate file references, and face identification data.  

You obtain various font data like metrics, names, and glyph outlines from the <b>IDWriteFontFace1</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>. <b>IDWriteFontFace1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics">GetCaretMetrics</a>
</td>
<td align="left" width="63%">
Gets caret metrics for the font in design units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getdesignglyphadvances">GetDesignGlyphAdvances</a>
</td>
<td align="left" width="63%">
Retrieves the advances in design units for a sequences of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getgdicompatibleglyphadvances">GetGdiCompatibleGlyphAdvances</a>
</td>
<td align="left" width="63%">
Returns the pixel-aligned advances for a sequences of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getgdicompatiblemetrics">GetGdiCompatibleMetrics</a>
</td>
<td align="left" width="63%">
Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments">GetKerningPairAdjustments</a>
</td>
<td align="left" width="63%">
Retrieves the kerning pair adjustments from the font's kern table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getrecommendedrenderingmode">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getunicoderanges">GetUnicodeRanges</a>
</td>
<td align="left" width="63%">
Retrieves a list of character ranges supported by a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants">GetVerticalGlyphVariants</a>
</td>
<td align="left" width="63%">
Retrieves the vertical forms of the nominal glyphs retrieved from
    GetGlyphIndices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs">HasKerningPairs</a>
</td>
<td align="left" width="63%">
Determines whether the font supports pair-kerning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-hasverticalglyphvariants">HasVerticalGlyphVariants</a>
</td>
<td align="left" width="63%">
Determines whether the font has any vertical glyph variants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-ismonospacedfont">IsMonospacedFont</a>
</td>
<td align="left" width="63%">
Determines whether the font of a text range is monospaced, that is, the font characters are the
    same fixed-pitch width.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>
 

 

