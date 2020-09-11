---
UID: NF:dwrite_1.IDWriteTextAnalysisSink1.SetGlyphOrientation
title: IDWriteTextAnalysisSink1::SetGlyphOrientation (dwrite_1.h)
description: The text analyzer calls back to this to report the actual orientation of each character for shaping and drawing.
helpviewer_keywords: ["IDWriteTextAnalysisSink1 interface [Direct Write]","SetGlyphOrientation method","IDWriteTextAnalysisSink1.SetGlyphOrientation","IDWriteTextAnalysisSink1::SetGlyphOrientation","SetGlyphOrientation","SetGlyphOrientation method [Direct Write]","SetGlyphOrientation method [Direct Write]","IDWriteTextAnalysisSink1 interface","directwrite.idwritetextanalysissink1_setglyphorientation","dwrite_1/IDWriteTextAnalysisSink1::SetGlyphOrientation"]
old-location: directwrite\idwritetextanalysissink1_setglyphorientation.htm
tech.root: DirectWrite
ms.assetid: 81BD4C36-273B-4C28-A89E-88BABCAD511A
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink1 interface [Direct Write],SetGlyphOrientation method, IDWriteTextAnalysisSink1.SetGlyphOrientation, IDWriteTextAnalysisSink1::SetGlyphOrientation, SetGlyphOrientation, SetGlyphOrientation method [Direct Write], SetGlyphOrientation method [Direct Write],IDWriteTextAnalysisSink1 interface, directwrite.idwritetextanalysissink1_setglyphorientation, dwrite_1/IDWriteTextAnalysisSink1::SetGlyphOrientation
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
 - IDWriteTextAnalysisSink1::SetGlyphOrientation
 - dwrite_1/IDWriteTextAnalysisSink1::SetGlyphOrientation
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
 - IDWriteTextAnalysisSink1.SetGlyphOrientation
---

# IDWriteTextAnalysisSink1::SetGlyphOrientation


## -description

The text analyzer calls back to this to report the actual orientation
    of each character for shaping and drawing.

## -parameters

### -param textPosition

Type: <b>UINT32 </b>

The starting position to report from.

### -param textLength

Type: <b>UINT32 </b>

Number of UTF-16 units of the reported range.

### -param glyphOrientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a>-typed value that specifies the angle of the glyphs within the text
    range (pass to <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform">IDWriteTextAnalyzer1::GetGlyphOrientationTransform</a> to get the world
    relative transform).

### -param adjustedBidiLevel

Type: <b>UINT8</b>

The adjusted bidi level to be used by
    the client layout for reordering runs. This will differ from the
    resolved bidi level retrieved from the source for cases such as
    Arabic stacked top-to-bottom, where the glyphs are still shaped
    as RTL, but the runs are TTB along with any CJK or Latin.

### -param isSideways

Type: <b>BOOL</b>

Whether the glyphs are rotated on their side,
    which is the default case for CJK and the case stacked Latin

### -param isRightToLeft

Type: <b>BOOL</b>

Whether the script should be shaped as
    right-to-left. For Arabic stacked top-to-bottom, even when the
    adjusted bidi level is coerced to an even level, this will still
    be true.

## -returns

Type: <b>HRESULT</b>

Returns a successful code or an error code to abort analysis.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1">IDWriteTextAnalysisSink1</a>

