---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation
title: IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation (dwrite_1.h)
author: windows-sdk-content
description: Analyzes a text range for script orientation, reading text and attributes from the source and reporting results to the sink callback SetGlyphOrientation.
old-location: directwrite\idwritetextanalyzer1_analyzeverticalglyphorientation.htm
tech.root: DirectWrite
ms.assetid: E89C7E50-9EDA-4AC9-9FC0-B70E493ED1B4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AnalyzeVerticalGlyphOrientation, AnalyzeVerticalGlyphOrientation method [Direct Write], AnalyzeVerticalGlyphOrientation method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],AnalyzeVerticalGlyphOrientation method, IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation, IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation, directwrite.idwritetextanalyzer1_analyzeverticalglyphorientation, dwrite_1/IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation
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
 - IDWriteTextAnalyzer1.AnalyzeVerticalGlyphOrientation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer1::AnalyzeVerticalGlyphOrientation


## -description


Analyzes a text range for script orientation, reading text and
    attributes from the source and reporting results to the sink callback <a href="https://msdn.microsoft.com/81BD4C36-273B-4C28-A89E-88BABCAD511A">SetGlyphOrientation</a>.


## -parameters




### -param analysisSource

Type: <b><a href="https://msdn.microsoft.com/CFB9DB16-1F0B-409F-97BC-BB4B693AB3D6">IDWriteTextAnalysisSource1</a>*</b>

Source object to analyze.


### -param textPosition

Type: <b>UINT32</b>

Starting position within the source object.


### -param textLength

Type: <b>UINT32</b>

Length to analyze.


### -param analysisSink

Type: <b><a href="https://msdn.microsoft.com/46882D89-CD59-4C4F-A8BD-1ABC8B8C5C4B">IDWriteTextAnalysisSink1</a>*</b>

Length to analyze.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>
 

 

