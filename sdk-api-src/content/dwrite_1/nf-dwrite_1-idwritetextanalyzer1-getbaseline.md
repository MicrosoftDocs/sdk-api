---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetBaseline
title: IDWriteTextAnalyzer1::GetBaseline (dwrite_1.h)
author: windows-sdk-content
description: Retrieves the given baseline from the font.
old-location: directwrite\idwritetextanalyzer1_getbaseline.htm
tech.root: DirectWrite
ms.assetid: 5ACD5075-BD96-41FC-AE36-8D5D03F2EB54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBaseline, GetBaseline method [Direct Write], GetBaseline method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetBaseline method, IDWriteTextAnalyzer1.GetBaseline, IDWriteTextAnalyzer1::GetBaseline, directwrite.idwritetextanalyzer1_getbaseline, dwrite_1/IDWriteTextAnalyzer1::GetBaseline
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
 - IDWriteTextAnalyzer1.GetBaseline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer1::GetBaseline


## -description


Retrieves the given baseline from the font.


## -parameters




### -param fontFace

Type: <b><a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace</a>*</b>

The font face to read.


### -param baseline

Type: <b><a href="https://msdn.microsoft.com/A5708481-255B-4777-B689-B61208E3910E">DWRITE_BASELINE</a></b>

A <a href="https://msdn.microsoft.com/A5708481-255B-4777-B689-B61208E3910E">DWRITE_BASELINE</a>-typed value that specifies the baseline of interest.


### -param isVertical

Type: <b>BOOL</b>

Whether the baseline is vertical or horizontal.


### -param isSimulationAllowed

Type: <b>BOOL</b>

Simulate the baseline if it is missing in the font.


### -param scriptAnalysis

Type: <b><a href="https://msdn.microsoft.com/dafda5f6-39aa-4577-9213-898bdeddc7c2">DWRITE_SCRIPT_ANALYSIS</a></b>

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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the baseline does not exist in the font, it is not considered an
    error, but the function will return exists = false. You may then use
    heuristics to calculate the missing base, or, if the flag
    simulationAllowed is true, the function will compute a reasonable
    approximation for you.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>
 

 

