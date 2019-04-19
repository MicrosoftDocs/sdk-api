---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawSvgGlyphRun
title: ID2D1DeviceContext4::DrawSvgGlyphRun (d2d1_3.h)
author: windows-sdk-content
description: Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.
old-location: direct2d\id2d1devicecontext4_drawsvgglyphrun.htm
tech.root: Direct2D
ms.assetid: 20E9047F-3671-4C6D-8A46-C3F77E16BC1C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawSvgGlyphRun, DrawSvgGlyphRun method [Direct2D], DrawSvgGlyphRun method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawSvgGlyphRun method, ID2D1DeviceContext4.DrawSvgGlyphRun, ID2D1DeviceContext4::DrawSvgGlyphRun, d2d1_3/ID2D1DeviceContext4::DrawSvgGlyphRun, direct2d.id2d1devicecontext4_drawsvgglyphrun
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
 - ID2D1DeviceContext4.DrawSvgGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext4::DrawSvgGlyphRun


## -description


Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.


## -parameters




### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The origin of the baseline for the glyph run.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.


### -param defaultFillBrush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the specified glyphs.


### -param svgGlyphStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/FE01771A-D82A-4610-8014-E0C0C0C5402E">ID2D1SvgGlyphStyle</a>*</b>

Values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font. Note that this not the same as the paletteIndex in the
          DWRITE_COLOR_GLYPH_RUN struct, which is not relevant for SVG glyphs.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

Indicates the measuring method used for text layout.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>
 

 

