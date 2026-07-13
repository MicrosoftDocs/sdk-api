---
UID: NF:dwrite_3.IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUNconst,D2D1_POINT_2F,D2D1_POINT_2F)
title: IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F) (dwrite_3.h)
description: Converts glyph run placements to glyph origins. (overload 2/2)
helpviewer_keywords: ["ComputeGlyphOrigins","ComputeGlyphOrigins method [Direct Write]","ComputeGlyphOrigins method [Direct Write]","IDWriteFactory4 interface","IDWriteFactory4 interface [Direct Write]","ComputeGlyphOrigins method","IDWriteFactory4.ComputeGlyphOrigins","IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const","D2D1_POINT_2F","D2D1_POINT_2F)","IDWriteFactory4::ComputeGlyphOrigins","IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const","D2D1_POINT_2F","D2D1_POINT_2F)","directwrite.idwritefactory4_computeglyphorigins","dwrite_3/IDWriteFactory4::ComputeGlyphOrigins"]
old-location: directwrite\idwritefactory4_computeglyphorigins.htm
tech.root: DirectWrite
ms.assetid: 0AA609E2-28C3-4D0C-A627-0648FB0D126A
ms.date: 09/10/2025
ms.keywords: ComputeGlyphOrigins, ComputeGlyphOrigins method [Direct Write], ComputeGlyphOrigins method [Direct Write],IDWriteFactory4 interface, IDWriteFactory4 interface [Direct Write],ComputeGlyphOrigins method, IDWriteFactory4.ComputeGlyphOrigins, IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F), IDWriteFactory4::ComputeGlyphOrigins, IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F), directwrite.idwritefactory4_computeglyphorigins, dwrite_3/IDWriteFactory4::ComputeGlyphOrigins
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
 - IDWriteFactory4::ComputeGlyphOrigins
 - dwrite_3/IDWriteFactory4::ComputeGlyphOrigins
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
 - IDWriteFactory4.ComputeGlyphOrigins
---

## -description

Converts glyph run placements to glyph origins.

## -parameters

### -param glyphRun

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a></b>

Structure containing the properties of the glyph run.

### -param baselineOrigin

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.

### -param glyphOrigins

Type: [out] <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

On return contains the glyph origins for the glyphrun.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

The transform and DPI have no effect on the origin scaling. They are solely used to compute glyph advances when not supplied and align glyphs in pixel aligned measuring modes.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4">IDWriteFactory4</a>
