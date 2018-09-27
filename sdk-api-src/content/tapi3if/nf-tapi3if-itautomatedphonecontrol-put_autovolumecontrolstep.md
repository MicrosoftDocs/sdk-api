---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControlStep
title: ITAutomatedPhoneControl::put_AutoVolumeControlStep
author: windows-sdk-content
description: The put_AutoVolumeControlStep method sets the AutoVolumeControlStep property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrolstep.htm
tech.root: tapi
ms.assetid: 19766507-7a15-4c45-91bd-4b49ceb177e6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControlStep method, ITAutomatedPhoneControl.put_AutoVolumeControlStep, ITAutomatedPhoneControl::put_AutoVolumeControlStep, _tapi3_itautomatedphonecontrol_put_autovolumecontrolstep, put_AutoVolumeControlStep, put_AutoVolumeControlStep method [TAPI 2.2], put_AutoVolumeControlStep method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrolstep, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlStep
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
 - ITAutomatedPhoneControl.put_AutoVolumeControlStep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::put_AutoVolumeControlStep


## -description


The 
<b>put_AutoVolumeControlStep</b> method sets the <b>AutoVolumeControlStep</b> property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.


## -parameters




### -param lStepSize [in]

Volume control step, in milliseconds. The default value of the <b>AutoVolumeControlStep</b> property is 4096.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/6cf6beba-36ca-417b-91b4-9c008a14efef">get_AutoVolumeControlStep</a>



<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>
 

 

