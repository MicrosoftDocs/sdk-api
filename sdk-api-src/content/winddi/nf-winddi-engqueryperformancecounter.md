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

# EngQueryPerformanceCounter function


## -description


The <b>EngQueryPerformanceCounter</b> function queries the performance counter.


## -parameters




### -param pPerformanceCount [out]

Pointer to a location that receives the performance counter value, in hertz.


## -returns



None




## -remarks



<b>EngQueryPerformanceCounter</b> always returns a 64-bit integer that represents the number of ticks per second. The count begins accumulating when the system is booted.

A driver should call this routine sparingly. Frequent calls to <b>EngQueryPerformanceCounter</b> can degrade the I/O performance for the calling driver and for the system as a whole.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564996">EngQueryPerformanceFrequency</a>
 

 

