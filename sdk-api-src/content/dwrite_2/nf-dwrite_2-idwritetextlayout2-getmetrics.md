---
UID: NF:dwrite_2.IDWriteTextLayout2.GetMetrics
title: IDWriteTextLayout2::GetMetrics
author: windows-sdk-content
description: Retrieves overall metrics for the formatted string.
old-location: directwrite\idwritetextlayout2_getmetrics.htm
tech.root: DirectWrite
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteTextLayout2 interface, IDWriteTextLayout2 interface [Direct Write],GetMetrics method, IDWriteTextLayout2.GetMetrics, IDWriteTextLayout2::GetMetrics, directwrite.idwritetextlayout2_getmetrics, dwrite_2/IDWriteTextLayout2::GetMetrics
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout2::GetMetrics


## -description


 Retrieves overall metrics for the formatted string.


## -parameters




### -param textMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/1C374FD8-8BDC-4719-921F-2E14A919E7EF">DWRITE_TEXT_METRICS1</a>*</b>

When this method returns, contains the measured distances of text and associated content after being formatted.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/034D795B-016A-401E-AD75-D5B0D1E87806">IDWriteTextLayout2</a>
 

 

