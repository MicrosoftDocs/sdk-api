---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetGlyphOrientationTransform
title: IDWriteTextAnalyzer1::GetGlyphOrientationTransform (dwrite_1.h)
description: Returns 2x3 transform matrix for the respective angle to draw the glyph run. (IDWriteTextAnalyzer1.GetGlyphOrientationTransform)
helpviewer_keywords: ["GetGlyphOrientationTransform","GetGlyphOrientationTransform method [Direct Write]","GetGlyphOrientationTransform method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","GetGlyphOrientationTransform method","IDWriteTextAnalyzer1.GetGlyphOrientationTransform","IDWriteTextAnalyzer1::GetGlyphOrientationTransform","directwrite.idwritetextanalyzer1_getglyphorientationtransform","dwrite_1/IDWriteTextAnalyzer1::GetGlyphOrientationTransform"]
old-location: directwrite\idwritetextanalyzer1_getglyphorientationtransform.htm
tech.root: DirectWrite
ms.assetid: 583AFE54-F816-4098-844B-C3F838BE46B0
ms.date: 12/05/2018
ms.keywords: GetGlyphOrientationTransform, GetGlyphOrientationTransform method [Direct Write], GetGlyphOrientationTransform method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetGlyphOrientationTransform method, IDWriteTextAnalyzer1.GetGlyphOrientationTransform, IDWriteTextAnalyzer1::GetGlyphOrientationTransform, directwrite.idwritetextanalyzer1_getglyphorientationtransform, dwrite_1/IDWriteTextAnalyzer1::GetGlyphOrientationTransform
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextAnalyzer1::GetGlyphOrientationTransform
 - dwrite_1/IDWriteTextAnalyzer1::GetGlyphOrientationTransform
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
 - IDWriteTextAnalyzer1.GetGlyphOrientationTransform
---

# IDWriteTextAnalyzer1::GetGlyphOrientationTransform


## -description

Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

## -parameters

### -param glyphOrientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a>-typed value that specifies the angle that was reported into
    <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">IDWriteTextAnalysisSink1::SetGlyphOrientation</a>.

### -param isSideways

Type: <b>BOOL</b>

Whether the run's glyphs are sideways or not.

### -param transform [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

Returned transform.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The translation component of the transform returned is zero.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>

