---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetJustifiedGlyphs
title: IDWriteTextAnalyzer1::GetJustifiedGlyphs (dwrite_1.h)
description: Fills in new glyphs for complex scripts where justification increased the advances of glyphs, such as Arabic with kashida.
helpviewer_keywords: ["GetJustifiedGlyphs","GetJustifiedGlyphs method [Direct Write]","GetJustifiedGlyphs method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","GetJustifiedGlyphs method","IDWriteTextAnalyzer1.GetJustifiedGlyphs","IDWriteTextAnalyzer1::GetJustifiedGlyphs","directwrite.idwritetextanalyzer1_getjustifiedglyphs","dwrite_1/IDWriteTextAnalyzer1::GetJustifiedGlyphs"]
old-location: directwrite\idwritetextanalyzer1_getjustifiedglyphs.htm
tech.root: DirectWrite
ms.assetid: 8F7BB9EC-90AE-48BD-A596-EAF2EDC4053F
ms.date: 12/05/2018
ms.keywords: GetJustifiedGlyphs, GetJustifiedGlyphs method [Direct Write], GetJustifiedGlyphs method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetJustifiedGlyphs method, IDWriteTextAnalyzer1.GetJustifiedGlyphs, IDWriteTextAnalyzer1::GetJustifiedGlyphs, directwrite.idwritetextanalyzer1_getjustifiedglyphs, dwrite_1/IDWriteTextAnalyzer1::GetJustifiedGlyphs
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
 - IDWriteTextAnalyzer1::GetJustifiedGlyphs
 - dwrite_1/IDWriteTextAnalyzer1::GetJustifiedGlyphs
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
 - IDWriteTextAnalyzer1.GetJustifiedGlyphs
---

# IDWriteTextAnalyzer1::GetJustifiedGlyphs


## -description

Fills in new glyphs for complex scripts where justification increased
    the advances of glyphs, such as Arabic with kashida.

## -parameters

### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace</a>*</b>

Font face used for shaping.

May be NULL.

### -param fontEmSize

Type: <b>FLOAT</b>

Font em size used for the glyph run.

### -param scriptAnalysis

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a></b>

Script of the text from the itemizer.

### -param textLength

Type: <b>UINT32</b>

Length of the text.

### -param glyphCount

Type: <b>UINT32</b>

Number of glyphs.

### -param maxGlyphCount

Type: <b>UINT32</b>

Maximum number of output glyphs allocated
    by caller.

### -param clusterMap [in, optional]

Type: <b>const UINT16*</b>

Clustermap produced from shaping.

### -param glyphIndices [in]

Type: <b>const UINT16*</b>

Original glyphs produced from shaping.

### -param glyphAdvances [in]

Type: <b>const FLOAT*</b>

Original glyph advances produced from shaping.

### -param justifiedGlyphAdvances [in]

Type: <b>const FLOAT*</b>

Justified glyph advances from
    <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>.

### -param justifiedGlyphOffsets [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

Justified glyph offsets from
    <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>.

### -param glyphProperties [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties">DWRITE_SHAPING_GLYPH_PROPERTIES</a>*</b>

Properties of each glyph, from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a>.

### -param actualGlyphCount [out]

Type: <b>UINT32*</b>

The new glyph count written to the
    modified arrays, or the needed glyph count if the size is not
    large enough.

### -param modifiedClusterMap [out, optional]

Type: <b>UINT16*</b>

Updated clustermap.

### -param modifiedGlyphIndices [out]

Type: <b>UINT16*</b>

Updated glyphs with new glyphs
    inserted where needed.

### -param modifiedGlyphAdvances [out]

Type: <b>FLOAT*</b>

Updated glyph advances.

### -param modifiedGlyphOffsets [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

Updated glyph offsets.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You call <b>GetJustifiedGlyphs</b> after the line has been justified, and it is per-run.

You should call <b>GetJustifiedGlyphs</b> if <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties">IDWriteTextAnalyzer1::GetScriptProperties</a> returns a non-null <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties">DWRITE_SCRIPT_PROPERTIES.justificationCharacter</a> for that script.

 Use  <b>GetJustifiedGlyphs</b> mainly for cursive scripts
    like Arabic. If <i>maxGlyphCount</i> is not large enough, <b>GetJustifiedGlyphs</b> returns the error
    E_NOT_SUFFICIENT_BUFFER and fills the variable  to which <i>actualGlyphCount</i>  points with
    the needed glyph count.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties">IDWriteTextAnalyzer1::GetScriptProperties</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a>

