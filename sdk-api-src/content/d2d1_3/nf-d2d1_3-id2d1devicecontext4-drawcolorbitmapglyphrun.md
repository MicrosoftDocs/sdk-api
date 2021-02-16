---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawColorBitmapGlyphRun
title: ID2D1DeviceContext4::DrawColorBitmapGlyphRun (d2d1_3.h)
description: Draws a color bitmap glyph run using one of the bitmap formats.
helpviewer_keywords: ["DrawColorBitmapGlyphRun","DrawColorBitmapGlyphRun method [Direct2D]","DrawColorBitmapGlyphRun method [Direct2D]","ID2D1DeviceContext4 interface","ID2D1DeviceContext4 interface [Direct2D]","DrawColorBitmapGlyphRun method","ID2D1DeviceContext4.DrawColorBitmapGlyphRun","ID2D1DeviceContext4::DrawColorBitmapGlyphRun","d2d1_3/ID2D1DeviceContext4::DrawColorBitmapGlyphRun","direct2d.id2d1devicecontext4_drawcolorbitmapglyphrun"]
old-location: direct2d\id2d1devicecontext4_drawcolorbitmapglyphrun.htm
tech.root: Direct2D
ms.assetid: E3DDC924-87A1-43C7-8FC7-3C4E3FC2AC59
ms.date: 12/05/2018
ms.keywords: DrawColorBitmapGlyphRun, DrawColorBitmapGlyphRun method [Direct2D], DrawColorBitmapGlyphRun method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawColorBitmapGlyphRun method, ID2D1DeviceContext4.DrawColorBitmapGlyphRun, ID2D1DeviceContext4::DrawColorBitmapGlyphRun, d2d1_3/ID2D1DeviceContext4::DrawColorBitmapGlyphRun, direct2d.id2d1devicecontext4_drawcolorbitmapglyphrun
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
 - ID2D1DeviceContext4::DrawColorBitmapGlyphRun
 - d2d1_3/ID2D1DeviceContext4::DrawColorBitmapGlyphRun
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
 - ID2D1DeviceContext4.DrawColorBitmapGlyphRun
---

# ID2D1DeviceContext4::DrawColorBitmapGlyphRun


## -description

Draws a color bitmap glyph run using one of the bitmap formats.

## -parameters

### -param glyphImageFormat

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Specifies the format of the glyph image. Supported formats are DWRITE_GLYPH_IMAGE_FORMATS_PNG, DWRITE_GLYPH_IMAGE_FORMATS_JPEG,
          DWRITE_GLYPH_IMAGE_FORMATS_TIFF, or DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8.  This method will result in an error if the color glyph run does not contain the requested format.
          

Only one format can be specified at a time, combinations of flags are not valid input.

### -param baselineOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The origin of the baseline for the glyph run.

### -param glyphRun [in]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.

### -param measuringMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Indicates the measuring method.

### -param bitmapSnapOption

Type: <b><a href="/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_color_bitmap_glyph_snap_option">D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION</a></b>

Specifies the pixel snapping policy when rendering color bitmap glyphs.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>