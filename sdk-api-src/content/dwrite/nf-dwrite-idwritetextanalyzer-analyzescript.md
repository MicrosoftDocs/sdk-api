---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeScript
title: IDWriteTextAnalyzer::AnalyzeScript
author: windows-sdk-content
description: Analyzes a text range for script boundaries, reading text attributes from the source and reporting the Unicode script ID to the sink callback SetScript.
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeScript.htm
tech.root: DirectWrite
ms.assetid: e681f7c8-7d87-454b-a7b6-6c3fe38b0f92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AnalyzeScript, AnalyzeScript method [Direct Write], AnalyzeScript method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeScript method, IDWriteTextAnalyzer.AnalyzeScript, IDWriteTextAnalyzer::AnalyzeScript, directwrite.IDWriteTextAnalyzer_AnalyzeScript, dwrite/IDWriteTextAnalyzer::AnalyzeScript
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextAnalyzer.AnalyzeScript
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer::AnalyzeScript


## -description


 Analyzes a text range for script boundaries, reading text attributes
     from the source and reporting the Unicode script ID to the sink 
     callback <a href="https://msdn.microsoft.com/beae0420-b244-4c87-a3cb-a1b34562c3ed">SetScript</a>.


## -parameters




### -param analysisSource

Type: <b><a href="https://msdn.microsoft.com/7e2a523d-9191-4f99-9e73-a7955c432126">IDWriteTextAnalysisSource</a>*</b>

A pointer to the source object to analyze.


### -param textPosition

Type: <b>UINT32</b>

The starting text position within the source object.


### -param textLength

Type: <b>UINT32</b>

The text length to analyze.


### -param analysisSink

Type: <b><a href="https://msdn.microsoft.com/1fd2ca46-006c-4b01-8258-6c24f4be1641">IDWriteTextAnalysisSink</a>*</b>

A pointer to the sink callback object that receives the text analysis.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>
 

 

