---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAMClockAdjust::SetClockDelta


## -description



The <code>SetClockDelta</code> method adjusts the clock time.




## -parameters




### -param rtDelta [in]

Specifies the amount by which to adjust the clock, as a <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> value. A positive value moves the clock forward, and a negative value moves the clock backward.


## -returns



Returns S_OK or an <b>HRESULT</b> error code.




## -remarks



The time values returned by <a href="https://msdn.microsoft.com/1fcf8b8a-f449-4f42-8061-cc4116867d9d">IReferenceClock::GetTime</a> are monotonically increasing. If you set the clock back, <b>GetTime</b> continues to report the old time until the internal clock catches up.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e24105a5-711a-498a-a07c-842307602613">IAMClockAdjust Interface</a>
 

 

