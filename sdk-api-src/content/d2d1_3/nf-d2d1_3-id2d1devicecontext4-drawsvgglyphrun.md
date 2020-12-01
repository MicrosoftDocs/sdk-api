---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawSvgGlyphRun
title: ID2D1DeviceContext4::DrawSvgGlyphRun (d2d1_3.h)
description: Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.
helpviewer_keywords: ["DrawSvgGlyphRun","DrawSvgGlyphRun method [Direct2D]","DrawSvgGlyphRun method [Direct2D]","ID2D1DeviceContext4 interface","ID2D1DeviceContext4 interface [Direct2D]","DrawSvgGlyphRun method","ID2D1DeviceContext4.DrawSvgGlyphRun","ID2D1DeviceContext4::DrawSvgGlyphRun","d2d1_3/ID2D1DeviceContext4::DrawSvgGlyphRun","direct2d.id2d1devicecontext4_drawsvgglyphrun"]
old-location: direct2d\id2d1devicecontext4_drawsvgglyphrun.htm
tech.root: Direct2D
ms.assetid: 20E9047F-3671-4C6D-8A46-C3F77E16BC1C
ms.date: 12/05/2018
ms.keywords: DrawSvgGlyphRun, DrawSvgGlyphRun method [Direct2D], DrawSvgGlyphRun method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawSvgGlyphRun method, ID2D1DeviceContext4.DrawSvgGlyphRun, ID2D1DeviceContext4::DrawSvgGlyphRun, d2d1_3/ID2D1DeviceContext4::DrawSvgGlyphRun, direct2d.id2d1devicecontext4_drawsvgglyphrun
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext4::DrawSvgGlyphRun
 - d2d1_3/ID2D1DeviceContext4::DrawSvgGlyphRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext4.DrawSvgGlyphRun
---

# ID2D1DeviceContext4::DrawSvgGlyphRun


## -description

Draws a color glyph run that has the format of DWRITE_GLYPH_IMAGE_FORMATS_SVG.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The origin of the baseline for the glyph run.

### -param glyphRun [in]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.

### -param defaultFillBrush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the specified glyphs.

### -param svgGlyphStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>*</b>

Values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.

### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font. Note that this not the same as the paletteIndex in the
          DWRITE_COLOR_GLYPH_RUN struct, which is not relevant for SVG glyphs.

### -param measuringMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Indicates the measuring method used for text layout.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>