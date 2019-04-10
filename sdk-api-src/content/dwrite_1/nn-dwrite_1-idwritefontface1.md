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
---

# IDWriteFontFace1 interface


## -description


Represents an absolute reference to a font face.  

This interface contains the font face type, appropriate file references, and face identification data.  

You obtain various font data like metrics, names, and glyph outlines from the <b>IDWriteFontFace1</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace1</b> interface inherits from <a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>. <b>IDWriteFontFace1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D9006617-A5B5-4575-9C00-26F52A73DC0D">GetCaretMetrics</a>
</td>
<td align="left" width="63%">
Gets caret metrics for the font in design units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E40518F-51E0-48F6-99ED-BE9407B61B6E">GetDesignGlyphAdvances</a>
</td>
<td align="left" width="63%">
Retrieves the advances in design units for a sequences of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/187DF4C8-203E-4658-9DBF-D02988F92BBB">GetGdiCompatibleGlyphAdvances</a>
</td>
<td align="left" width="63%">
Returns the pixel-aligned advances for a sequences of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FD26970-8CF3-453F-A08D-30CC4A820281">GetGdiCompatibleMetrics</a>
</td>
<td align="left" width="63%">
Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA837B04-85BC-4A3B-A6FE-24D5AFD21B14">GetKerningPairAdjustments</a>
</td>
<td align="left" width="63%">
Retrieves the kerning pair adjustments from the font's kern table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F899D56-F56B-4C4C-A17D-B42A34CAA0F1">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4726A5FC-6481-4986-AE2D-EBC044D0B9C6">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0464BA91-B098-463D-A4A9-8D3C05E45F0E">GetUnicodeRanges</a>
</td>
<td align="left" width="63%">
Retrieves a list of character ranges supported by a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91CD924E-A664-45C6-B787-61129C31501B">GetVerticalGlyphVariants</a>
</td>
<td align="left" width="63%">
Retrieves the vertical forms of the nominal glyphs retrieved from
    GetGlyphIndices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/701B874A-BA95-43CA-8762-70BA571FDC10">HasKerningPairs</a>
</td>
<td align="left" width="63%">
Determines whether the font supports pair-kerning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/694F003E-4189-4DC6-ADC8-B94EE8C624BE">HasVerticalGlyphVariants</a>
</td>
<td align="left" width="63%">
Determines whether the font has any vertical glyph variants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A83F330-FADA-4307-BCCE-DDCCF5D1D429">IsMonospacedFont</a>
</td>
<td align="left" width="63%">
Determines whether the font of a text range is monospaced, that is, the font characters are the
    same fixed-pitch width.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>
 

 

