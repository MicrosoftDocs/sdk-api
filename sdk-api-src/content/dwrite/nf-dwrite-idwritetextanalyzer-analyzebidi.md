---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeBidi
title: IDWriteTextAnalyzer::AnalyzeBidi (dwrite.h)
description: Analyzes a text range for script directionality, reading attributes from the source and reporting levels to the sink callback SetBidiLevel.
helpviewer_keywords: ["AnalyzeBidi","AnalyzeBidi method [Direct Write]","AnalyzeBidi method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","AnalyzeBidi method","IDWriteTextAnalyzer.AnalyzeBidi","IDWriteTextAnalyzer::AnalyzeBidi","directwrite.IDWriteTextAnalyzer_AnalyzeBidi","dwrite/IDWriteTextAnalyzer::AnalyzeBidi"]
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeBidi.htm
tech.root: DirectWrite
ms.assetid: 413d49d2-bacd-4e98-bfac-c0aea2650a7c
ms.date: 12/05/2018
ms.keywords: AnalyzeBidi, AnalyzeBidi method [Direct Write], AnalyzeBidi method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeBidi method, IDWriteTextAnalyzer.AnalyzeBidi, IDWriteTextAnalyzer::AnalyzeBidi, directwrite.IDWriteTextAnalyzer_AnalyzeBidi, dwrite/IDWriteTextAnalyzer::AnalyzeBidi
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
 - IDWriteTextAnalyzer::AnalyzeBidi
 - dwrite/IDWriteTextAnalyzer::AnalyzeBidi
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
 - IDWriteTextAnalyzer.AnalyzeBidi
---

# IDWriteTextAnalyzer::AnalyzeBidi


## -description

 Analyzes a text range for script directionality, reading attributes
     from the source and reporting levels to the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setbidilevel">SetBidiLevel</a>.

## -parameters

### -param analysisSource

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>*</b>

A pointer to a source object to analyze.

### -param textPosition

Type: <b>UINT32</b>

The starting text position within the source object.

### -param textLength

Type: <b>UINT32</b>

The text length to analyze.

### -param analysisSink

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>*</b>

A pointer to the sink callback object that receives the text analysis.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 While the function can handle multiple paragraphs, the text range
     should not arbitrarily split the middle of paragraphs. Otherwise, the
     returned levels may be wrong, because the Bidi algorithm is meant to
     apply to the paragraph as a whole.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

