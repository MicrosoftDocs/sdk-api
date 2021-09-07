---
UID: NF:tapi3if.ITPhoneEvent.get_HookSwitchState
title: ITPhoneEvent::get_HookSwitchState (tapi3if.h)
description: The get_HookSwitchState method returns a PHONE_HOOK_SWITCH_STATE value specifying the state to which the hookswitch has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_HOOKSWITCH.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_HookSwitchState method","ITPhoneEvent.get_HookSwitchState","ITPhoneEvent::get_HookSwitchState","_tapi3_itphoneevent_get_hookswitchstate","get_HookSwitchState","get_HookSwitchState method [TAPI 2.2]","get_HookSwitchState method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_hookswitchstate","tapi3if/ITPhoneEvent::get_HookSwitchState"]
old-location: tapi3\itphoneevent_get_hookswitchstate.htm
tech.root: tapi3
ms.assetid: d7d1033d-0a37-4b9c-86d7-bab5a2cbb454
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_HookSwitchState method, ITPhoneEvent.get_HookSwitchState, ITPhoneEvent::get_HookSwitchState, _tapi3_itphoneevent_get_hookswitchstate, get_HookSwitchState, get_HookSwitchState method [TAPI 2.2], get_HookSwitchState method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_hookswitchstate, tapi3if/ITPhoneEvent::get_HookSwitchState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPhoneEvent::get_HookSwitchState
 - tapi3if/ITPhoneEvent::get_HookSwitchState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhoneEvent.get_HookSwitchState
---

# ITPhoneEvent::get_HookSwitchState


## -description

The 
<b>get_HookSwitchState</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_state">PHONE_HOOK_SWITCH_STATE</a> value specifying the state to which the hookswitch has transitioned. This information is available only when the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> method returns PE_HOOKSWITCH.

## -parameters

### -param pState [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_state">PHONE_HOOK_SWITCH_STATE</a> descriptor of the current hookswitch state.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>