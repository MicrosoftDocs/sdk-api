---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeLineBreakpoints
title: IDWriteTextAnalyzer::AnalyzeLineBreakpoints (dwrite.h)
description: Analyzes a text range for potential breakpoint opportunities, reading attributes from the source and reporting breakpoint opportunities to the sink callback SetLineBreakpoints.
helpviewer_keywords: ["AnalyzeLineBreakpoints","AnalyzeLineBreakpoints method [Direct Write]","AnalyzeLineBreakpoints method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","AnalyzeLineBreakpoints method","IDWriteTextAnalyzer.AnalyzeLineBreakpoints","IDWriteTextAnalyzer::AnalyzeLineBreakpoints","directwrite.IDWriteTextAnalyzer_AnalyzeLineBreakpoints","dwrite/IDWriteTextAnalyzer::AnalyzeLineBreakpoints"]
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeLineBreakpoints.htm
tech.root: DirectWrite
ms.assetid: 6c676065-0226-456c-b8c4-10752a8daec8
ms.date: 12/05/2018
ms.keywords: AnalyzeLineBreakpoints, AnalyzeLineBreakpoints method [Direct Write], AnalyzeLineBreakpoints method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeLineBreakpoints method, IDWriteTextAnalyzer.AnalyzeLineBreakpoints, IDWriteTextAnalyzer::AnalyzeLineBreakpoints, directwrite.IDWriteTextAnalyzer_AnalyzeLineBreakpoints, dwrite/IDWriteTextAnalyzer::AnalyzeLineBreakpoints
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
 - IDWriteTextAnalyzer::AnalyzeLineBreakpoints
 - dwrite/IDWriteTextAnalyzer::AnalyzeLineBreakpoints
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
 - IDWriteTextAnalyzer.AnalyzeLineBreakpoints
---

# IDWriteTextAnalyzer::AnalyzeLineBreakpoints


## -description

 Analyzes a text range for potential breakpoint opportunities, reading
     attributes from the source and reporting breakpoint opportunities to
     the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setlinebreakpoints">SetLineBreakpoints</a>.

## -parameters

### -param analysisSource

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>*</b>

A pointer to the source object to analyze.

### -param textPosition

Type: <b>UINT32</b>

The starting text position within the source object.

### -param textLength

Type: <b>UINT32</b>

The text length to analyze.

### -param analysisSink

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>*</b>

A pointer to the  sink callback object that receives the text analysis.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Although the function can handle multiple paragraphs, the text range
     should not arbitrarily split the middle of paragraphs, unless the
     specified text span is considered a whole unit. Otherwise, the
     returned properties for the first and last characters will
     inappropriately allow breaks.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

