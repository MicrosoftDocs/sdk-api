---
UID: NF:dwrite.IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
title: IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements (dwrite.h)
description: Place glyphs output from the GetGlyphs method according to the font and the writing system's rendering rules.
helpviewer_keywords: ["GetGdiCompatibleGlyphPlacements","GetGdiCompatibleGlyphPlacements method [Direct Write]","GetGdiCompatibleGlyphPlacements method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","GetGdiCompatibleGlyphPlacements method","IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements","IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements","directwrite.idwritetextanalyzer_getgdicompatibleglyphplacements","dwrite/IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements"]
old-location: directwrite\idwritetextanalyzer_getgdicompatibleglyphplacements.htm
tech.root: DirectWrite
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
ms.date: 12/05/2018
ms.keywords: GetGdiCompatibleGlyphPlacements, GetGdiCompatibleGlyphPlacements method [Direct Write], GetGdiCompatibleGlyphPlacements method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],GetGdiCompatibleGlyphPlacements method, IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements, IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements, directwrite.idwritetextanalyzer_getgdicompatibleglyphplacements, dwrite/IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements
 - dwrite/IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements
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
 - IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
---

# IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements


## -description

Place glyphs output from the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a> method according to the font 
    and the writing system's rendering rules.

## -parameters

### -param textString [in]

Type: <b>const WCHAR*</b>

An array of characters containing the original string from which the glyphs came.

### -param clusterMap [in]

Type: <b>const UINT16*</b>

A pointer to the mapping from character ranges to glyph 
     ranges. This is returned by <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>.

### -param textProps [in]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties">DWRITE_SHAPING_TEXT_PROPERTIES</a>*</b>

A pointer to an array of structures that contains  shaping properties for each character. This structure is returned by 
     <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>.

### -param textLength

Type: <b>UINT32</b>

The text length of <i>textString</i>.

### -param glyphIndices [in]

Type: <b>const UINT16*</b>

An array of glyph indices returned by <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>.

### -param glyphProps [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties">DWRITE_SHAPING_GLYPH_PROPERTIES</a>*</b>

A pointer to an array of structures that contain  shaping properties for each glyph returned by <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>.

### -param glyphCount

Type: <b>UINT32</b>

The number of glyphs returned from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>.

### -param fontFace [in]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

A pointer to the font face that is the source for the output glyphs.

### -param fontEmSize

Type: <b>FLOAT</b>

The logical font size in DIPs.

### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP.

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

An optional transform applied to the glyphs and their positions. This transform is applied after the scaling specified by the font size and <i>pixelsPerDip</i>.

### -param useGdiNatural

Type: <b>BOOL</b>

When set to <b>FALSE</b>, the metrics are the same as the metrics of GDI aliased text.  When set to <b>TRUE</b>, the metrics are the same as the metrics of text measured by GDI using a font created with <b>CLEARTYPE_NATURAL_QUALITY</b>.

### -param isSideways

Type: <b>BOOL</b>

A Boolean flag set to <b>TRUE</b> if the text is intended to be
     drawn vertically.

### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag set to <b>TRUE</b> for right-to-left text.

### -param scriptAnalysis [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a>*</b>

A pointer to a Script analysis result from an<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript">AnalyzeScript</a> call.

### -param localeName [in, optional]

Type: <b>const WCHAR*</b>

An array of characters containing the locale to use when selecting glyphs.
     For example, the same character may map to different glyphs for ja-jp versus zh-chs.
     If this is <b>NULL</b>, then the default mapping based on the script is used.

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

### -param glyphAdvances [out]

Type: <b>FLOAT*</b>

When this method returns, contains the advance width of each glyph.

### -param glyphOffsets [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

When this method returns, contains the offset of the origin of each glyph.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

