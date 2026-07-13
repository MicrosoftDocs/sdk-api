---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetTextComplexity
title: IDWriteTextAnalyzer1::GetTextComplexity (dwrite_1.h)
description: Determines the complexity of text, and whether you need to call IDWriteTextAnalyzer::GetGlyphs for full script shaping.
helpviewer_keywords: ["GetTextComplexity","GetTextComplexity method [Direct Write]","GetTextComplexity method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","GetTextComplexity method","IDWriteTextAnalyzer1.GetTextComplexity","IDWriteTextAnalyzer1::GetTextComplexity","directwrite.idwritetextanalyzer1_gettextcomplexity","dwrite_1/IDWriteTextAnalyzer1::GetTextComplexity"]
old-location: directwrite\idwritetextanalyzer1_gettextcomplexity.htm
tech.root: DirectWrite
ms.assetid: EC9364F7-4A00-4DEE-B51A-F26FBBA5683F
ms.date: 12/05/2018
ms.keywords: GetTextComplexity, GetTextComplexity method [Direct Write], GetTextComplexity method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetTextComplexity method, IDWriteTextAnalyzer1.GetTextComplexity, IDWriteTextAnalyzer1::GetTextComplexity, directwrite.idwritetextanalyzer1_gettextcomplexity, dwrite_1/IDWriteTextAnalyzer1::GetTextComplexity
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
 - IDWriteTextAnalyzer1::GetTextComplexity
 - dwrite_1/IDWriteTextAnalyzer1::GetTextComplexity
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
 - IDWriteTextAnalyzer1.GetTextComplexity
---

# IDWriteTextAnalyzer1::GetTextComplexity


## -description

Determines the complexity of text, and whether you need to call <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a> for full script
    shaping.

## -parameters

### -param textString [in]

Type: <b>const WCHAR*</b>

The text to check for complexity. This string
    may be UTF-16, but any supplementary characters will be considered
    complex.

### -param textLength

Type: <b>UINT32</b>

Length of the text to check.

### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace</a>*</b>

The font face to read.

### -param isTextSimple [out]

Type: <b>BOOL*</b>

If true, the text is simple, and the
    <i>glyphIndices</i> array will already have the nominal glyphs for you.
    Otherwise, you need to call <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a> to properly shape complex
    scripts and OpenType features.

### -param textLengthRead [out]

Type: <b>UINT32*</b>

The length read of the text run with the
    same complexity, simple or complex. You may call again from that
    point onward.

### -param glyphIndices [out, optional]

Type: <b>UINT16*</b>

Optional glyph indices for the text. If the
    function returned that the text was simple, you already have the
    glyphs you need. Otherwise the glyph indices are not meaningful,
    and you need to call <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a> for shaping instead.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Text is not simple if the characters are part of a script that has
    complex shaping requirements, require bidi analysis, combine with
    other characters, reside in the supplementary planes, or have glyphs
    that participate in standard OpenType features. The length returned
    will not split combining marks from their base characters.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a>

