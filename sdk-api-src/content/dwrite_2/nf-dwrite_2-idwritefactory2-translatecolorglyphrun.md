---
UID: NF:dwrite_2.IDWriteFactory2.TranslateColorGlyphRun
title: IDWriteFactory2::TranslateColorGlyphRun (dwrite_2.h)
description: This method is called on a glyph run to translate it in to multiple color glyph runs.
helpviewer_keywords: ["IDWriteFactory2 interface [Direct Write]","TranslateColorGlyphRun method","IDWriteFactory2.TranslateColorGlyphRun","IDWriteFactory2::TranslateColorGlyphRun","TranslateColorGlyphRun","TranslateColorGlyphRun method [Direct Write]","TranslateColorGlyphRun method [Direct Write]","IDWriteFactory2 interface","directwrite.idwritefactory2_translatecolorglyphrun","dwrite_2/IDWriteFactory2::TranslateColorGlyphRun"]
old-location: directwrite\idwritefactory2_translatecolorglyphrun.htm
tech.root: DirectWrite
ms.assetid: 1D31F807-C3F2-466F-9723-E6F12B13BFA1
ms.date: 12/05/2018
ms.keywords: IDWriteFactory2 interface [Direct Write],TranslateColorGlyphRun method, IDWriteFactory2.TranslateColorGlyphRun, IDWriteFactory2::TranslateColorGlyphRun, TranslateColorGlyphRun, TranslateColorGlyphRun method [Direct Write], TranslateColorGlyphRun method [Direct Write],IDWriteFactory2 interface, directwrite.idwritefactory2_translatecolorglyphrun, dwrite_2/IDWriteFactory2::TranslateColorGlyphRun
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory2::TranslateColorGlyphRun
 - dwrite_2/IDWriteFactory2::TranslateColorGlyphRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory2.TranslateColorGlyphRun
---

# IDWriteFactory2::TranslateColorGlyphRun


## -description

This method is called on a glyph run to translate it in to multiple color glyph runs.

## -parameters

### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal baseline origin of the original glyph run.

### -param baselineOriginY

Type: <b>FLOAT</b>

The vertical baseline origin of the original glyph run.

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

Original glyph run containing monochrome glyph IDs.

### -param glyphRunDescription [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Optional glyph run description.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Measuring mode used to compute glyph positions if the run contains color glyphs.

### -param worldToDeviceTransform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

World transform multiplied by any DPI scaling. This is needed to compute glyph positions if the run contains color glyphs and the 
            measuring mode is not <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>. 
            If this parameter is <b>NULL</b>, and identity transform is assumed.

### -param colorPaletteIndex

Type: <b>UINT32</b>

Zero-based index of the color palette to use. Valid indices are less than the number of palettes in the font, as 
            returned by <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontface2-getcolorpalettecount">IDWriteFontFace2::GetColorPaletteCount</a>.

### -param colorLayers [out]

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritecolorglyphrunenumerator">IDWriteColorGlyphRunEnumerator</a>**</b>

If the original glyph run contains color glyphs, this parameter receives a pointer to 
            an <a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritecolorglyphrunenumerator">IDWriteColorGlyphRunEnumerator</a> interface. 
            The client uses the returned interface to get information about glyph runs and associated colors to render instead of the original glyph run. 
            If the original glyph run does not contain color glyphs, this method returns <b>DWRITE_E_NOCOLOR</b> and the output pointer is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the code calls this method with a glyph run that contains no color information, the method returns <b>DWRITE_E_NOCOLOR</b> to 
          let the application know that it can just draw the original glyph run. If the glyph run contains color information, the function returns an object
          that can be enumerated through to expose runs and associated colors. The application then 
          calls <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun">DrawGlyphRun</a> with each of the returned glyph runs and foreground colors.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefactory2">IDWriteFactory2</a>

