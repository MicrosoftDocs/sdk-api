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

# EngQueryPerformanceFrequency function


## -description


The <b>EngQueryPerformanceFrequency</b> function queries the frequency of the performance counter.


## -parameters




### -param pFrequency [out]

Pointer to a location that receives the performance counter frequency.


## -returns



None




## -remarks



The resolution of the timer is 1/<i>x</i>, where <i>x</i> is the value returned in the location to which <i>pFrequency</i> points. For example, if the value returned in <i>pFrequency</i> is 2 million, each tick is 1/2 millionth of a second. Each 1/<i>x</i> millionth increment of the count corresponds to one second of elapsed time.

A driver should call this routine sparingly. Frequent calls to <b>EngQueryPerformanceFrequency</b> can degrade the I/O performance for the calling driver and for the system as a whole.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564994">EngQueryPerformanceCounter</a>
 

 

