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

# BatteryClassStatusNotify function


## -description


<b>BatteryClassStatusNotify</b> notifies the battery class driver of changes in battery status.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>.


## -returns



<b>BatteryClassStatusNotify</b> returns STATUS_SUCCESS.




## -remarks



Battery miniclass drivers must call <b>BatteryClassStatusNotify</b> whenever any of the following occur:

<ul>
<li>
The battery goes online or offline.

</li>
<li>
The battery's capacity becomes critically low.

</li>
<li>
The battery's power state changes; that is, the battery starts or stops charging or discharging.

</li>
<li>
The battery's capacity or power state deviates from the criteria set by a previous call to <a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a>. 

</li>
</ul>
The battery class driver queues status requests internally. If any such requests are pending when the miniclass driver calls <b>BatteryClassStatusNotify</b>, the class driver immediately calls the miniclass driver's <a href="https://msdn.microsoft.com/04811f63-8a57-4b39-84c5-c9b7f803c057">BatteryMiniQueryStatus</a> routine.




## -see-also




<a href="https://msdn.microsoft.com/04811f63-8a57-4b39-84c5-c9b7f803c057">BatteryMiniQueryStatus</a>



<a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a>
 

 

