---
UID: NF:tapi3if.ITPhoneEvent.get_ButtonState
title: ITPhoneEvent::get_ButtonState (tapi3if.h)
description: The get_ButtonState method returns a PHONE_BUTTON_STATE value specifying the state to which the button has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_BUTTON.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_ButtonState method","ITPhoneEvent.get_ButtonState","ITPhoneEvent::get_ButtonState","_tapi3_itphoneevent_get_buttonstate","get_ButtonState","get_ButtonState method [TAPI 2.2]","get_ButtonState method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_buttonstate","tapi3if/ITPhoneEvent::get_ButtonState"]
old-location: tapi3\itphoneevent_get_buttonstate.htm
tech.root: tapi3
ms.assetid: 6eedda9d-c127-446d-972c-09a7c1a4bd0f
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_ButtonState method, ITPhoneEvent.get_ButtonState, ITPhoneEvent::get_ButtonState, _tapi3_itphoneevent_get_buttonstate, get_ButtonState, get_ButtonState method [TAPI 2.2], get_ButtonState method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_buttonstate, tapi3if/ITPhoneEvent::get_ButtonState
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
 - ITPhoneEvent::get_ButtonState
 - tapi3if/ITPhoneEvent::get_ButtonState
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
 - ITPhoneEvent.get_ButtonState
---

# ITPhoneEvent::get_ButtonState


## -description

The 
<b>get_ButtonState</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_state">PHONE_BUTTON_STATE</a> value specifying the state to which the button has transitioned. This information is available only when the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> method returns PE_BUTTON.

## -parameters

### -param pState [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_state">PHONE_BUTTON_STATE</a> descriptor of the button's current state.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is available because some buttons do not support the PBS_DOWN button state, but instead momentarily report PBS_PRESSED. Additionally, the application can miss the button press on phones that do support PBS_DOWN if the button is pressed only for a short time and the call to the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonstate">ITPhone::get_ButtonState</a> method does not execute quickly enough.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>