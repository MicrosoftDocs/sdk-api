---
UID: NE:tapi3if.PHONE_BUTTON_MODE
title: PHONE_BUTTON_MODE (tapi3if.h)
description: The PHONE_BUTTON_MODE enum describes the mode of a phone button.
helpviewer_keywords: ["PBM_CALL","PBM_DISPLAY","PBM_DUMMY","PBM_FEATURE","PBM_KEYPAD","PBM_LOCAL","PHONE_BUTTON_MODE","PHONE_BUTTON_MODE enumeration [TAPI 2.2]","_tapi3_phone_button_mode","tapi3.phone_button_mode","tapi3if/PBM_CALL","tapi3if/PBM_DISPLAY","tapi3if/PBM_DUMMY","tapi3if/PBM_FEATURE","tapi3if/PBM_KEYPAD","tapi3if/PBM_LOCAL","tapi3if/PHONE_BUTTON_MODE"]
old-location: tapi3\phone_button_mode.htm
tech.root: tapi3
ms.assetid: ae410224-bb01-4d56-95e8-1c2ead544cf1
ms.date: 12/05/2018
ms.keywords: PBM_CALL, PBM_DISPLAY, PBM_DUMMY, PBM_FEATURE, PBM_KEYPAD, PBM_LOCAL, PHONE_BUTTON_MODE, PHONE_BUTTON_MODE enumeration [TAPI 2.2], _tapi3_phone_button_mode, tapi3.phone_button_mode, tapi3if/PBM_CALL, tapi3if/PBM_DISPLAY, tapi3if/PBM_DUMMY, tapi3if/PBM_FEATURE, tapi3if/PBM_KEYPAD, tapi3if/PBM_LOCAL, tapi3if/PHONE_BUTTON_MODE
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
req.typenames: PHONE_BUTTON_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_BUTTON_MODE
 - tapi3if/PHONE_BUTTON_MODE
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
 - PHONE_BUTTON_MODE
---

# PHONE_BUTTON_MODE enumeration


## -description

The 
<b>PHONE_BUTTON_MODE</b> enum describes the mode of a phone button.

## -enum-fields

### -field PBM_DUMMY:0

Dummy button.

### -field PBM_CALL

Call button.

### -field PBM_FEATURE

Feature button.

### -field PBM_KEYPAD

Keypad button.

### -field PBM_LOCAL

Local function button, such as mute or volume control.

### -field PBM_DISPLAY

Display button.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonmode">ITPhone::get_ButtonMode</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttonmode">ITPhone::put_ButtonMode</a>
