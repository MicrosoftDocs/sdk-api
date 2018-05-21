---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControl
title: ITAutomatedPhoneControl::put_AutoVolumeControl
author: windows-driver-content
description: The put_AutoVolumeControl method sets the AutoVolumeControl property for this phone.
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrol.htm
old-project: Tapi
ms.assetid: 3d45ef58-a7d7-41ab-b06a-9d53bf79690a
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControl method, ITAutomatedPhoneControl.put_AutoVolumeControl, ITAutomatedPhoneControl::put_AutoVolumeControl, _tapi3_itautomatedphonecontrol_put_autovolumecontrol, put_AutoVolumeControl, put_AutoVolumeControl method [TAPI 2.2], put_AutoVolumeControl method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrol, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControl
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
-	ITAutomatedPhoneControl.put_AutoVolumeControl
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl::put_AutoVolumeControl


## -description


The 
<b>put_AutoVolumeControl</b> method sets the <b>AutoVolumeControl</b> property for this phone. When this feature is enabled, the phone's wave output volume is automatically adjusted whenever a volume button is pressed. The volume is adjusted by the amount indicated by the <b>AutoVolumeControlStep</b> property.


## -parameters




### -param fEnabled [in]

If VARIANT_TRUE, enables automatic volume control. If VARIANT_FALSE, disables automatic volume control. The default value is VARIANT_TRUE.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoVolumeControl</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoVolumeControl</b> property at any time. The reconfiguration takes effect the next time a volume button is pressed.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/7dae6d41-59d8-40ab-901f-91d97b59ac83">get_AutoVolumeControl</a>



<a href="https://msdn.microsoft.com/19766507-7a15-4c45-91bd-4b49ceb177e6">put_AutoVolumeControlStep</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

