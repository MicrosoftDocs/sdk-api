---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeScript
title: IDWriteTextAnalyzer::AnalyzeScript (dwrite.h)
description: Analyzes a text range for script boundaries, reading text attributes from the source and reporting the Unicode script ID to the sink callback SetScript.
helpviewer_keywords: ["AnalyzeScript","AnalyzeScript method [Direct Write]","AnalyzeScript method [Direct Write]","IDWriteTextAnalyzer interface","IDWriteTextAnalyzer interface [Direct Write]","AnalyzeScript method","IDWriteTextAnalyzer.AnalyzeScript","IDWriteTextAnalyzer::AnalyzeScript","directwrite.IDWriteTextAnalyzer_AnalyzeScript","dwrite/IDWriteTextAnalyzer::AnalyzeScript"]
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeScript.htm
tech.root: DirectWrite
ms.assetid: e681f7c8-7d87-454b-a7b6-6c3fe38b0f92
ms.date: 12/05/2018
ms.keywords: AnalyzeScript, AnalyzeScript method [Direct Write], AnalyzeScript method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeScript method, IDWriteTextAnalyzer.AnalyzeScript, IDWriteTextAnalyzer::AnalyzeScript, directwrite.IDWriteTextAnalyzer_AnalyzeScript, dwrite/IDWriteTextAnalyzer::AnalyzeScript
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
 - IDWriteTextAnalyzer::AnalyzeScript
 - dwrite/IDWriteTextAnalyzer::AnalyzeScript
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
 - IDWriteTextAnalyzer.AnalyzeScript
---

# IDWriteTextAnalyzer::AnalyzeScript


## -description

 Analyzes a text range for script boundaries, reading text attributes
     from the source and reporting the Unicode script ID to the sink 
     callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setscriptanalysis">SetScript</a>.

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

A pointer to the sink callback object that receives the text analysis.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>

