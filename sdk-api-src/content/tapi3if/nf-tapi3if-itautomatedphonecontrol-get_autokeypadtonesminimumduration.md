---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration
title: ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration
author: windows-sdk-content
description: The get_AutoKeypadTonesMinimumDuration method retrieves the current value of the AutoKeypadTonesMinimumDuration property. The property specifies how long to play keypad tones on PBS_DOWN.
old-location: tapi3\itautomatedphonecontrol_get_autokeypadtonesminimumduration.htm
tech.root: tapi
ms.assetid: 9f1ae3f0-ae6a-408a-ac53-e4181ecf2c4b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoKeypadTonesMinimumDuration method, ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration, ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration, _tapi3_itautomatedphonecontrol_get_autokeypadtonesminimumduration, get_AutoKeypadTonesMinimumDuration, get_AutoKeypadTonesMinimumDuration method [TAPI 2.2], get_AutoKeypadTonesMinimumDuration method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autokeypadtonesminimumduration, tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration
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
 - ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration


## -description


The 
<b>get_AutoKeypadTonesMinimumDuration</b> method retrieves the current value of the <b>AutoKeypadTonesMinimumDuration</b> property. The property specifies how long to play keypad tones on PBS_DOWN.


## -parameters




### -param plDuration [out]

Minimum duration of keypad tones, in milliseconds (ms). The default value is 250 ms. If the minimum duration elapses without a PBS_UP event, the keypad tone continues until the PBS_UP event is received.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoKeypadTonesMinimumDuration</b> property functions only when the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>



<a href="https://msdn.microsoft.com/8c4bdd45-7d19-47a4-aa18-5944d3e58797">put_AutoKeypadTonesMinimumDuration</a>
 

 

