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

# _PDH_TIME_INFO structure


## -description



			The 
<b>PDH_TIME_INFO</b> structure contains information on time intervals as applied to the sampling of performance data.
		


## -struct-fields




### -field StartTime

Starting time of the sample interval, in local <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.
					


### -field EndTime

Ending time of the sample interval, in local <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.


### -field SampleCount

Number of samples collected during the interval.


## -see-also




<a href="https://msdn.microsoft.com/ed0e100e-9f82-48c0-b4bb-72820c5eeaa8">PdhSetQueryTimeRange</a>
 

 

