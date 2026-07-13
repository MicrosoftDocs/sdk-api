---
UID: NF:dwrite_3.IDWriteFactory4.TranslateColorGlyphRun
title: IDWriteFactory4::TranslateColorGlyphRun (dwrite_3.h)
description: Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original &quot;base&quot; run.
helpviewer_keywords: ["IDWriteFactory4 interface [Direct Write]","TranslateColorGlyphRun method","IDWriteFactory4.TranslateColorGlyphRun","IDWriteFactory4::TranslateColorGlyphRun","TranslateColorGlyphRun","TranslateColorGlyphRun method [Direct Write]","TranslateColorGlyphRun method [Direct Write]","IDWriteFactory4 interface","directwrite.idwritefactory4_translatecolorglyphrun","dwrite_3/IDWriteFactory4::TranslateColorGlyphRun"]
old-location: directwrite\idwritefactory4_translatecolorglyphrun.htm
tech.root: DirectWrite
ms.assetid: D8C38635-8D7B-4C05-87D5-CCDCF31A4070
ms.date: 09/10/2025
ms.keywords: IDWriteFactory4 interface [Direct Write],TranslateColorGlyphRun method, IDWriteFactory4.TranslateColorGlyphRun, IDWriteFactory4::TranslateColorGlyphRun, TranslateColorGlyphRun, TranslateColorGlyphRun method [Direct Write], TranslateColorGlyphRun method [Direct Write],IDWriteFactory4 interface, directwrite.idwritefactory4_translatecolorglyphrun, dwrite_3/IDWriteFactory4::TranslateColorGlyphRun
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 14393
req.target-min-winversvr: Windows 10 Build 14393
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory4::TranslateColorGlyphRun
 - dwrite_3/IDWriteFactory4::TranslateColorGlyphRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFactory4.TranslateColorGlyphRun
---

# IDWriteFactory4::TranslateColorGlyphRun


## -description

Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original "base" run.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

Horizontal and vertical origin of the base glyph run in pre-transform coordinates.

### -param glyphRun [in]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a></b>

Pointer to the original "base" glyph run.

### -param glyphRunDescription [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description">DWRITE_GLYPH_RUN_DESCRIPTION</a></b>

Optional glyph run description.

### -param desiredGlyphImageFormats

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Which data formats the runs should be split into.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Measuring mode, needed to compute the origins of each glyph.

### -param worldAndDpiTransform [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a></b>

Matrix converting from the client's coordinate space to device coordinates (pixels), i.e., the world transform multiplied by any DPI scaling.

### -param colorPaletteIndex

Type: <b>UINT32</b>

Zero-based index of the color palette to use.
          Valid indices are less than the number of palettes in the font, as returned
          by <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontface2-getcolorpalettecount">IDWriteFontFace2::GetColorPaletteCount</a>.

### -param colorLayers [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1">IDWriteColorGlyphRunEnumerator1</a>**</b>

If the function succeeds, receives a pointer to an enumerator object that can be used to obtain the color glyph runs.
          If the base run has no color glyphs, then the output pointer is NULL and the method returns DWRITE_E_NOCOLOR.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns DWRITE_E_NOCOLOR if the font has no color information, the glyph run
          does not contain any color glyphs, or the specified color palette index
          is out of range. In this case, the client should render the original glyph 
          run. Otherwise, returns a standard HRESULT error code.

## -remarks

Calling <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun">IDWriteFactory2::TranslateColorGlyphRun</a> is equivalent 
        to calling <b>IDWriteFactory4::TranslateColorGlyph</b> run with the following formats specified: DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE|DWRITE_GLYPH_IMAGE_FORMATS_CFF|DWRITE_GLYPH_IMAGE_FORMATS_COLR.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4">IDWriteFactory4</a>

