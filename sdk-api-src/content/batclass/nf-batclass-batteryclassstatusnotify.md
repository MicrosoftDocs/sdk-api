---
UID: NF:batclass.BatteryClassStatusNotify
title: BatteryClassStatusNotify function
author: windows-sdk-content
description: BatteryClassStatusNotify notifies the battery class driver of changes in battery status.
old-location: battery\batteryclassstatusnotify.htm
old-project: battery
ms.assetid: b74466e0-d900-49c6-a92e-d10a994fa948
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BatteryClassStatusNotify, BatteryClassStatusNotify function [Battery Devices], bat-rtn_3e9d25d2-bd07-419a-80a5-98fcc08faedd.xml, batclass/BatteryClassStatusNotify, battery.batteryclassstatusnotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: batclass.h
req.include-header: Batclass.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Battc.lib
 - Battc.dll
api_name:
 - BatteryClassStatusNotify
product: Windows
targetos: Windows
req.lib: Battc.lib
req.dll: 
req.irql: 
---

# BatteryClassStatusNotify function


## -description


<b>BatteryClassStatusNotify</b> notifies the battery class driver of changes in battery status.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="https://msdn.microsoft.com/0af685a5-f5c2-4448-b8b2-f5cd9ed77047">BatteryClassInitializeDevice</a>.


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
 

 

