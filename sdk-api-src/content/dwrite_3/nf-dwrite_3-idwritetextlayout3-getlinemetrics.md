---
UID: NF:dwrite_3.IDWriteTextLayout3.GetLineMetrics
title: IDWriteTextLayout3::GetLineMetrics (dwrite_3.h)
description: Retrieves properties of each line.
helpviewer_keywords: ["GetLineMetrics","GetLineMetrics method [Direct Write]","GetLineMetrics method [Direct Write]","IDWriteTextLayout3 interface","IDWriteTextLayout3 interface [Direct Write]","GetLineMetrics method","IDWriteTextLayout3.GetLineMetrics","IDWriteTextLayout3::GetLineMetrics","directwrite.idwritetextlayout3_getlinemetrics","dwrite_3/IDWriteTextLayout3::GetLineMetrics"]
old-location: directwrite\idwritetextlayout3_getlinemetrics.htm
tech.root: DirectWrite
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
ms.date: 09/10/2025
ms.keywords: GetLineMetrics, GetLineMetrics method [Direct Write], GetLineMetrics method [Direct Write],IDWriteTextLayout3 interface, IDWriteTextLayout3 interface [Direct Write],GetLineMetrics method, IDWriteTextLayout3.GetLineMetrics, IDWriteTextLayout3::GetLineMetrics, directwrite.idwritetextlayout3_getlinemetrics, dwrite_3/IDWriteTextLayout3::GetLineMetrics
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteTextLayout3::GetLineMetrics
 - dwrite_3/IDWriteTextLayout3::GetLineMetrics
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
 - IDWriteTextLayout3.GetLineMetrics
---

# IDWriteTextLayout3::GetLineMetrics


## -description

Retrieves properties of each line.

## -parameters

### -param lineMetrics [out]

The array to fill with line information.

### -param maxLineCount

The maximum size of the lineMetrics array.

### -param actualLineCount [out]

The actual size of the lineMetrics    
     array that is needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If maxLineCount is not large enough E_NOT_SUFFICIENT_BUFFER,   
     which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER),  
     is returned and actualLineCount is set to the number of lines   
     needed.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout3">IDWriteTextLayout3</a>

