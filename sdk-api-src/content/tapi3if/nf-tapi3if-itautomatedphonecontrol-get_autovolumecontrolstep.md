---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControlStep
title: ITAutomatedPhoneControl::get_AutoVolumeControlStep
author: windows-sdk-content
description: The get_AutoVolumeControlStep method retrieves the current value of the AutoVolumeControlStep property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrolstep.htm
old-project: Tapi
ms.assetid: 6cf6beba-36ca-417b-91b4-9c008a14efef
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControlStep method, ITAutomatedPhoneControl.get_AutoVolumeControlStep, ITAutomatedPhoneControl::get_AutoVolumeControlStep, _tapi3_itautomatedphonecontrol_get_autovolumecontrolstep, get_AutoVolumeControlStep, get_AutoVolumeControlStep method [TAPI 2.2], get_AutoVolumeControlStep method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrolstep, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlStep
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAutomatedPhoneControl.get_AutoVolumeControlStep
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl::get_AutoVolumeControlStep


## -description


The 
<b>get_AutoVolumeControlStep</b> method retrieves the current value of the <b>AutoVolumeControlStep</b> property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.


## -parameters




### -param plStepSize [out]

Volume control step. The default value of the <b>AutoVolumeControlStep</b> property is 4096.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>



<a href="https://msdn.microsoft.com/19766507-7a15-4c45-91bd-4b49ceb177e6">put_AutoVolumeControlStep</a>
 

 

