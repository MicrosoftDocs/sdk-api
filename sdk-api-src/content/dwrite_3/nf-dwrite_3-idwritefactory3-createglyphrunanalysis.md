---
UID: NF:dwrite_3.IDWriteFactory3.CreateGlyphRunAnalysis
title: IDWriteFactory3::CreateGlyphRunAnalysis (dwrite_3.h)
description: Creates a glyph-run-analysis object that encapsulates info that DirectWrite uses to render a glyph run.
helpviewer_keywords: ["CreateGlyphRunAnalysis","CreateGlyphRunAnalysis method [Direct Write]","CreateGlyphRunAnalysis method [Direct Write]","IDWriteFactory3 interface","IDWriteFactory3 interface [Direct Write]","CreateGlyphRunAnalysis method","IDWriteFactory3.CreateGlyphRunAnalysis","IDWriteFactory3::CreateGlyphRunAnalysis","directwrite.idwritefactory3_createglyphrunanalysis","dwrite_3/IDWriteFactory3::CreateGlyphRunAnalysis"]
old-location: directwrite\idwritefactory3_createglyphrunanalysis.htm
tech.root: DirectWrite
ms.assetid: 5BF8BA9C-F07F-43F0-B712-71220E6535A5
ms.date: 09/10/2025
ms.keywords: CreateGlyphRunAnalysis, CreateGlyphRunAnalysis method [Direct Write], CreateGlyphRunAnalysis method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateGlyphRunAnalysis method, IDWriteFactory3.CreateGlyphRunAnalysis, IDWriteFactory3::CreateGlyphRunAnalysis, directwrite.idwritefactory3_createglyphrunanalysis, dwrite_3/IDWriteFactory3::CreateGlyphRunAnalysis
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFactory3::CreateGlyphRunAnalysis
 - dwrite_3/IDWriteFactory3::CreateGlyphRunAnalysis
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
 - IDWriteFactory3.CreateGlyphRunAnalysis
---

# IDWriteFactory3::CreateGlyphRunAnalysis


## -description

Creates a glyph-run-analysis object that encapsulates info that <a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> uses to render a glyph run.

## -parameters

### -param glyphRun [in]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a></b>

A <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a> structure that contains the properties of the glyph run.

### -param transform [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a></b>

A <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a> structure that describes the optional transform to be applied to glyphs and their positions.

### -param renderingMode

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1">DWRITE_RENDERING_MODE1</a></b>

A <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1">DWRITE_RENDERING_MODE1</a>-typed value that specifies the rendering mode, which must be one of the raster rendering modes (that is, not default and not outline).

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

A <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a>-typed value that specifies the measuring method for glyphs in the run. This method uses this value with the other properties to determine the rendering mode.

### -param gridFitMode

Type: <b><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode">DWRITE_GRID_FIT_MODE</a></b>

A <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode">DWRITE_GRID_FIT_MODE</a>-typed value that specifies how to grid-fit glyph outlines. This value must be non-default.

### -param antialiasMode

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE</a>-typed value that specifies the type of antialiasing to use for text when the rendering mode calls for antialiasing.

### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.

### -param baselineOriginY

Type: <b>FLOAT</b>

The vertical position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.

### -param glyphRunAnalysis [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a> interface for the newly created glyph-run-analysis object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>

