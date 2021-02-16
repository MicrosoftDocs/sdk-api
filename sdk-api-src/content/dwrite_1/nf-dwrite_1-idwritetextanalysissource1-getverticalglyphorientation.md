---
UID: NF:dwrite_1.IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation
title: IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation (dwrite_1.h)
description: Used by the text analyzer to obtain the desired glyph orientation and resolved bidi level.
helpviewer_keywords: ["GetVerticalGlyphOrientation","GetVerticalGlyphOrientation method [Direct Write]","GetVerticalGlyphOrientation method [Direct Write]","IDWriteTextAnalysisSource1 interface","IDWriteTextAnalysisSource1 interface [Direct Write]","GetVerticalGlyphOrientation method","IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation","IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation","directwrite.idwritetextanalysissource1_getverticalglyphorientation","dwrite_1/IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation"]
old-location: directwrite\idwritetextanalysissource1_getverticalglyphorientation.htm
tech.root: DirectWrite
ms.assetid: 2F229E8A-171D-4DED-9E9E-F2925855E8C0
ms.date: 12/05/2018
ms.keywords: GetVerticalGlyphOrientation, GetVerticalGlyphOrientation method [Direct Write], GetVerticalGlyphOrientation method [Direct Write],IDWriteTextAnalysisSource1 interface, IDWriteTextAnalysisSource1 interface [Direct Write],GetVerticalGlyphOrientation method, IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation, IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation, directwrite.idwritetextanalysissource1_getverticalglyphorientation, dwrite_1/IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation
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
 - IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation
 - dwrite_1/IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation
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
 - IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation
---

# IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation


## -description

Used by the text analyzer to obtain the desired glyph
    orientation and resolved bidi level.

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The text position.

### -param textLength [out]

Type: <b>UINT32*</b>

A pointer to the text length.

### -param glyphOrientation [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation">DWRITE_VERTICAL_GLYPH_ORIENTATION</a>*</b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation">DWRITE_VERTICAL_GLYPH_ORIENTATION</a>-typed value that specifies the desired kind of glyph orientation for the text.

### -param bidiLevel [out]

Type: <b>UINT8*</b>

A pointer to the resolved bidi level.

## -returns

Type: <b>HRESULT</b>

Returning an error will abort the
    analysis.

## -remarks

The text analyzer calls back to this to get the desired glyph
    orientation and resolved bidi level, which it uses along with the
    script properties of the text to determine the actual orientation of
    each character, which it reports back to the client via the sink
    SetGlyphOrientation method.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1">IDWriteTextAnalysisSource1</a>

