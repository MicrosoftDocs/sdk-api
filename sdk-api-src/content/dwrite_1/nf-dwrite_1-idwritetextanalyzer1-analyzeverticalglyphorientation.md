---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation
title: IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation (dwrite_1.h)
description: Analyzes a text range for script orientation, reading text and attributes from the source and reporting results to the sink callback SetGlyphOrientation.
helpviewer_keywords: ["AnalyzeVerticalGlyphOrientation","AnalyzeVerticalGlyphOrientation method [Direct Write]","AnalyzeVerticalGlyphOrientation method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","AnalyzeVerticalGlyphOrientation method","IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation","IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation","directwrite.idwritetextanalyzer1_analyzeverticalglyphorientation","dwrite_1/IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation"]
old-location: directwrite\idwritetextanalyzer1_analyzeverticalglyphorientation.htm
tech.root: DirectWrite
ms.assetid: E89C7E50-9EDA-4AC9-9FC0-B70E493ED1B4
ms.date: 12/05/2018
ms.keywords: AnalyzeVerticalGlyphOrientation, AnalyzeVerticalGlyphOrientation method [Direct Write], AnalyzeVerticalGlyphOrientation method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],AnalyzeVerticalGlyphOrientation method, IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation, IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation, directwrite.idwritetextanalyzer1_analyzeverticalglyphorientation, dwrite_1/IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation
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
 - IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation
 - dwrite_1/IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation
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
 - IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation
---

# IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation


## -description

Analyzes a text range for script orientation, reading text and
    attributes from the source and reporting results to the sink callback <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">SetGlyphOrientation</a>.

## -parameters

### -param analysisSource

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1">IDWriteTextAnalysisSource1</a>*</b>

Source object to analyze.

### -param textPosition

Type: <b>UINT32</b>

Starting position within the source object.

### -param textLength

Type: <b>UINT32</b>

Length to analyze.

### -param analysisSink

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1">IDWriteTextAnalysisSink1</a>*</b>

Length to analyze.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>

