---
UID: NE:tapi3if.PHONE_HOOK_SWITCH_DEVICE
title: PHONE_HOOK_SWITCH_DEVICE
author: windows-sdk-content
description: The PHONE_HOOK_SWITCH_DEVICE enum is used to indicate the types of switch hooks on a phone device.
old-location: tapi3\phone_hook_switch_device.htm
tech.root: Tapi
ms.assetid: 20b17e2f-f745-41ef-91ac-d2ab21d43695
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PHONE_HOOK_SWITCH_DEVICE, PHONE_HOOK_SWITCH_DEVICE enumeration [TAPI 2.2], PHSD_HANDSET, PHSD_HEADSET, PHSD_SPEAKERPHONE, _tapi3_phone_hook_switch_device, tapi3.phone_hook_switch_device, tapi3if/PHONE_HOOK_SWITCH_DEVICE, tapi3if/PHSD_HANDSET, tapi3if/PHSD_HEADSET, tapi3if/PHSD_SPEAKERPHONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - PHONE_HOOK_SWITCH_DEVICE
product: Windows
targetos: Windows
req.typenames: PHONE_HOOK_SWITCH_DEVICE
req.redist: 
---

# PHONE_HOOK_SWITCH_DEVICE enumeration


## -description


The 
<b>PHONE_HOOK_SWITCH_DEVICE</b> enum is used to indicate the types of switch hooks on a phone device.


## -enum-fields




### -field PHSD_HANDSET

The handset's hookswitch.


### -field PHSD_SPEAKERPHONE

The speakerphone's hookswitch.


### -field PHSD_HEADSET

The headset's hookswitch.


## -see-also




<a href="https://msdn.microsoft.com/4560b447-45af-482a-b97b-dd0cbdb52466">ITPhone::get_HookSwitchState</a>



<a href="https://msdn.microsoft.com/ab0bcd30-6985-4f53-a39d-90230421b6f4">ITPhone::put_HookSwitchState</a>



<a href="https://msdn.microsoft.com/acc25e8e-966f-4b54-ad59-226d2b7728b8">ITPhoneEvent::get_HookSwitchDevice</a>
 

 

