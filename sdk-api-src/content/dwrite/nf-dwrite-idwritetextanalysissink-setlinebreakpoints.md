---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetLineBreakpoints
title: IDWriteTextAnalysisSink::SetLineBreakpoints
author: windows-sdk-content
description: Sets line-break opportunities for each character, starting from the specified position.
old-location: directwrite\idwritetextanalysissink_setlinebreakpoints.htm
old-project: DirectWrite
ms.assetid: 423f1f0e-b2bd-48b6-aa3b-c79a2b542d5d
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetLineBreakpoints method, IDWriteTextAnalysisSink.SetLineBreakpoints, IDWriteTextAnalysisSink::SetLineBreakpoints, SetLineBreakpoints, SetLineBreakpoints method [Direct Write], SetLineBreakpoints method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setlinebreakpoints, dwrite/IDWriteTextAnalysisSink::SetLineBreakpoints
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextAnalysisSink.SetLineBreakpoints
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextAnalysisSink::SetLineBreakpoints


## -description


Sets line-break opportunities for each character, starting from the specified position.


## -parameters




### -param textPosition

Type: <b>UINT32</b>

The starting text position from which to report.


### -param textLength

Type: <b>UINT32</b>

The number of UTF16 units of the reported range.


### -param lineBreakpoints [in]

Type: <b><a href="https://msdn.microsoft.com/6f2b26e9-95b3-4ac5-ba8e-7055f873d1da">DWRITE_LINE_BREAKPOINT</a>*</b>

A pointer to a structure that contains breaking conditions set for each character from the starting position to the end of the specified range.


## -returns



Type: <b>HRESULT</b>

A successful code or error code to stop analysis.




## -see-also




<a href="https://msdn.microsoft.com/1fd2ca46-006c-4b01-8258-6c24f4be1641">IDWriteTextAnalysisSink</a>
 

 

