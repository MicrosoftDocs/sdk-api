---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoStopRingOnOffHook
title: ITAutomatedPhoneControl::put_AutoStopRingOnOffHook
author: windows-sdk-content
description: The put_AutoStopRingOnOffHook method sets the AutoStopRingOnOffHook property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to ITAutomatedPhoneControl::StopRinger).
old-location: tapi3\itautomatedphonecontrol_put_autostopringonoffhook.htm
tech.root: tapi
ms.assetid: 114e17e2-63e7-47f9-8ae7-1c7e452376f6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoStopRingOnOffHook method, ITAutomatedPhoneControl.put_AutoStopRingOnOffHook, ITAutomatedPhoneControl::put_AutoStopRingOnOffHook, _tapi3_itautomatedphonecontrol_put_autostopringonoffhook, put_AutoStopRingOnOffHook, put_AutoStopRingOnOffHook method [TAPI 2.2], put_AutoStopRingOnOffHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autostopringonoffhook, tapi3if/ITAutomatedPhoneControl::put_AutoStopRingOnOffHook
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.put_AutoStopRingOnOffHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::put_AutoStopRingOnOffHook


## -description


The 
<b>put_AutoStopRingOnOffHook</b> method sets the <b>AutoStopRingOnOffHook</b> property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to 
<a href="https://msdn.microsoft.com/74829b2a-6530-40d2-8693-7c6104de7309">ITAutomatedPhoneControl::StopRinger</a>).


## -parameters




### -param fEnabled [in]

If VARIANT_TRUE, enables automatic incoming ring termination if the phone goes offhook. If VARIANT_FALSE, disables automatic incoming ring termination if the phone goes offhook. The default value is VARIANT_TRUE.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoStopRingOnOffHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopRingOnOffHook</b> property at any time. The reconfiguration takes effect the next time the phone goes offhook.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/74829b2a-6530-40d2-8693-7c6104de7309">ITAutomatedPhoneControl::StopRinger</a>



<a href="https://msdn.microsoft.com/357266e7-b103-43c1-a6af-b00347c90f51">get_AutoStopRingOnOffHook</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

