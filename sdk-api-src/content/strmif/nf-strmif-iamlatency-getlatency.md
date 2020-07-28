---
UID: NF:strmif.IAMLatency.GetLatency
title: IAMLatency::GetLatency (strmif.h)
description: The GetLatency method retrieves the expected latency associated with this filter.
helpviewer_keywords: ["GetLatency","GetLatency method [DirectShow]","GetLatency method [DirectShow]","IAMLatency interface","IAMLatency interface [DirectShow]","GetLatency method","IAMLatency.GetLatency","IAMLatency::GetLatency","IAMLatencyGetLatency","dshow.iamlatency_getlatency","strmif/IAMLatency::GetLatency"]
old-location: dshow\iamlatency_getlatency.htm
tech.root: dshow
ms.assetid: 5c5f6a73-d216-4a26-958e-ce8055575d17
ms.date: 12/05/2018
ms.keywords: GetLatency, GetLatency method [DirectShow], GetLatency method [DirectShow],IAMLatency interface, IAMLatency interface [DirectShow],GetLatency method, IAMLatency.GetLatency, IAMLatency::GetLatency, IAMLatencyGetLatency, dshow.iamlatency_getlatency, strmif/IAMLatency::GetLatency
f1_keywords:
- strmif/IAMLatency.GetLatency
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMLatency.GetLatency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMLatency::GetLatency


## -description



The <code>GetLatency</code> method retrieves the expected latency associated with this filter.




## -parameters




### -param prtLatency [in]

Pointer to a variable that receives the latency in 100-nanosecond units.


## -returns



Returns S_OK if successsful, or an error code otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamlatency">IAMLatency Interface</a>
 

 

