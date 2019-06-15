---
UID: NN:sensevts.ISensOnNow
title: ISensOnNow (sensevts.h)
author: windows-sdk-content
description: The ISensOnNow interface handles AC and battery power events fired by the System Event Notification Service (SENS).
old-location: sens\isensonnow.htm
tech.root: Sens
ms.assetid: 39d483be-8dbd-41f9-9804-af9dc4535c05
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISensOnNow, ISensOnNow interface [SENS], ISensOnNow interface [SENS],described, _zaw_isensonnow, sens.isensonnow, sensevts/ISensOnNow, syncmgr.isensonnow
ms.topic: interface
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
 - ISensOnNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensOnNow interface


## -description


The 
<b>ISensOnNow</b> interface handles AC and battery power events fired by the System Event Notification Service (SENS).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensOnNow</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISensOnNow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISensOnNow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensonnow-batterylow">BatteryLow</a>
</td>
<td align="left" width="63%">
Battery power is low.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensonnow-onacpower">OnACPower</a>
</td>
<td align="left" width="63%">
Switched to AC power.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensonnow-onbatterypower">OnBatteryPower</a>
</td>
<td align="left" width="63%">
Switched to Battery power.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isensnetwork">ISensNetwork</a>
 

 

