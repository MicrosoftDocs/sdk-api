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

# ITAutomatedPhoneControl::get_AutoStopRingOnOffHook


## -description


The 
<b>get_AutoStopRingOnOffHook</b> method retrieves the current value of the <b>AutoStopRingOnOffHook</b> property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to 
<a href="https://msdn.microsoft.com/74829b2a-6530-40d2-8693-7c6104de7309">ITAutomatedPhoneControl::StopRinger</a>).


## -parameters




### -param pfEnabled [out]

If VARIANT_TRUE, automatic incoming ring termination when the phone goes offhook is enabled. If VARIANT_FALSE, automatic incoming ring termination when the phone goes offhook is disabled.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoStopRingOnOffHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopRingOnOffHook</b> property at any time. The reconfiguration takes effect the next time the phone goes offhook.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/74829b2a-6530-40d2-8693-7c6104de7309">ITAutomatedPhoneControl::StopRinger</a>



<a href="https://msdn.microsoft.com/114e17e2-63e7-47f9-8ae7-1c7e452376f6">put_AutoStopRingOnOffHook</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

