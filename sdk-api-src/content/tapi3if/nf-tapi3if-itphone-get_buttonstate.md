---
UID: NF:tapi3if.ITPhone.get_ButtonState
title: ITPhone::get_ButtonState (tapi3if.h)
description: The get_ButtonState method retrieves the button state associated with a particular button.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_ButtonState method","ITPhone.get_ButtonState","ITPhone::get_ButtonState","_tapi3_itphone_get_buttonstate","get_ButtonState","get_ButtonState method [TAPI 2.2]","get_ButtonState method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_buttonstate","tapi3if/ITPhone::get_ButtonState"]
old-location: tapi3\itphone_get_buttonstate.htm
tech.root: tapi3
ms.assetid: f14e0593-0f03-4119-b80a-12d32b68aa99
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonState method, ITPhone.get_ButtonState, ITPhone::get_ButtonState, _tapi3_itphone_get_buttonstate, get_ButtonState, get_ButtonState method [TAPI 2.2], get_ButtonState method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttonstate, tapi3if/ITPhone::get_ButtonState
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
 - ITPhone::get_ButtonState
 - tapi3if/ITPhone::get_ButtonState
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
 - ITPhone.get_ButtonState
---

# ITPhone::get_ButtonState


## -description

The 
<b>get_ButtonState</b> method retrieves the button state associated with a particular button.

The application must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before invoking this method; otherwise, the invocation fails.

## -parameters

### -param lButtonID [in]

Button identifier.

### -param pButtonState [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_state">PHONE_BUTTON_STATE</a> descriptor for the button's state.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_buttonstate">ITPhoneEvent::get_ButtonState</a>