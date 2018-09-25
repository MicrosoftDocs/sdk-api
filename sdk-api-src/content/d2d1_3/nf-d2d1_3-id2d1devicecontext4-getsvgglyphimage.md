---
UID: NF:d2d1_3.ID2D1DeviceContext4.GetSvgGlyphImage
title: ID2D1DeviceContext4::GetSvgGlyphImage
author: windows-sdk-content
description: Retrieves an image of the SVG glyph from the color glyph cache.
old-location: direct2d\id2d1devicecontext4_getsvgglyphimage.htm
tech.root: direct2d
ms.assetid: 096ED0A3-6222-4DC4-9463-E90D36F2442A
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetSvgGlyphImage, GetSvgGlyphImage method [Direct2D], GetSvgGlyphImage method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],GetSvgGlyphImage method, ID2D1DeviceContext4.GetSvgGlyphImage, ID2D1DeviceContext4::GetSvgGlyphImage, d2d1_3/ID2D1DeviceContext4::GetSvgGlyphImage, direct2d.id2d1devicecontext4_getsvgglyphimage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID2D1DeviceContext4.GetSvgGlyphImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext4::GetSvgGlyphImage


## -description


Retrieves an image of the SVG glyph from the color glyph cache. If the cache  does not already contain the requested resource, it will be created.
          This method may be used to extend the lifetime of a glyph image even after it is evicted from the color glyph cache.
        


## -parameters




### -param glyphOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

Origin of the glyph.


### -param fontFace [in]

Type: <b><a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>*</b>

Reference to a font face which contains font face type, appropriate file references, face identification data and various font data such as metrics, names and glyph outlines.


### -param fontEmSize

Type: <b>FLOAT</b>

The specified font size affects the output
          glyphTransform, causing it to properly scale the glyph.


### -param glyphIndex

Type: <b>UINT16</b>

Index of the glyph to retrieve.


### -param isSideways

Type: <b>BOOL</b>

If true, specifies that glyphs are rotated 90 degrees to the left and vertical metrics are used. Vertical writing is achieved by specifying isSideways as true and rotating the entire run 90 degrees to the right via a rotate transform.


### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the image.


### -param defaultFillBrush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

Describes how the area is painted.


### -param svgGlyphStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/FE01771A-D82A-4610-8014-E0C0C0C5402E">ID2D1SvgGlyphStyle</a>*</b>

The values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font. 
          Note that this not the same as the paletteIndex in the DWRITE_COLOR_GLYPH_RUN struct, which is not relevant for SVG glyphs.


### -param glyphTransform [out]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

Output transform, which transforms from the glyph's space to the same output space as the worldTransform. 
          This includes the input glyphOrigin, the glyph's offset from the glyphOrigin, and any other required transformations.


### -param glyphImage [out]

Type: <b><a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a>**</b>

On completion, contains the retrieved glyph image.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>
 

 

