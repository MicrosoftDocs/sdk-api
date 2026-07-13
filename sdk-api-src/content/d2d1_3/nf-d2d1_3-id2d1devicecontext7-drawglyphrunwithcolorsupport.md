---
UID: NF:d2d1_3.ID2D1DeviceContext7.DrawGlyphRunWithColorSupport
tech.root: Direct2D
title: ID2D1DeviceContext7::DrawGlyphRunWithColorSupport
ms.date: 09/15/2023
targetos: Windows
description: Draws a glyph run, using color representations of glyphs if available in the font.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d2d1_3.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d2d1_3.h
api_name:
 - ID2D1DeviceContext7::DrawGlyphRunWithColorSupport
f1_keywords:
 - ID2D1DeviceContext7::DrawGlyphRunWithColorSupport
 - d2d1_3/ID2D1DeviceContext7::DrawGlyphRunWithColorSupport
dev_langs:
 - c++
helpviewer_keywords:
 - DrawGlyphRunWithColorSupport
---

## -description

Draws a glyph run, using color representations of glyphs if available in the font. We recommended that you render color glyphs by using this method.

## -parameters

### -param baselineOrigin

Type: **[D2D1_POINT_2F](/windows/win32/direct2d/d2d1-point-2f)**

The baseline.

### -param glyphRun

Type: \_In\_ **CONST [DWRITE_GLYPH_RUN](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

The glyph run to draw.

### -param glyphRunDescription

Type: \_In\_opt\_ **CONST [DWRITE_GLYPH_RUN_DESCRIPTION](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

A description of the glyph run to draw.

### -param foregroundBrush

Type: \_In\_opt\_ **[ID2D1Brush](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) \***

Foreground brush for the text.

### -param svgGlyphStyle

Type: \_In\_opt\_ **[ID2D1SvgGlyphStyle](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle) \***

The glyph style.

### -param colorPaletteIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font-defined color palette to use.

### -param measuringMode

Type: **[DWRITE_MEASURING_MODE](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode) = DWRITE_MEASURING_MODE_NATURAL**

Specifies measuring mode for positioning glyphs in the run.

### -param bitmapSnapOption

Type: **[D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION](/windows/win32/api/d2d1_3/ne-d2d1_3-d2d1_color_bitmap_glyph_snap_option) = D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT**

Snap options.

## -remarks

## -see-also
