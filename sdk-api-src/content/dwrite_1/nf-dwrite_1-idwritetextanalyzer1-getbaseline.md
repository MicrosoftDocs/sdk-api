---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetBaseline
title: IDWriteTextAnalyzer1::GetBaseline (dwrite_1.h)
description: Retrieves the given baseline from the font.
helpviewer_keywords: ["GetBaseline","GetBaseline method [Direct Write]","GetBaseline method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","GetBaseline method","IDWriteTextAnalyzer1.GetBaseline","IDWriteTextAnalyzer1::GetBaseline","directwrite.idwritetextanalyzer1_getbaseline","dwrite_1/IDWriteTextAnalyzer1::GetBaseline"]
old-location: directwrite\idwritetextanalyzer1_getbaseline.htm
tech.root: DirectWrite
ms.assetid: 5ACD5075-BD96-41FC-AE36-8D5D03F2EB54
ms.date: 12/05/2018
ms.keywords: GetBaseline, GetBaseline method [Direct Write], GetBaseline method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetBaseline method, IDWriteTextAnalyzer1.GetBaseline, IDWriteTextAnalyzer1::GetBaseline, directwrite.idwritetextanalyzer1_getbaseline, dwrite_1/IDWriteTextAnalyzer1::GetBaseline
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
 - IDWriteTextAnalyzer1::GetBaseline
 - dwrite_1/IDWriteTextAnalyzer1::GetBaseline
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
 - IDWriteTextAnalyzer1.GetBaseline
---

# IDWriteTextAnalyzer1::GetBaseline


## -description

Retrieves the given baseline from the font.

## -parameters

### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace</a>*</b>

The font face to read.

### -param baseline

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_baseline">DWRITE_BASELINE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_baseline">DWRITE_BASELINE</a>-typed value that specifies the baseline of interest.

### -param isVertical

Type: <b>BOOL</b>

Whether the baseline is vertical or horizontal.

### -param isSimulationAllowed

Type: <b>BOOL</b>

Simulate the baseline if it is missing in the font.

### -param scriptAnalysis

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a></b>

Script analysis result from AnalyzeScript.

<div class="alert"><b>Note</b>  You can pass an empty script analysis structure, like this <code>DWRITE_SCRIPT_ANALYSIS scriptAnalysis = {};</code>, and this method will return the default baseline.</div>
<div> </div>

### -param localeName [in, optional]

Type: <b>const WCHAR*</b>

The language of the run.

### -param baselineCoordinate [out]

Type: <b>INT32*</b>

The baseline coordinate value in design units.

### -param exists [out]

Type: <b>BOOL*</b>

Whether the returned baseline exists in the font.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the baseline does not exist in the font, it is not considered an
    error, but the function will return exists = false. You may then use
    heuristics to calculate the missing base, or, if the flag
    simulationAllowed is true, the function will compute a reasonable
    approximation for you.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>

