---
UID: NE:tapi3if.PHONE_HOOK_SWITCH_DEVICE
title: PHONE_HOOK_SWITCH_DEVICE (tapi3if.h)
description: The PHONE_HOOK_SWITCH_DEVICE enum is used to indicate the types of switch hooks on a phone device.
helpviewer_keywords: ["PHONE_HOOK_SWITCH_DEVICE","PHONE_HOOK_SWITCH_DEVICE enumeration [TAPI 2.2]","PHSD_HANDSET","PHSD_HEADSET","PHSD_SPEAKERPHONE","_tapi3_phone_hook_switch_device","tapi3.phone_hook_switch_device","tapi3if/PHONE_HOOK_SWITCH_DEVICE","tapi3if/PHSD_HANDSET","tapi3if/PHSD_HEADSET","tapi3if/PHSD_SPEAKERPHONE"]
old-location: tapi3\phone_hook_switch_device.htm
tech.root: tapi3
ms.assetid: 20b17e2f-f745-41ef-91ac-d2ab21d43695
ms.date: 12/05/2018
ms.keywords: PHONE_HOOK_SWITCH_DEVICE, PHONE_HOOK_SWITCH_DEVICE enumeration [TAPI 2.2], PHSD_HANDSET, PHSD_HEADSET, PHSD_SPEAKERPHONE, _tapi3_phone_hook_switch_device, tapi3.phone_hook_switch_device, tapi3if/PHONE_HOOK_SWITCH_DEVICE, tapi3if/PHSD_HANDSET, tapi3if/PHSD_HEADSET, tapi3if/PHSD_SPEAKERPHONE
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
targetos: Windows
req.typenames: PHONE_HOOK_SWITCH_DEVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_HOOK_SWITCH_DEVICE
 - tapi3if/PHONE_HOOK_SWITCH_DEVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - PHONE_HOOK_SWITCH_DEVICE
---

# PHONE_HOOK_SWITCH_DEVICE enumeration


## -description

The 
<b>PHONE_HOOK_SWITCH_DEVICE</b> enum is used to indicate the types of switch hooks on a phone device.

## -enum-fields

### -field PHSD_HANDSET:0x1

The handset's hookswitch.

### -field PHSD_SPEAKERPHONE:0x2

The speakerphone's hookswitch.

### -field PHSD_HEADSET:0x4

The headset's hookswitch.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_hookswitchstate">ITPhone::get_HookSwitchState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_hookswitchstate">ITPhone::put_HookSwitchState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_hookswitchdevice">ITPhoneEvent::get_HookSwitchDevice</a>
