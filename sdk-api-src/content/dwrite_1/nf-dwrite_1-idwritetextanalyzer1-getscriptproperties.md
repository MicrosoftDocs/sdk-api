---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetScriptProperties
title: IDWriteTextAnalyzer1::GetScriptProperties (dwrite_1.h)
description: Retrieves the properties for a given script.
helpviewer_keywords: ["GetScriptProperties","GetScriptProperties method [Direct Write]","GetScriptProperties method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","GetScriptProperties method","IDWriteTextAnalyzer1.GetScriptProperties","IDWriteTextAnalyzer1::GetScriptProperties","directwrite.idwritetextanalyzer1_getscriptproperties","dwrite_1/IDWriteTextAnalyzer1::GetScriptProperties"]
old-location: directwrite\idwritetextanalyzer1_getscriptproperties.htm
tech.root: DirectWrite
ms.assetid: CBC1DA09-6D3D-42D8-8E77-CFDBA733C228
ms.date: 12/05/2018
ms.keywords: GetScriptProperties, GetScriptProperties method [Direct Write], GetScriptProperties method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetScriptProperties method, IDWriteTextAnalyzer1.GetScriptProperties, IDWriteTextAnalyzer1::GetScriptProperties, directwrite.idwritetextanalyzer1_getscriptproperties, dwrite_1/IDWriteTextAnalyzer1::GetScriptProperties
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
 - IDWriteTextAnalyzer1::GetScriptProperties
 - dwrite_1/IDWriteTextAnalyzer1::GetScriptProperties
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
 - IDWriteTextAnalyzer1.GetScriptProperties
---

# IDWriteTextAnalyzer1::GetScriptProperties


## -description

Retrieves the properties for a given script.

## -parameters

### -param scriptAnalysis

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis">DWRITE_SCRIPT_ANALYSIS</a></b>

The script for a run of text returned
    from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript">IDWriteTextAnalyzer::AnalyzeScript</a>.

### -param scriptProperties [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties">DWRITE_SCRIPT_PROPERTIES</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties">DWRITE_SCRIPT_PROPERTIES</a> structure that describes info for the script.

## -returns

Type: <b>HRESULT</b>

Returns properties for the given script. If the script is invalid,
    it returns generic properties for the unknown script and E_INVALIDARG.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>

