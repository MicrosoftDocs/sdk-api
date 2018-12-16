---
UID: NF:dwrite.IDWriteTextLayout.GetMetrics
title: IDWriteTextLayout::GetMetrics
author: windows-sdk-content
description: Retrieves overall metrics for the formatted string.
old-location: directwrite\IDWriteTextLayout_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: cbfafccc-f66c-4b75-9540-e393ee203859
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetMetrics method, IDWriteTextLayout.GetMetrics, IDWriteTextLayout::GetMetrics, directwrite.IDWriteTextLayout_GetMetrics, dwrite/IDWriteTextLayout::GetMetrics
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
 - IDWriteTextLayout.GetMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetMetrics


## -description


 Retrieves overall metrics for the formatted string.


## -parameters




### -param textMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/4524ace3-fca6-4daf-9ecb-516771e53fc9">DWRITE_TEXT_METRICS</a>*</b>

When this method returns, contains the measured distances of text and associated content after being formatted.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

