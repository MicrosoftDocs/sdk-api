---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetScriptProperties
title: IDWriteTextAnalyzer1::GetScriptProperties
author: windows-sdk-content
description: Retrieves the properties for a given script.
old-location: directwrite\idwritetextanalyzer1_getscriptproperties.htm
tech.root: DirectWrite
ms.assetid: CBC1DA09-6D3D-42D8-8E77-CFDBA733C228
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetScriptProperties, GetScriptProperties method [Direct Write], GetScriptProperties method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetScriptProperties method, IDWriteTextAnalyzer1.GetScriptProperties, IDWriteTextAnalyzer1::GetScriptProperties, directwrite.idwritetextanalyzer1_getscriptproperties, dwrite_1/IDWriteTextAnalyzer1::GetScriptProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteTextAnalyzer1.GetScriptProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1::GetScriptProperties


## -description


Retrieves the properties for a given script.


## -parameters




### -param scriptAnalysis

Type: <b><a href="https://msdn.microsoft.com/dafda5f6-39aa-4577-9213-898bdeddc7c2">DWRITE_SCRIPT_ANALYSIS</a></b>

The script for a run of text returned
    from <a href="https://msdn.microsoft.com/e681f7c8-7d87-454b-a7b6-6c3fe38b0f92">IDWriteTextAnalyzer::AnalyzeScript</a>.


### -param scriptProperties [out]

Type: <b><a href="https://msdn.microsoft.com/5210C04E-618B-4FE9-A6FC-6F0FF17A64D5">DWRITE_SCRIPT_PROPERTIES</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/5210C04E-618B-4FE9-A6FC-6F0FF17A64D5">DWRITE_SCRIPT_PROPERTIES</a> structure that describes info for the script.


## -returns



Type: <b>HRESULT</b>

Returns properties for the given script. If the script is invalid,
    it returns generic properties for the unknown script and E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>
 

 

