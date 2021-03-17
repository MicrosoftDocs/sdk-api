---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetScriptAnalysis
title: IDWriteTextAnalysisSink::SetScriptAnalysis (dwrite.h)
description: Reports script analysis for the specified text range.
helpviewer_keywords: ["IDWriteTextAnalysisSink interface [Direct Write]","SetScriptAnalysis method","IDWriteTextAnalysisSink.SetScriptAnalysis","IDWriteTextAnalysisSink::SetScriptAnalysis","SetScriptAnalysis","SetScriptAnalysis method [Direct Write]","SetScriptAnalysis method [Direct Write]","IDWriteTextAnalysisSink interface","directwrite.idwritetextanalysissink_setscriptanalysis","dwrite/IDWriteTextAnalysisSink::SetScriptAnalysis"]
old-location: directwrite\idwritetextanalysissink_setscriptanalysis.htm
tech.root: DirectWrite
ms.assetid: beae0420-b244-4c87-a3cb-a1b34562c3ed
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetScriptAnalysis method, IDWriteTextAnalysisSink.SetScriptAnalysis, IDWriteTextAnalysisSink::SetScriptAnalysis, SetScriptAnalysis, SetScriptAnalysis method [Direct Write], SetScriptAnalysis method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setscriptanalysis, dwrite/IDWriteTextAnalysisSink::SetScriptAnalysis
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
 - IDWriteTextAnalysisSink::SetScriptAnalysis
 - dwrite/IDWriteTextAnalysisSink::SetScriptAnalysis
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
 - IDWriteTextAnalysisSink.SetScriptAnalysis
---

# IDWriteTextAnalysisSink::SetScriptAnalysis


## -description

Reports script analysis for the specified text range.

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The starting position from which to report.

### -param textLength

Type: <b>UINT32</b>

The number of UTF16 units of the reported range.

### -param scriptAnalysis

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a>*</b>

A pointer to a structure that contains a zero-based index representation of a writing system script and a value indicating whether additional shaping of text is required.

## -returns

Type: <b>HRESULT</b>

A successful code or error code to stop analysis.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>

