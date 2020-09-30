---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetLineBreakpoints
title: IDWriteTextAnalysisSink::SetLineBreakpoints (dwrite.h)
description: Sets line-break opportunities for each character, starting from the specified position.
helpviewer_keywords: ["IDWriteTextAnalysisSink interface [Direct Write]","SetLineBreakpoints method","IDWriteTextAnalysisSink.SetLineBreakpoints","IDWriteTextAnalysisSink::SetLineBreakpoints","SetLineBreakpoints","SetLineBreakpoints method [Direct Write]","SetLineBreakpoints method [Direct Write]","IDWriteTextAnalysisSink interface","directwrite.idwritetextanalysissink_setlinebreakpoints","dwrite/IDWriteTextAnalysisSink::SetLineBreakpoints"]
old-location: directwrite\idwritetextanalysissink_setlinebreakpoints.htm
tech.root: DirectWrite
ms.assetid: 423f1f0e-b2bd-48b6-aa3b-c79a2b542d5d
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetLineBreakpoints method, IDWriteTextAnalysisSink.SetLineBreakpoints, IDWriteTextAnalysisSink::SetLineBreakpoints, SetLineBreakpoints, SetLineBreakpoints method [Direct Write], SetLineBreakpoints method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setlinebreakpoints, dwrite/IDWriteTextAnalysisSink::SetLineBreakpoints
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextAnalysisSink::SetLineBreakpoints
 - dwrite/IDWriteTextAnalysisSink::SetLineBreakpoints
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextAnalysisSink.SetLineBreakpoints
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

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint">DWRITE_LINE_BREAKPOINT</a>*</b>

A pointer to a structure that contains breaking conditions set for each character from the starting position to the end of the specified range.

## -returns

Type: <b>HRESULT</b>

A successful code or error code to stop analysis.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>

