---
UID: NE:tapi3if.PHONE_HOOK_SWITCH_STATE
title: PHONE_HOOK_SWITCH_STATE
author: windows-driver-content
description: The PHONE_HOOK_SWITCH_STATE enum provides indicators of the phone hookswitch status.
old-location: tapi3\phone_hook_switch_state.htm
old-project: Tapi
ms.assetid: c9501a3f-1aaa-4d58-aca1-5ef00c31d195
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PHONE_HOOK_SWITCH_STATE, PHONE_HOOK_SWITCH_STATE enumeration [TAPI 2.2], PHSS_OFFHOOK, PHSS_OFFHOOK_MIC_ONLY, PHSS_OFFHOOK_SPEAKER_ONLY, PHSS_ONHOOK, _tapi3_phone_hook_switch_state, tapi3.phone_hook_switch_state, tapi3if/PHONE_HOOK_SWITCH_STATE, tapi3if/PHSS_OFFHOOK, tapi3if/PHSS_OFFHOOK_MIC_ONLY, tapi3if/PHSS_OFFHOOK_SPEAKER_ONLY, tapi3if/PHSS_ONHOOK
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
req.typenames: PHONE_HOOK_SWITCH_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	PHONE_HOOK_SWITCH_STATE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# PHONE_HOOK_SWITCH_STATE enumeration


## -description


The 
<b>PHONE_HOOK_SWITCH_STATE</b> enum provides indicators of the phone hookswitch status.


## -enum-fields




### -field PHSS_ONHOOK

Indicates that the phone is onhook.


### -field PHSS_OFFHOOK_MIC_ONLY

Indicates that only the phone's microphone is offhook.


### -field PHSS_OFFHOOK_SPEAKER_ONLY

Indicates that only the phone's speaker is offhook.


### -field PHSS_OFFHOOK

Indicates that the phone is offhook.


## -see-also




<a href="https://msdn.microsoft.com/4560b447-45af-482a-b97b-dd0cbdb52466">ITPhone::get_HookSwitchState</a>



<a href="https://msdn.microsoft.com/ab0bcd30-6985-4f53-a39d-90230421b6f4">ITPhone::put_HookSwitchState</a>



<a href="https://msdn.microsoft.com/d7d1033d-0a37-4b9c-86d7-bab5a2cbb454">ITPhoneEvent::get_HookSwitchState</a>
 

 

