---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay
title: ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay
author: windows-driver-content
description: The get_AutoVolumeControlRepeatDelay method retrieves the current value of the AutoVolumeControlRepeatDelay property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrolrepeatdelay.htm
old-project: Tapi
ms.assetid: a26fd436-b792-4415-bc47-eca2b1114002
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControlRepeatDelay method, ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay, ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay, _tapi3_itautomatedphonecontrol_get_autovolumecontrolrepeatdelay, get_AutoVolumeControlRepeatDelay, get_AutoVolumeControlRepeatDelay method [TAPI 2.2], get_AutoVolumeControlRepeatDelay method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrolrepeatdelay, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay


## -description


The 
<b>get_AutoVolumeControlRepeatDelay</b> method retrieves the current value of the <b>AutoVolumeControlRepeatDelay</b> property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.


## -parameters




### -param plDelay [out]

Delay, in milliseconds, of the volume repeat delay. The default value is 500 ms.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>



<a href="https://msdn.microsoft.com/a00993af-2ff2-4f91-889e-b0d3ae550642">put_AutoVolumeControlRepeatDelay</a>
 

 

