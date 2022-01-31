---
UID: NE:tapi3if.PHONE_BUTTON_STATE
title: PHONE_BUTTON_STATE (tapi3if.h)
description: The PHONE_BUTTON_STATE enum describes the state of a phone button.
helpviewer_keywords: ["PBS_DOWN","PBS_UNAVAIL","PBS_UNKNOWN","PBS_UP","PHONE_BUTTON_STATE","PHONE_BUTTON_STATE enumeration [TAPI 2.2]","_tapi3_phone_button_state","tapi3.phone_button_state","tapi3if/PBS_DOWN","tapi3if/PBS_UNAVAIL","tapi3if/PBS_UNKNOWN","tapi3if/PBS_UP","tapi3if/PHONE_BUTTON_STATE"]
old-location: tapi3\phone_button_state.htm
tech.root: tapi3
ms.assetid: a9f7b527-9c74-45ac-9394-6f736aae1ccf
ms.date: 12/05/2018
ms.keywords: PBS_DOWN, PBS_UNAVAIL, PBS_UNKNOWN, PBS_UP, PHONE_BUTTON_STATE, PHONE_BUTTON_STATE enumeration [TAPI 2.2], _tapi3_phone_button_state, tapi3.phone_button_state, tapi3if/PBS_DOWN, tapi3if/PBS_UNAVAIL, tapi3if/PBS_UNKNOWN, tapi3if/PBS_UP, tapi3if/PHONE_BUTTON_STATE
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
req.typenames: PHONE_BUTTON_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_BUTTON_STATE
 - tapi3if/PHONE_BUTTON_STATE
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
 - PHONE_BUTTON_STATE
---

# PHONE_BUTTON_STATE enumeration


## -description

The 
<b>PHONE_BUTTON_STATE</b> enum describes the state of a phone button.

## -enum-fields

### -field PBS_UP:0x1

State of the button is up.

### -field PBS_DOWN:0x2

State of the button is down.

### -field PBS_UNKNOWN:0x4

State of the button is not known.

### -field PBS_UNAVAIL:0x8

State of the button is not available.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonstate">ITPhone::get_ButtonState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_buttonstate">ITPhoneEvent::get_ButtonState</a>
