---
UID: NF:tapi3if.ITPhoneEvent.get_HookSwitchState
title: ITPhoneEvent::get_HookSwitchState
author: windows-sdk-content
description: The get_HookSwitchState method returns a PHONE_HOOK_SWITCH_STATE value specifying the state to which the hookswitch has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_HOOKSWITCH.
old-location: tapi3\itphoneevent_get_hookswitchstate.htm
tech.root: Tapi
ms.assetid: d7d1033d-0a37-4b9c-86d7-bab5a2cbb454
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_HookSwitchState method, ITPhoneEvent.get_HookSwitchState, ITPhoneEvent::get_HookSwitchState, _tapi3_itphoneevent_get_hookswitchstate, get_HookSwitchState, get_HookSwitchState method [TAPI 2.2], get_HookSwitchState method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_hookswitchstate, tapi3if/ITPhoneEvent::get_HookSwitchState
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
 - ITPhoneEvent.get_HookSwitchState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhoneEvent::get_HookSwitchState


## -description


The 
<b>get_HookSwitchState</b> method returns a 
<a href="https://msdn.microsoft.com/c9501a3f-1aaa-4d58-aca1-5ef00c31d195">PHONE_HOOK_SWITCH_STATE</a> value specifying the state to which the hookswitch has transitioned. This information is available only when the 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> method returns PE_HOOKSWITCH.


## -parameters




### -param pState [out]

Pointer to the 
<a href="https://msdn.microsoft.com/c9501a3f-1aaa-4d58-aca1-5ef00c31d195">PHONE_HOOK_SWITCH_STATE</a> descriptor of the current hookswitch state.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

