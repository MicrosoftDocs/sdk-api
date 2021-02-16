---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetBidiLevel
title: IDWriteTextAnalysisSink::SetBidiLevel (dwrite.h)
description: Sets a bidirectional level on the range, which is called once per run change (either explicit or resolved implicit).
helpviewer_keywords: ["IDWriteTextAnalysisSink interface [Direct Write]","SetBidiLevel method","IDWriteTextAnalysisSink.SetBidiLevel","IDWriteTextAnalysisSink::SetBidiLevel","SetBidiLevel","SetBidiLevel method [Direct Write]","SetBidiLevel method [Direct Write]","IDWriteTextAnalysisSink interface","directwrite.idwritetextanalysissink_setbidilevel","dwrite/IDWriteTextAnalysisSink::SetBidiLevel"]
old-location: directwrite\idwritetextanalysissink_setbidilevel.htm
tech.root: DirectWrite
ms.assetid: f51bae22-b4a0-4f72-a341-4479d66cfec5
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetBidiLevel method, IDWriteTextAnalysisSink.SetBidiLevel, IDWriteTextAnalysisSink::SetBidiLevel, SetBidiLevel, SetBidiLevel method [Direct Write], SetBidiLevel method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setbidilevel, dwrite/IDWriteTextAnalysisSink::SetBidiLevel
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
 - IDWriteTextAnalysisSink::SetBidiLevel
 - dwrite/IDWriteTextAnalysisSink::SetBidiLevel
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
 - IDWriteTextAnalysisSink.SetBidiLevel
---

# IDWriteTextAnalysisSink::SetBidiLevel


## -description

Sets a bidirectional level on the range, which is  called once per  run change (either explicit or resolved implicit).

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The starting position from which to report.

### -param textLength

Type: <b>UINT32</b>

The number of UTF16 units of the reported range.

### -param explicitLevel

Type: <b>UINT8</b>

The explicit level from the paragraph reading direction and any embedded control codes RLE/RLO/LRE/LRO/PDF, which is determined before any additional rules.

### -param resolvedLevel

Type: <b>UINT8</b>

The final implicit level considering the
         explicit level and characters' natural directionality, after all
         Bidi rules have been applied.

## -returns

Type: <b>HRESULT</b>

A successful code or error code to stop analysis.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>

