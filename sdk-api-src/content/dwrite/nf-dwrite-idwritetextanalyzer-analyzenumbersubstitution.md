---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeNumberSubstitution
title: IDWriteTextAnalyzer::AnalyzeNumberSubstitution
author: windows-sdk-content
description: Analyzes a text range for spans where number substitution is applicable, reading attributes from the source and reporting substitutable ranges to the sink callback SetNumberSubstitution.
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeNumberSubstitution.htm
tech.root: DirectWrite
ms.assetid: 1cd53f79-5bbc-4a70-b66a-b807fe163a98
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AnalyzeNumberSubstitution, AnalyzeNumberSubstitution method [Direct Write], AnalyzeNumberSubstitution method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeNumberSubstitution method, IDWriteTextAnalyzer.AnalyzeNumberSubstitution, IDWriteTextAnalyzer::AnalyzeNumberSubstitution, directwrite.IDWriteTextAnalyzer_AnalyzeNumberSubstitution, dwrite/IDWriteTextAnalyzer::AnalyzeNumberSubstitution
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
 - IDWriteTextAnalyzer.AnalyzeNumberSubstitution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer::AnalyzeNumberSubstitution


## -description


 Analyzes a text range for spans where number substitution is applicable,
     reading attributes from the source and reporting substitutable ranges
     to the sink callback <a href="https://msdn.microsoft.com/09b00b49-702e-4cef-bf1c-397c5d572513">SetNumberSubstitution</a>.


## -parameters




### -param analysisSource

Type: <b><a href="https://msdn.microsoft.com/7e2a523d-9191-4f99-9e73-a7955c432126">IDWriteTextAnalysisSource</a>*</b>

The source object to analyze.


### -param textPosition

Type: <b>UINT32</b>

The starting position within the source object.


### -param textLength

Type: <b>UINT32</b>

The length to analyze.


### -param analysisSink

Type: <b><a href="https://msdn.microsoft.com/1fd2ca46-006c-4b01-8258-6c24f4be1641">IDWriteTextAnalysisSink</a>*</b>

A pointer to the sink callback object that receives the text analysis.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Although the function can handle multiple ranges of differing number
     substitutions, the text ranges should not arbitrarily split the
     middle of numbers. Otherwise, it will treat the numbers separately
     and will not translate any intervening punctuation.




## -see-also




<a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>
 

 

