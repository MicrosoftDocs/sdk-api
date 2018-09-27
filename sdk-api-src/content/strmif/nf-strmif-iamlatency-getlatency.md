---
UID: NF:strmif.IAMLatency.GetLatency
title: IAMLatency::GetLatency
author: windows-sdk-content
description: The GetLatency method retrieves the expected latency associated with this filter.
old-location: dshow\iamlatency_getlatency.htm
tech.root: DirectShow
ms.assetid: 5c5f6a73-d216-4a26-958e-ce8055575d17
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetLatency, GetLatency method [DirectShow], GetLatency method [DirectShow],IAMLatency interface, IAMLatency interface [DirectShow],GetLatency method, IAMLatency.GetLatency, IAMLatency::GetLatency, IAMLatencyGetLatency, dshow.iamlatency_getlatency, strmif/IAMLatency::GetLatency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/83384ef6-40d6-4d37-866d-6059dc5d7542">IAMLatency Interface</a>
 

 

