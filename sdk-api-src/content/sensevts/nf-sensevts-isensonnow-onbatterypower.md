---
UID: NF:sensevts.ISensOnNow.OnBatteryPower
title: ISensOnNow::OnBatteryPower (sensevts.h)
description: SENS calls the OnBatteryPower method to notify an application that a computer is using battery power.
helpviewer_keywords: ["ISensOnNow interface [SENS]","OnBatteryPower method","ISensOnNow.OnBatteryPower","ISensOnNow::OnBatteryPower","OnBatteryPower","OnBatteryPower method [SENS]","OnBatteryPower method [SENS]","ISensOnNow interface","_zaw_isensonnow_onbatterypower","sens.isensonnow_onbatterypower","sensevts/ISensOnNow::OnBatteryPower","syncmgr.isensonnow_onbatterypower"]
old-location: sens\isensonnow_onbatterypower.htm
tech.root: Sens
ms.assetid: e8b4ce25-0d1b-401a-b16e-8eef7f292edf
ms.date: 12/05/2018
ms.keywords: ISensOnNow interface [SENS],OnBatteryPower method, ISensOnNow.OnBatteryPower, ISensOnNow::OnBatteryPower, OnBatteryPower, OnBatteryPower method [SENS], OnBatteryPower method [SENS],ISensOnNow interface, _zaw_isensonnow_onbatterypower, sens.isensonnow_onbatterypower, sensevts/ISensOnNow::OnBatteryPower, syncmgr.isensonnow_onbatterypower
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
 - ISensOnNow::OnBatteryPower
 - sensevts/ISensOnNow::OnBatteryPower
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
 - ISensOnNow.OnBatteryPower
---

# ISensOnNow::OnBatteryPower


## -description

SENS calls the 
<b>OnBatteryPower</b> method to notify an application that a computer is using battery power.

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



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensonnow-batterylow">ISensOnNow::BatteryLow</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensonnow-onacpower">ISensOnNow::OnACPower</a>