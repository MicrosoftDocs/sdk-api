---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

