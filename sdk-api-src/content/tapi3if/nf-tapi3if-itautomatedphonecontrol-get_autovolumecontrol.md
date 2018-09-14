---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControl
title: ITAutomatedPhoneControl::get_AutoVolumeControl
author: windows-sdk-content
description: The get_AutoVolumeControl method retrieves the current value of the AutoVolumeControl property.
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrol.htm
tech.root: TAPI
ms.assetid: 7dae6d41-59d8-40ab-901f-91d97b59ac83
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControl method, ITAutomatedPhoneControl.get_AutoVolumeControl, ITAutomatedPhoneControl::get_AutoVolumeControl, _tapi3_itautomatedphonecontrol_get_autovolumecontrol, get_AutoVolumeControl, get_AutoVolumeControl method [TAPI 2.2], get_AutoVolumeControl method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrol, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControl
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
 - ITAutomatedPhoneControl.get_AutoVolumeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::get_AutoVolumeControl


## -description


The 
<b>get_AutoVolumeControl</b> method retrieves the current value of the <b>AutoVolumeControl</b> property. When this feature is enabled, the phone's wave output volume is automatically adjusted whenever a volume button is pressed. The volume is adjusted by the amount indicated by the <b>AutoVolumeControlStep</b> property.


## -parameters




### -param fEnabled [out]

VARIANT_TRUE indicates that automatic volume control is enabled. VARIANT_FALSE indicates that automatic volume control is disabled.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



You can set the <b>AutoVolumeControl</b> property at any time. The reconfiguration takes effect the next time a volume button is pressed.

The <b>AutoVolumeControl</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/3d45ef58-a7d7-41ab-b06a-9d53bf79690a">put_AutoVolumeControl</a>



<a href="https://msdn.microsoft.com/19766507-7a15-4c45-91bd-4b49ceb177e6">put_AutoVolumeControlStep</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

