---
UID: NN:sensevts.ISensOnNow
title: ISensOnNow
author: windows-sdk-content
description: The ISensOnNow interface handles AC and battery power events fired by the System Event Notification Service (SENS).
old-location: sens\isensonnow.htm
old-project: Sens
ms.assetid: 39d483be-8dbd-41f9-9804-af9dc4535c05
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISensOnNow, ISensOnNow interface [SENS], ISensOnNow interface [SENS],described, _zaw_isensonnow, sens.isensonnow, sensevts/ISensOnNow, syncmgr.isensonnow
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: QOCINFO, *LPQOCINFO
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
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISensOnNow interface


## -description


The 
<b>ISensOnNow</b> interface handles AC and battery power events fired by the System Event Notification Service (SENS).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensOnNow</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISensOnNow</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/78b305ef-761b-48b8-8f1b-371a75df4edb">BatteryLow</a>
</td>
<td align="left" width="63%">
Battery power is low.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d9e8de9-a329-4f8c-883b-e4baab04729b">OnACPower</a>
</td>
<td align="left" width="63%">
Switched to AC power.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8b4ce25-0d1b-401a-b16e-8eef7f292edf">OnBatteryPower</a>
</td>
<td align="left" width="63%">
Switched to Battery power.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/77c02510-6386-4f6d-af1a-e7337f5d347d">ISensLogon</a>



<a href="https://msdn.microsoft.com/1cea5dff-13ea-4afb-84ac-7b8df4f55fc8">ISensNetwork</a>
 

 

