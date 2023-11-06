---
UID: NF:dwrite_2.IDWriteFactory2.CreateGlyphRunAnalysis
title: IDWriteFactory2::CreateGlyphRunAnalysis (dwrite_2.h)
description: Creates a glyph run analysis object, which encapsulates information used to render a glyph run. (IDWriteFactory2.CreateGlyphRunAnalysis)
helpviewer_keywords: ["CreateGlyphRunAnalysis","CreateGlyphRunAnalysis method [Direct Write]","CreateGlyphRunAnalysis method [Direct Write]","IDWriteFactory2 interface","IDWriteFactory2 interface [Direct Write]","CreateGlyphRunAnalysis method","IDWriteFactory2.CreateGlyphRunAnalysis","IDWriteFactory2::CreateGlyphRunAnalysis","directwrite.idwritefactory2_createglyphrunanalysis","dwrite_2/IDWriteFactory2::CreateGlyphRunAnalysis"]
old-location: directwrite\idwritefactory2_createglyphrunanalysis.htm
tech.root: DirectWrite
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
ms.date: 12/05/2018
ms.keywords: CreateGlyphRunAnalysis, CreateGlyphRunAnalysis method [Direct Write], CreateGlyphRunAnalysis method [Direct Write],IDWriteFactory2 interface, IDWriteFactory2 interface [Direct Write],CreateGlyphRunAnalysis method, IDWriteFactory2.CreateGlyphRunAnalysis, IDWriteFactory2::CreateGlyphRunAnalysis, directwrite.idwritefactory2_createglyphrunanalysis, dwrite_2/IDWriteFactory2::CreateGlyphRunAnalysis
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
 - IDWriteFactory2::CreateGlyphRunAnalysis
 - dwrite_2/IDWriteFactory2::CreateGlyphRunAnalysis
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
 - IDWriteFactory2.CreateGlyphRunAnalysis
---

# IDWriteFactory2::CreateGlyphRunAnalysis


## -description

Creates a glyph run analysis object, which encapsulates information used to render a glyph run.

## -parameters

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

Structure specifying the properties of the glyph run.

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

Optional transform applied to the glyphs and their positions. This transform is applied after the
          scaling specified by the emSize and pixelsPerDip.

### -param renderingMode

Type: <b>DWRITE_RENDERING_MODE</b>

Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default
          and not outline).

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Specifies the method to measure glyphs.

### -param gridFitMode

Type: <b><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode">DWRITE_GRID_FIT_MODE</a></b>

How to grid-fit glyph outlines. This must be non-default.

### -param antialiasMode

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

Specifies the antialias mode.

### -param baselineOriginX

Type: <b>FLOAT</b>

Horizontal position of the baseline origin, in DIPs.

### -param baselineOriginY

Type: <b>FLOAT</b>

Vertical position of the baseline origin, in DIPs.

### -param glyphRunAnalysis [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>**</b>

Receives a pointer to the newly created object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefactory2">IDWriteFactory2</a>

