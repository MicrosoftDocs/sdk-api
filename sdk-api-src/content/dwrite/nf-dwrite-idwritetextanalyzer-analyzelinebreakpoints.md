---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeLineBreakpoints
title: IDWriteTextAnalyzer::AnalyzeLineBreakpoints
author: windows-sdk-content
description: Analyzes a text range for potential breakpoint opportunities, reading attributes from the source and reporting breakpoint opportunities to the sink callback SetLineBreakpoints.
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeLineBreakpoints.htm
tech.root: DirectWrite
ms.assetid: 6c676065-0226-456c-b8c4-10752a8daec8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AnalyzeLineBreakpoints, AnalyzeLineBreakpoints method [Direct Write], AnalyzeLineBreakpoints method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeLineBreakpoints method, IDWriteTextAnalyzer.AnalyzeLineBreakpoints, IDWriteTextAnalyzer::AnalyzeLineBreakpoints, directwrite.IDWriteTextAnalyzer_AnalyzeLineBreakpoints, dwrite/IDWriteTextAnalyzer::AnalyzeLineBreakpoints
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
 - IDWriteTextAnalyzer.AnalyzeLineBreakpoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer::AnalyzeLineBreakpoints


## -description


 Analyzes a text range for potential breakpoint opportunities, reading
     attributes from the source and reporting breakpoint opportunities to
     the sink callback <a href="https://msdn.microsoft.com/423f1f0e-b2bd-48b6-aa3b-c79a2b542d5d">SetLineBreakpoints</a>.


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

A pointer to the  sink callback object that receives the text analysis.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Although the function can handle multiple paragraphs, the text range
     should not arbitrarily split the middle of paragraphs, unless the
     specified text span is considered a whole unit. Otherwise, the
     returned properties for the first and last characters will
     inappropriately allow breaks.




## -see-also




<a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>
 

 

