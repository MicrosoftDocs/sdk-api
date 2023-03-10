---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeNumberSubstitution
title: IDWriteTextAnalyzer::AnalyzeNumberSubstitution (dwrite.h)
description: Analyzes a text range for spans where number substitution is applicable, reading attributes from the source and reporting substitutable ranges to the sink callback SetNumberSubstitution.
helpviewer_keywords: ["AnalyzeNumberSubstitution","AnalyzeNumberSubstitution method [Direct Write]","AnalyzeNumberSubstitution method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","AnalyzeNumberSubstitution method","IDWriteTextAnalyzer.AnalyzeNumberSubstitution","IDWriteTextAnalyzer::AnalyzeNumberSubstitution","directwrite.IDWriteTextAnalyzer_AnalyzeNumberSubstitution","dwrite/IDWriteTextAnalyzer::AnalyzeNumberSubstitution"]
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeNumberSubstitution.htm
tech.root: DirectWrite
ms.assetid: 1cd53f79-5bbc-4a70-b66a-b807fe163a98
ms.date: 12/05/2018
ms.keywords: AnalyzeNumberSubstitution, AnalyzeNumberSubstitution method [Direct Write], AnalyzeNumberSubstitution method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeNumberSubstitution method, IDWriteTextAnalyzer.AnalyzeNumberSubstitution, IDWriteTextAnalyzer::AnalyzeNumberSubstitution, directwrite.IDWriteTextAnalyzer_AnalyzeNumberSubstitution, dwrite/IDWriteTextAnalyzer::AnalyzeNumberSubstitution
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
 - IDWriteTextAnalyzer::AnalyzeNumberSubstitution
 - dwrite/IDWriteTextAnalyzer::AnalyzeNumberSubstitution
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
 - IDWriteTextAnalyzer.AnalyzeNumberSubstitution
---

# IDWriteTextAnalyzer::AnalyzeNumberSubstitution


## -description

 Analyzes a text range for spans where number substitution is applicable,
     reading attributes from the source and reporting substitutable ranges
     to the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution">SetNumberSubstitution</a>.

## -parameters

### -param analysisSource

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>*</b>

The source object to analyze.

### -param textPosition

Type: <b>UINT32</b>

The starting position within the source object.

### -param textLength

Type: <b>UINT32</b>

The length to analyze.

### -param analysisSink

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>*</b>

A pointer to the sink callback object that receives the text analysis.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Although the function can handle multiple ranges of differing number
     substitutions, the text ranges should not arbitrarily split the
     middle of numbers. Otherwise, it will treat the numbers separately
     and will not translate any intervening punctuation.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

