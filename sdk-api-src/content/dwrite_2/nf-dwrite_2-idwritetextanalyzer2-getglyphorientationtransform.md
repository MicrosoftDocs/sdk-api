---
UID: NF:dwrite_2.IDWriteTextAnalyzer2.GetGlyphOrientationTransform
title: IDWriteTextAnalyzer2::GetGlyphOrientationTransform (dwrite_2.h)
description: Returns 2x3 transform matrix for the respective angle to draw the glyph run. (IDWriteTextAnalyzer2.GetGlyphOrientationTransform)
helpviewer_keywords: ["GetGlyphOrientationTransform","GetGlyphOrientationTransform method [Direct Write]","GetGlyphOrientationTransform method [Direct Write]","IDWriteTextAnalyzer2 interface","IDWriteTextAnalyzer2 interface [Direct Write]","GetGlyphOrientationTransform method","IDWriteTextAnalyzer2.GetGlyphOrientationTransform","IDWriteTextAnalyzer2::GetGlyphOrientationTransform","directwrite.idwritetextanalyzer2_getglyphorientationtransform","dwrite_2/IDWriteTextAnalyzer2::GetGlyphOrientationTransform"]
old-location: directwrite\idwritetextanalyzer2_getglyphorientationtransform.htm
tech.root: DirectWrite
ms.assetid: 4483AB14-3BC6-4980-A455-131BCBEBBFB9
ms.date: 12/05/2018
ms.keywords: GetGlyphOrientationTransform, GetGlyphOrientationTransform method [Direct Write], GetGlyphOrientationTransform method [Direct Write],IDWriteTextAnalyzer2 interface, IDWriteTextAnalyzer2 interface [Direct Write],GetGlyphOrientationTransform method, IDWriteTextAnalyzer2.GetGlyphOrientationTransform, IDWriteTextAnalyzer2::GetGlyphOrientationTransform, directwrite.idwritetextanalyzer2_getglyphorientationtransform, dwrite_2/IDWriteTextAnalyzer2::GetGlyphOrientationTransform
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
 - IDWriteTextAnalyzer2::GetGlyphOrientationTransform
 - dwrite_2/IDWriteTextAnalyzer2::GetGlyphOrientationTransform
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
 - IDWriteTextAnalyzer2.GetGlyphOrientationTransform
---

# IDWriteTextAnalyzer2::GetGlyphOrientationTransform


## -description

Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

Extends <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform">IDWriteTextAnalyzer1::GetGlyphOrientationTransform</a> to pass valid values for the baseline origin rather than zeroes.

## -parameters

### -param glyphOrientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a>-typed value that specifies the angle that was reported into
    <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">IDWriteTextAnalysisSink1::SetGlyphOrientation</a>.

### -param isSideways

Type: <b>BOOL</b>

Whether the run's glyphs are sideways or not.

### -param originX

Type: <b>FLOAT</b>

The X value of the baseline origin.

### -param originY

Type: <b>FLOAT</b>

The Y value of the baseline origin.

### -param transform [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

Returned transform.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextanalyzer2">IDWriteTextAnalyzer2</a>

