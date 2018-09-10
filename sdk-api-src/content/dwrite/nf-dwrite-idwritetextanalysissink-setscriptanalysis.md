---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetScriptAnalysis
title: IDWriteTextAnalysisSink::SetScriptAnalysis
author: windows-sdk-content
description: Reports script analysis for the specified text range.
old-location: directwrite\idwritetextanalysissink_setscriptanalysis.htm
tech.root: DirectWrite
ms.assetid: beae0420-b244-4c87-a3cb-a1b34562c3ed
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetScriptAnalysis method, IDWriteTextAnalysisSink.SetScriptAnalysis, IDWriteTextAnalysisSink::SetScriptAnalysis, SetScriptAnalysis, SetScriptAnalysis method [Direct Write], SetScriptAnalysis method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setscriptanalysis, dwrite/IDWriteTextAnalysisSink::SetScriptAnalysis
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
 - IDWriteTextAnalysisSink.SetScriptAnalysis
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b>const <a href="https://msdn.microsoft.com/dafda5f6-39aa-4577-9213-898bdeddc7c2">DWRITE_SCRIPT_ANALYSIS</a>*</b>

A pointer to a structure that contains a zero-based index representation of a writing system script and a value indicating whether additional shaping of text is required.


## -returns



Type: <b>HRESULT</b>

A successful code or error code to stop analysis.




## -see-also




<a href="https://msdn.microsoft.com/1fd2ca46-006c-4b01-8258-6c24f4be1641">IDWriteTextAnalysisSink</a>
 

 

