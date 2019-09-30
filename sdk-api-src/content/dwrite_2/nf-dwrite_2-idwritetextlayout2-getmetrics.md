---
UID: NF:dwrite_2.IDWriteTextLayout2.GetMetrics
title: IDWriteTextLayout2::GetMetrics (dwrite_2.h)
author: windows-sdk-content
description: Retrieves overall metrics for the formatted string.
old-location: directwrite\idwritetextlayout2_getmetrics.htm
tech.root: DirectWrite
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteTextLayout2 interface, IDWriteTextLayout2 interface [Direct Write],GetMetrics method, IDWriteTextLayout2.GetMetrics, IDWriteTextLayout2::GetMetrics, directwrite.idwritetextlayout2_getmetrics, dwrite_2/IDWriteTextLayout2::GetMetrics
ms.topic: method
f1_keywords: 
 - "dwrite_2/IDWriteTextLayout2.GetMetrics"
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextLayout2.GetMetrics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout2::GetMetrics


## -description


 Retrieves overall metrics for the formatted string.


## -parameters




### -param textMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1">DWRITE_TEXT_METRICS1</a>*</b>

When this method returns, contains the measured distances of text and associated content after being formatted.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/DirectWrite/idwritetextlayout2">IDWriteTextLayout2</a>
 

 

