---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.JustifyGlyphAdvances
title: IDWriteTextAnalyzer1::JustifyGlyphAdvances (dwrite_1.h)
description: Justifies an array of glyph advances to fit the line width.
helpviewer_keywords: ["IDWriteTextAnalyzer1 interface [Direct Write]","JustifyGlyphAdvances method","IDWriteTextAnalyzer1.JustifyGlyphAdvances","IDWriteTextAnalyzer1::JustifyGlyphAdvances","JustifyGlyphAdvances","JustifyGlyphAdvances method [Direct Write]","JustifyGlyphAdvances method [Direct Write]","IDWriteTextAnalyzer1 interface","directwrite.idwritetextanalyzer1_justifyglyphadvances","dwrite_1/IDWriteTextAnalyzer1::JustifyGlyphAdvances"]
old-location: directwrite\idwritetextanalyzer1_justifyglyphadvances.htm
tech.root: DirectWrite
ms.assetid: BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalyzer1 interface [Direct Write],JustifyGlyphAdvances method, IDWriteTextAnalyzer1.JustifyGlyphAdvances, IDWriteTextAnalyzer1::JustifyGlyphAdvances, JustifyGlyphAdvances, JustifyGlyphAdvances method [Direct Write], JustifyGlyphAdvances method [Direct Write],IDWriteTextAnalyzer1 interface, directwrite.idwritetextanalyzer1_justifyglyphadvances, dwrite_1/IDWriteTextAnalyzer1::JustifyGlyphAdvances
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
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextAnalyzer1::JustifyGlyphAdvances
 - dwrite_1/IDWriteTextAnalyzer1::JustifyGlyphAdvances
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteTextAnalyzer1.JustifyGlyphAdvances
---

# IDWriteTextAnalyzer1::JustifyGlyphAdvances


## -description

Justifies an array of glyph advances to fit the line width.

## -parameters

### -param lineWidth

Type: <b>FLOAT</b>

The line width.

### -param glyphCount

Type: <b>UINT32</b>

The glyph count.

### -param justificationOpportunities [in]

Type: <b>const <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity">DWRITE_JUSTIFICATION_OPPORTUNITY</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity">DWRITE_JUSTIFICATION_OPPORTUNITY</a> structure that contains info for the
    allowed justification expansion/compression for each glyph. Get this info from <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities">IDWriteTextAnalyzer1::GetJustificationOpportunities</a>.

### -param glyphAdvances [in]

Type: <b>const FLOAT*</b>

An array of glyph advances.

### -param glyphOffsets [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

An array of glyph offsets.

### -param justifiedGlyphAdvances [out]

Type: <b>FLOAT*</b>

The returned array of justified glyph advances.

### -param justifiedGlyphOffsets [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

The returned array of justified glyph offsets.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You call  <b>JustifyGlyphAdvances</b> after you call <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities">IDWriteTextAnalyzer1::GetJustificationOpportunities</a> to collect all the opportunities, and <b>JustifyGlyphAdvances</b> spans across the entire line. The input and output arrays are allowed
    to alias each other, permitting in-place update.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities">IDWriteTextAnalyzer1::GetJustificationOpportunities</a>

