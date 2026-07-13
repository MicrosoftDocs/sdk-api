---
UID: NF:d2d1_3.ID2D1DeviceContext7.DrawPaintGlyphRun
tech.root: Direct2D
title: ID2D1DeviceContext7::DrawPaintGlyphRun
ms.date: 09/15/2023
targetos: Windows
description: To support COLR v1, draws a color glyph run that has the format of [DWRITE_GLYPH_IMAGE_FORMATS_COLR_PAINT_TREE](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats).
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
 - ID2D1DeviceContext7::DrawPaintGlyphRun
f1_keywords:
 - ID2D1DeviceContext7::DrawPaintGlyphRun
 - d2d1_3/ID2D1DeviceContext7::DrawPaintGlyphRun
dev_langs:
 - c++
helpviewer_keywords:
 - DrawPaintGlyphRun
---

## -description

To support COLR v1, draws a color glyph run that has the format of [DWRITE_GLYPH_IMAGE_FORMATS_COLR_PAINT_TREE](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats).

## -parameters

### -param baselineOrigin

Type: **[D2D1_POINT_2F](/windows/win32/direct2d/d2d1-point-2f)**

The baseline.

### -param glyphRun

Type: \_In\_ **CONST [DWRITE_GLYPH_RUN](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

The glyph run to draw.

### -param defaultFillBrush

Type: \_In\_opt\_ **[ID2D1Brush](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) \***

Default fill brush.

### -param colorPaletteIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The index used to select a color palette within a color font. Note that this not the same as the *paletteIndex* in the [DWRITE_COLOR_GLYPH_RUN](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_color_glyph_run) struct, which is not relevant for paint glyphs.

### -param measuringMode

Type: **[DWRITE_MEASURING_MODE](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode) = DWRITE_MEASURING_MODE_NATURAL**

Specifies measuring mode for positioning glyphs in the run.

## -remarks

## -see-also
