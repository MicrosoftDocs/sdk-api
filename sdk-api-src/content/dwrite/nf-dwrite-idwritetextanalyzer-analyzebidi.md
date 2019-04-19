---
UID: NF:dwrite.IDWriteTextAnalyzer.AnalyzeBidi
title: IDWriteTextAnalyzer::AnalyzeBidi (dwrite.h)
author: windows-sdk-content
description: Analyzes a text range for script directionality, reading attributes from the source and reporting levels to the sink callback SetBidiLevel.
old-location: directwrite\IDWriteTextAnalyzer_AnalyzeBidi.htm
tech.root: DirectWrite
ms.assetid: 413d49d2-bacd-4e98-bfac-c0aea2650a7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AnalyzeBidi, AnalyzeBidi method [Direct Write], AnalyzeBidi method [Direct Write],IDWriteTextAnalyzer interface, IDWriteTextAnalyzer interface [Direct Write],AnalyzeBidi method, IDWriteTextAnalyzer.AnalyzeBidi, IDWriteTextAnalyzer::AnalyzeBidi, directwrite.IDWriteTextAnalyzer_AnalyzeBidi, dwrite/IDWriteTextAnalyzer::AnalyzeBidi
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
 - IDWriteTextAnalyzer.AnalyzeBidi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer::AnalyzeBidi


## -description


 Analyzes a text range for script directionality, reading attributes
     from the source and reporting levels to the sink callback <a href="https://msdn.microsoft.com/f51bae22-b4a0-4f72-a341-4479d66cfec5">SetBidiLevel</a>.


## -parameters




### -param analysisSource

Type: <b><a href="https://msdn.microsoft.com/7e2a523d-9191-4f99-9e73-a7955c432126">IDWriteTextAnalysisSource</a>*</b>

A pointer to a source object to analyze.


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




## -remarks



 While the function can handle multiple paragraphs, the text range
     should not arbitrarily split the middle of paragraphs. Otherwise, the
     returned levels may be wrong, because the Bidi algorithm is meant to
     apply to the paragraph as a whole.




## -see-also




<a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>
 

 

