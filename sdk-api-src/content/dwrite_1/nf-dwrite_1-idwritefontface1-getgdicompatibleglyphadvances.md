---
UID: NF:dwrite_1.IDWriteFontFace1.GetGdiCompatibleGlyphAdvances
title: IDWriteFontFace1::GetGdiCompatibleGlyphAdvances
author: windows-sdk-content
description: Returns the pixel-aligned advances for a sequences of glyphs.
old-location: directwrite\idwritefontface1_getgdicompatibleglyphadvances.htm
tech.root: DirectWrite
ms.assetid: 187DF4C8-203E-4658-9DBF-D02988F92BBB
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetGdiCompatibleGlyphAdvances, GetGdiCompatibleGlyphAdvances method [Direct Write], GetGdiCompatibleGlyphAdvances method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetGdiCompatibleGlyphAdvances method, IDWriteFontFace1.GetGdiCompatibleGlyphAdvances, IDWriteFontFace1::GetGdiCompatibleGlyphAdvances, directwrite.idwritefontface1_getgdicompatibleglyphadvances, dwrite_1/IDWriteFontFace1::GetGdiCompatibleGlyphAdvances
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetGdiCompatibleGlyphAdvances
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace1::GetGdiCompatibleGlyphAdvances


## -description


Returns the pixel-aligned advances for a sequences of glyphs.


## -parameters




### -param emSize

Type: <b>FLOAT</b>

Logical size of the font in DIP units. A DIP
    ("device-independent pixel") equals 1/96 inch.


### -param pixelsPerDip

Type: <b>FLOAT</b>

Number of physical pixels per DIP. For
    example, if the DPI of the rendering surface is 96 this value is
    1.0f. If the DPI is 120, this value is 120.0f/96.


### -param transform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

Optional transform applied to the glyphs and
    their positions. This transform is applied after the scaling
    specified by the font size and pixelsPerDip.


### -param useGdiNatural

Type: <b>BOOL</b>

When FALSE, the metrics are the same as
    GDI aliased text (DWRITE_MEASURING_MODE_GDI_CLASSIC). When TRUE,
    the metrics are the same as those measured by GDI using a font
    using CLEARTYPE_NATURAL_QUALITY (DWRITE_MEASURING_MODE_GDI_NATURAL).


### -param isSideways

Type: <b>BOOL</b>

Retrieve the glyph's vertical advances rather
    than horizontal advances.


### -param glyphCount

Type: <b>UINT32</b>

Total glyphs to retrieve adjustments for.


### -param glyphIndices [in]

Type: <b>const UINT16*</b>

An array of glyph id's to retrieve advances.


### -param glyphAdvances [out]

Type: <b>const INT32*</b>

The returned advances in font design units for
    each glyph.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is equivalent to calling <a href="https://msdn.microsoft.com/7bda3916-6db3-4f56-b18c-288506c0b646">GetGdiCompatibleGlyphMetrics</a> and using only the advance width and height. 

Like <a href="https://msdn.microsoft.com/7bda3916-6db3-4f56-b18c-288506c0b646">GetGdiCompatibleGlyphMetrics</a>, these are in
    design units, meaning they must be scaled down by
    DWRITE_FONT_METRICS::designUnitsPerEm.




## -see-also




<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>
 

 

