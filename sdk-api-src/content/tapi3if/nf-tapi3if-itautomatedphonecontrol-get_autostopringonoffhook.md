---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoStopRingOnOffHook
title: ITAutomatedPhoneControl::get_AutoStopRingOnOffHook
author: windows-sdk-content
description: The get_AutoStopRingOnOffHook method retrieves the current value of the AutoStopRingOnOffHook property.
old-location: tapi3\itautomatedphonecontrol_get_autostopringonoffhook.htm
old-project: tapi
ms.assetid: 357266e7-b103-43c1-a6af-b00347c90f51
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoStopRingOnOffHook method, ITAutomatedPhoneControl.get_AutoStopRingOnOffHook, ITAutomatedPhoneControl::get_AutoStopRingOnOffHook, _tapi3_itautomatedphonecontrol_get_autostopringonoffhook, get_AutoStopRingOnOffHook, get_AutoStopRingOnOffHook method [TAPI 2.2], get_AutoStopRingOnOffHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autostopringonoffhook, tapi3if/ITAutomatedPhoneControl::get_AutoStopRingOnOffHook
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.get_AutoStopRingOnOffHook
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

