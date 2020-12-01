---
UID: NF:sensevts.ISensOnNow.BatteryLow
title: ISensOnNow::BatteryLow (sensevts.h)
description: The BatteryLow method notifies an application that battery power is low. SENS calls the BatteryLow method to notify an application that a computer is using battery power.
helpviewer_keywords: ["BatteryLow","BatteryLow method [SENS]","BatteryLow method [SENS]","ISensOnNow interface","ISensOnNow interface [SENS]","BatteryLow method","ISensOnNow.BatteryLow","ISensOnNow::BatteryLow","_zaw_isensonnow_batterylow","sens.isensonnow_batterylow","sensevts/ISensOnNow::BatteryLow","syncmgr.isensonnow_batterylow"]
old-location: sens\isensonnow_batterylow.htm
tech.root: Sens
ms.assetid: 78b305ef-761b-48b8-8f1b-371a75df4edb
ms.date: 12/05/2018
ms.keywords: BatteryLow, BatteryLow method [SENS], BatteryLow method [SENS],ISensOnNow interface, ISensOnNow interface [SENS],BatteryLow method, ISensOnNow.BatteryLow, ISensOnNow::BatteryLow, _zaw_isensonnow_batterylow, sens.isensonnow_batterylow, sensevts/ISensOnNow::BatteryLow, syncmgr.isensonnow_batterylow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensOnNow::BatteryLow
 - sensevts/ISensOnNow::BatteryLow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensOnNow.BatteryLow
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

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isensonnow">ISensOnNow</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensonnow-onbatterypower">ISensOnNow::OnBatteryPower</a>