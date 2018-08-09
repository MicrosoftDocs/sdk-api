---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook
title: ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook
author: windows-sdk-content
description: The get_AutoStopTonesOnOnHook method retrieves the current value of the AutoStopTonesOnOnHook property.
old-location: tapi3\itautomatedphonecontrol_get_autostoptonesononhook.htm
old-project: tapi
ms.assetid: 2ece8d7a-b280-42b6-9f51-d88650488699
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoStopTonesOnOnHook method, ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook, ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook, _tapi3_itautomatedphonecontrol_get_autostoptonesononhook, get_AutoStopTonesOnOnHook, get_AutoStopTonesOnOnHook method [TAPI 2.2], get_AutoStopTonesOnOnHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autostoptonesononhook, tapi3if/ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook
ms.prod: windows
ms.technology: windows-sdk
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
 - ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook


## -description


The 
<b>get_AutoStopTonesOnOnHook</b> method retrieves the current value of the <b>AutoStopTonesOnOnHook</b> property. When this feature is enabled, the phone going onhook results in the termination of any tone produced on the audio render device associated with the phone (via a call to 
<a href="https://msdn.microsoft.com/618743c3-6d4a-4cab-a4fc-7cd4e3b8cdd9">ITAutomatedPhoneControl::StopTone</a>).


## -parameters




### -param pfEnabled [out]

If VARIANT_TRUE, automatic stop of tone generation upon onhook is enabled. If VARIANT_FALSE, automatic stop of tone generation upon onhook is disabled.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoStopTonesOnOnHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopTonesOnOnHook</b> property at any time. The reconfiguration takes effect the next time the phone goes onhook.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/618743c3-6d4a-4cab-a4fc-7cd4e3b8cdd9">ITAutomatedPhoneControl::StopTone</a>



<a href="https://msdn.microsoft.com/0047b631-91fc-47fb-aa38-cedb096a5646">put_AutoStopTonesOnOnHook</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

