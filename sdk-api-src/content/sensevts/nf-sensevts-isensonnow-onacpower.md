---
UID: NF:sensevts.ISensOnNow.OnACPower
title: ISensOnNow::OnACPower (sensevts.h)
author: windows-sdk-content
description: SENS calls the OnACPower method to notify your application that the computer is using AC power.
old-location: sens\isensonnow_onacpower.htm
tech.root: Sens
ms.assetid: 4d9e8de9-a329-4f8c-883b-e4baab04729b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISensOnNow interface [SENS],OnACPower method, ISensOnNow.OnACPower, ISensOnNow::OnACPower, OnACPower, OnACPower method [SENS], OnACPower method [SENS],ISensOnNow interface, _zaw_isensonnow_onacpower, sens.isensonnow_onacpower, sensevts/ISensOnNow::OnACPower, syncmgr.isensonnow_onacpower
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
 - ISensOnNow.OnACPower
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensOnNow::OnACPower


## -description


SENS calls the 
<b>OnACPower</b> method to notify your application that the computer is using AC power.


## -parameters






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
Method returned successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify your application that AC power has been activated.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686510(v=VS.85).aspx">IEventSubscription</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685465(v=VS.85).aspx">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/39d483be-8dbd-41f9-9804-af9dc4535c05">ISensOnNow</a>



<a href="https://msdn.microsoft.com/e8b4ce25-0d1b-401a-b16e-8eef7f292edf">ISensOnNow::OnBatteryPower</a>
 

 

