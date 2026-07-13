---
UID: NF:dwrite.IDWriteTextLayout.GetMetrics
title: IDWriteTextLayout::GetMetrics (dwrite.h)
description: Retrieves overall metrics for the formatted string. (IDWriteTextLayout.GetMetrics)
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetMetrics method","IDWriteTextLayout.GetMetrics","IDWriteTextLayout::GetMetrics","directwrite.IDWriteTextLayout_GetMetrics","dwrite/IDWriteTextLayout::GetMetrics"]
old-location: directwrite\IDWriteTextLayout_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: cbfafccc-f66c-4b75-9540-e393ee203859
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetMetrics method, IDWriteTextLayout.GetMetrics, IDWriteTextLayout::GetMetrics, directwrite.IDWriteTextLayout_GetMetrics, dwrite/IDWriteTextLayout::GetMetrics
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
 - IDWriteTextLayout::GetMetrics
 - dwrite/IDWriteTextLayout::GetMetrics
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
 - IDWriteTextLayout.GetMetrics
---

# IDWriteTextLayout::GetMetrics


## -description

 Retrieves overall metrics for the formatted string.

## -parameters

### -param textMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics">DWRITE_TEXT_METRICS</a>*</b>

When this method returns, contains the measured distances of text and associated content after being formatted.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

