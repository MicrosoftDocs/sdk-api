---
UID: NF:sensevts.ISensOnNow.BatteryLow
title: ISensOnNow::BatteryLow
author: windows-sdk-content
description: The BatteryLow method notifies an application that battery power is low. SENS calls the BatteryLow method to notify an application that a computer is using battery power.
old-location: sens\isensonnow_batterylow.htm
tech.root: Sens
ms.assetid: 78b305ef-761b-48b8-8f1b-371a75df4edb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BatteryLow, BatteryLow method [SENS], BatteryLow method [SENS],ISensOnNow interface, ISensOnNow interface [SENS],BatteryLow method, ISensOnNow.BatteryLow, ISensOnNow::BatteryLow, _zaw_isensonnow_batterylow, sens.isensonnow_batterylow, sensevts/ISensOnNow::BatteryLow, syncmgr.isensonnow_batterylow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sensevts.h
req.include-header: 
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
req.type-library: Sensevts.tlb
req.lib: 
req.dll: Sens.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensOnNow.BatteryLow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sensevts.h
: 
- ISensOnNow.BatteryLow
: 
---

# ISensOnNow::BatteryLow


## -description


The 
<b>BatteryLow</b> method notifies an application that battery power is low. SENS calls the <b>BatteryLow</b> method to notify an application that a computer is using battery power. 

Low battery power is signaled when a system is on battery power and the battery is low according to the same logic used by the Advanced Power Management (APM) event PBT_APMBATTERYLOW. This event is broadcast when a system APM BIOS sends an APM battery low notification.

Some APM BIOS implementations do not provide notifications when batteries are low, which means that this event may never be broadcast on some computers.


## -parameters




### -param dwBatteryLifePercent [in]

The percent of battery power that remains.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method returns successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify an application that a computer is using battery power. The remaining percentage of battery power is specified.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686510(v=VS.85).aspx">IEventSubscription</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685465(v=VS.85).aspx">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/39d483be-8dbd-41f9-9804-af9dc4535c05">ISensOnNow</a>



<a href="https://msdn.microsoft.com/e8b4ce25-0d1b-401a-b16e-8eef7f292edf">ISensOnNow::OnBatteryPower</a>
 

 

