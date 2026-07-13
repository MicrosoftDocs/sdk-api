---
UID: NE:tapi3if.PHONE_HOOK_SWITCH_STATE
title: PHONE_HOOK_SWITCH_STATE (tapi3if.h)
description: The PHONE_HOOK_SWITCH_STATE enum provides indicators of the phone hookswitch status.
helpviewer_keywords: ["PHONE_HOOK_SWITCH_STATE","PHONE_HOOK_SWITCH_STATE enumeration [TAPI 2.2]","PHSS_OFFHOOK","PHSS_OFFHOOK_MIC_ONLY","PHSS_OFFHOOK_SPEAKER_ONLY","PHSS_ONHOOK","_tapi3_phone_hook_switch_state","tapi3.phone_hook_switch_state","tapi3if/PHONE_HOOK_SWITCH_STATE","tapi3if/PHSS_OFFHOOK","tapi3if/PHSS_OFFHOOK_MIC_ONLY","tapi3if/PHSS_OFFHOOK_SPEAKER_ONLY","tapi3if/PHSS_ONHOOK"]
old-location: tapi3\phone_hook_switch_state.htm
tech.root: tapi3
ms.assetid: c9501a3f-1aaa-4d58-aca1-5ef00c31d195
ms.date: 12/05/2018
ms.keywords: PHONE_HOOK_SWITCH_STATE, PHONE_HOOK_SWITCH_STATE enumeration [TAPI 2.2], PHSS_OFFHOOK, PHSS_OFFHOOK_MIC_ONLY, PHSS_OFFHOOK_SPEAKER_ONLY, PHSS_ONHOOK, _tapi3_phone_hook_switch_state, tapi3.phone_hook_switch_state, tapi3if/PHONE_HOOK_SWITCH_STATE, tapi3if/PHSS_OFFHOOK, tapi3if/PHSS_OFFHOOK_MIC_ONLY, tapi3if/PHSS_OFFHOOK_SPEAKER_ONLY, tapi3if/PHSS_ONHOOK
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
req.typenames: PHONE_HOOK_SWITCH_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_HOOK_SWITCH_STATE
 - tapi3if/PHONE_HOOK_SWITCH_STATE
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
 - PHONE_HOOK_SWITCH_STATE
---

# PHONE_HOOK_SWITCH_STATE enumeration


## -description

The 
<b>PHONE_HOOK_SWITCH_STATE</b> enum provides indicators of the phone hookswitch status.

## -enum-fields

### -field PHSS_ONHOOK:0x1

Indicates that the phone is onhook.

### -field PHSS_OFFHOOK_MIC_ONLY:0x2

Indicates that only the phone's microphone is offhook.

### -field PHSS_OFFHOOK_SPEAKER_ONLY:0x4

Indicates that only the phone's speaker is offhook.

### -field PHSS_OFFHOOK:0x8

Indicates that the phone is offhook.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_hookswitchstate">ITPhone::get_HookSwitchState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_hookswitchstate">ITPhone::put_HookSwitchState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_hookswitchstate">ITPhoneEvent::get_HookSwitchState</a>
