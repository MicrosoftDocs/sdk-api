---
UID: NF:sensevts.ISensOnNow.OnBatteryPower
title: ISensOnNow::OnBatteryPower
author: windows-sdk-content
description: SENS calls the OnBatteryPower method to notify an application that a computer is using battery power.
old-location: sens\isensonnow_onbatterypower.htm
old-project: sens
ms.assetid: e8b4ce25-0d1b-401a-b16e-8eef7f292edf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISensOnNow interface [SENS],OnBatteryPower method, ISensOnNow.OnBatteryPower, ISensOnNow::OnBatteryPower, OnBatteryPower, OnBatteryPower method [SENS], OnBatteryPower method [SENS],ISensOnNow interface, _zaw_isensonnow_onbatterypower, sens.isensonnow_onbatterypower, sensevts/ISensOnNow::OnBatteryPower, syncmgr.isensonnow_onbatterypower
ms.prod: windows
ms.technology: windows-sdk
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
 - ISensOnNow.OnBatteryPower
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686510(v=VS.85).aspx">IEventSubscription</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685465(v=VS.85).aspx">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/39d483be-8dbd-41f9-9804-af9dc4535c05">ISensOnNow</a>



<a href="https://msdn.microsoft.com/78b305ef-761b-48b8-8f1b-371a75df4edb">ISensOnNow::BatteryLow</a>



<a href="https://msdn.microsoft.com/4d9e8de9-a329-4f8c-883b-e4baab04729b">ISensOnNow::OnACPower</a>
 

 

