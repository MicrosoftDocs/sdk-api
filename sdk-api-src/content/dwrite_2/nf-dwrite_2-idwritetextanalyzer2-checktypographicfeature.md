---
UID: NF:dwrite_2.IDWriteTextAnalyzer2.CheckTypographicFeature
title: IDWriteTextAnalyzer2::CheckTypographicFeature (dwrite_2.h)
description: Checks if a typographic feature is available for a glyph or a set of glyphs.
helpviewer_keywords: ["CheckTypographicFeature","CheckTypographicFeature method [Direct Write]","CheckTypographicFeature method [Direct Write]","IDWriteTextAnalyzer2 interface","IDWriteTextAnalyzer2 interface [Direct Write]","CheckTypographicFeature method","IDWriteTextAnalyzer2.CheckTypographicFeature","IDWriteTextAnalyzer2::CheckTypographicFeature","directwrite.idwritetextanalyzer2_checktypographicfeature","dwrite_2/IDWriteTextAnalyzer2::CheckTypographicFeature"]
old-location: directwrite\idwritetextanalyzer2_checktypographicfeature.htm
tech.root: DirectWrite
ms.assetid: D929E654-1DF1-49AB-A311-010DB2D79E06
ms.date: 12/05/2018
ms.keywords: CheckTypographicFeature, CheckTypographicFeature method [Direct Write], CheckTypographicFeature method [Direct Write],IDWriteTextAnalyzer2 interface, IDWriteTextAnalyzer2 interface [Direct Write],CheckTypographicFeature method, IDWriteTextAnalyzer2.CheckTypographicFeature, IDWriteTextAnalyzer2::CheckTypographicFeature, directwrite.idwritetextanalyzer2_checktypographicfeature, dwrite_2/IDWriteTextAnalyzer2::CheckTypographicFeature
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
 - IDWriteTextAnalyzer2::CheckTypographicFeature
 - dwrite_2/IDWriteTextAnalyzer2::CheckTypographicFeature
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
 - IDWriteTextAnalyzer2.CheckTypographicFeature
---

# IDWriteTextAnalyzer2::CheckTypographicFeature


## -description

Checks if a typographic feature is available for a glyph or a set of glyphs.

## -parameters

### -param fontFace

The font face to read glyph information from.

### -param scriptAnalysis

The script analysis for the script or font to check.

### -param localeName [in, optional]

The locale name to check.

### -param featureTag

The font feature tag to check.

### -param glyphCount

The number of glyphs to check.

### -param glyphIndices [in]

An array of glyph indices to check.

### -param featureApplies [out]

An array of integers that indicate whether or not the font feature applies to each glyph specified.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextanalyzer2">IDWriteTextAnalyzer2</a>

