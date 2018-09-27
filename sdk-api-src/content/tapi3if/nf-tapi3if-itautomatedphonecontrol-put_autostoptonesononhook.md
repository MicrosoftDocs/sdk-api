---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook
title: ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook
author: windows-sdk-content
description: The put_AutoStopTonesOnOnHook method sets the AutoStopTonesOnOnHook property for this phone.
old-location: tapi3\itautomatedphonecontrol_put_autostoptonesononhook.htm
tech.root: tapi
ms.assetid: 0047b631-91fc-47fb-aa38-cedb096a5646
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoStopTonesOnOnHook method, ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook, ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook, _tapi3_itautomatedphonecontrol_put_autostoptonesononhook, put_AutoStopTonesOnOnHook, put_AutoStopTonesOnOnHook method [TAPI 2.2], put_AutoStopTonesOnOnHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autostoptonesononhook, tapi3if/ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook
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
 - ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook


## -description


The 
<b>put_AutoStopTonesOnOnHook</b> method sets the <b>AutoStopTonesOnOnHook</b> property for this phone. When this feature is enabled, the phone going onhook results in the termination of any tone produced on the audio render device associated with the phone (via a call to 
<a href="https://msdn.microsoft.com/618743c3-6d4a-4cab-a4fc-7cd4e3b8cdd9">ITAutomatedPhoneControl::StopTone</a>).


## -parameters




### -param fEnabled [in]

If VARIANT_TRUE, enables automatic stop of tone generation if the phone goes onhook. If VARIANT_FALSE, disables automatic stop if the phone goes onhook. The default value is VARIANT_TRUE.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoStopTonesOnOnHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopTonesOnOnHook</b> property at any time. The reconfiguration takes effect the next time the phone goes onhook.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/618743c3-6d4a-4cab-a4fc-7cd4e3b8cdd9">ITAutomatedPhoneControl::StopTone</a>



<a href="https://msdn.microsoft.com/2ece8d7a-b280-42b6-9f51-d88650488699">get_AutoStopTonesOnOnHook</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

