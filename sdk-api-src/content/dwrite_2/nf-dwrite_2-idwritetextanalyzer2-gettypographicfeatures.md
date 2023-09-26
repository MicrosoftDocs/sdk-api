---
UID: NF:dwrite_2.IDWriteTextAnalyzer2.GetTypographicFeatures
title: IDWriteTextAnalyzer2::GetTypographicFeatures (dwrite_2.h)
description: Returns a complete list of OpenType features available for a script or font.
helpviewer_keywords: ["GetTypographicFeatures","GetTypographicFeatures method [Direct Write]","GetTypographicFeatures method [Direct Write]","IDWriteTextAnalyzer2 interface","IDWriteTextAnalyzer2 interface [Direct Write]","GetTypographicFeatures method","IDWriteTextAnalyzer2.GetTypographicFeatures","IDWriteTextAnalyzer2::GetTypographicFeatures","directwrite.idwritetextanalyzer2_gettypographicfeatures","dwrite_2/IDWriteTextAnalyzer2::GetTypographicFeatures"]
old-location: directwrite\idwritetextanalyzer2_gettypographicfeatures.htm
tech.root: DirectWrite
ms.assetid: 36CAC2F8-9065-4FD9-8EFD-529B97CE94D8
ms.date: 12/05/2018
ms.keywords: GetTypographicFeatures, GetTypographicFeatures method [Direct Write], GetTypographicFeatures method [Direct Write],IDWriteTextAnalyzer2 interface, IDWriteTextAnalyzer2 interface [Direct Write],GetTypographicFeatures method, IDWriteTextAnalyzer2.GetTypographicFeatures, IDWriteTextAnalyzer2::GetTypographicFeatures, directwrite.idwritetextanalyzer2_gettypographicfeatures, dwrite_2/IDWriteTextAnalyzer2::GetTypographicFeatures
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
 - IDWriteTextAnalyzer2::GetTypographicFeatures
 - dwrite_2/IDWriteTextAnalyzer2::GetTypographicFeatures
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
 - IDWriteTextAnalyzer2.GetTypographicFeatures
---

# IDWriteTextAnalyzer2::GetTypographicFeatures


## -description

Returns a complete list of OpenType features available for a script or font. If a feature is partially supported, then this method indicates that it is supported.

## -parameters

### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

The font face to get features from.

### -param scriptAnalysis

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a></b>

The script analysis for the script or font to check.

### -param localeName [in, optional]

Type: <b>const WCHAR*</b>

The locale name to check.

### -param maxTagCount

Type: <b>UINT32</b>

The maximum number of tags to return.

### -param actualTagCount [out]

Type: <b>UINT32*</b>

The actual number of tags returned.

### -param tags [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag">DWRITE_FONT_FEATURE_TAG</a>*</b>

An array of OpenType font feature tags.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextanalyzer2">IDWriteTextAnalyzer2</a>

