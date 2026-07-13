---
UID: NF:dwrite.IDWriteTextAnalyzer.GetGlyphs
title: IDWriteTextAnalyzer::GetGlyphs (dwrite.h)
description: Parses the input text string and maps it to the set of glyphs and associated glyph data according to the font and the writing system's rendering rules.
helpviewer_keywords: ["GetGlyphs","GetGlyphs method [Direct Write]","GetGlyphs method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","GetGlyphs method","IDWriteTextAnalyzer.GetGlyphs","IDWriteTextAnalyzer::GetGlyphs","directwrite.IDWriteTextAnalyzer_GetGlyphs","dwrite/IDWriteTextAnalyzer::GetGlyphs"]
old-location: directwrite\IDWriteTextAnalyzer_GetGlyphs.htm
tech.root: DirectWrite
ms.assetid: 9bc373b6-9161-4ffc-a942-50d97d6509c3
ms.date: 12/05/2018
ms.keywords: GetGlyphs, GetGlyphs method [Direct Write], GetGlyphs method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],GetGlyphs method, IDWriteTextAnalyzer.GetGlyphs, IDWriteTextAnalyzer::GetGlyphs, directwrite.IDWriteTextAnalyzer_GetGlyphs, dwrite/IDWriteTextAnalyzer::GetGlyphs
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteTextAnalyzer::GetGlyphs
 - dwrite/IDWriteTextAnalyzer::GetGlyphs
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
 - IDWriteTextAnalyzer.GetGlyphs
---

# IDWriteTextAnalyzer::GetGlyphs


## -description

 Parses the input text string and maps it to the set of glyphs and associated glyph data
     according to the font and the writing system's rendering rules.

## -parameters

### -param textString [in]

Type: <b>const WCHAR*</b>

An array of characters to convert to glyphs.

### -param textLength

Type: <b>UINT32</b>

The length of <i>textString</i>.

### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

The font face that is the source of the output glyphs.

### -param isSideways

Type: <b>BOOL</b>

A Boolean flag set to <b>TRUE</b> if the text is intended to be
     drawn vertically.

### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag set to <b>TRUE</b> for right-to-left text.

### -param scriptAnalysis [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a>*</b>

A pointer to a Script analysis result from an <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript">AnalyzeScript</a> call.

### -param localeName [in, optional]

Type: <b>const WCHAR*</b>

The locale to use when selecting glyphs.
     For example the same character may map to different glyphs for ja-jp versus zh-chs.
     If this is <b>NULL</b>, then the default mapping based on the script is used.

### -param numberSubstitution [optional]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritenumbersubstitution">IDWriteNumberSubstitution</a>*</b>

A pointer to an optional number substitution which selects the appropriate glyphs for digits and related numeric characters, depending on the results obtained from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzenumbersubstitution">AnalyzeNumberSubstitution</a>. Passing <b>NULL</b> indicates that no substitution is needed and that the digits should receive nominal glyphs.

### -param features [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features">DWRITE_TYPOGRAPHIC_FEATURES</a>**</b>

An array of pointers to the sets of typographic 
     features to use in each feature range.

### -param featureRangeLengths [in, optional]

Type: <b>const UINT32*</b>

The length of each feature range, in characters.  
     The sum of all lengths should be equal to <i>textLength</i>.

### -param featureRanges

Type: <b>UINT32</b>

The number of feature ranges.

### -param maxGlyphCount

Type: <b>UINT32</b>

The maximum number of glyphs that can be
     returned.

### -param clusterMap [out]

Type: <b>UINT16*</b>

When this method returns, contains the mapping from character ranges to glyph 
     ranges.

### -param textProps [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties">DWRITE_SHAPING_TEXT_PROPERTIES</a>*</b>

When this method returns, contains a pointer to an array of structures that contains  shaping properties for each character.

### -param glyphIndices [out]

Type: <b>UINT16*</b>

The output glyph indices.

### -param glyphProps [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties">DWRITE_SHAPING_GLYPH_PROPERTIES</a>*</b>

When this method returns, contains a pointer to an array of structures that contain  shaping properties for each output glyph.

### -param actualGlyphCount [out]

Type: <b>UINT32*</b>

When this method returns, contains the actual number of glyphs returned if
     the call succeeds.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note that the mapping from characters to glyphs is, in general, many-to-many.  The recommended estimate for the per-glyph output buffers is (3 * <i>textLength</i> / 2 + 16).  This is not guaranteed to be sufficient.

The value of the <i>actualGlyphCount</i> parameter is only valid if the call succeeds.  In the event that <i>maxGlyphCount</i> is not big enough, <b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b> will be returned. The application should allocate a larger buffer and try again.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

