---
UID: NE:tapi3if.PHONE_EVENT
title: PHONE_EVENT (tapi3if.h)
description: The PHONE_EVENT enum indicates a type of phone event.
helpviewer_keywords: ["PE_ANSWER","PE_BUTTON","PE_CAPSCHANGE","PE_CLOSE","PE_DIALING","PE_DISCONNECT","PE_DISPLAY","PE_HOOKSWITCH","PE_LAMPMODE","PE_LASTITEM","PE_NUMBERGATHERED","PE_RINGMODE","PE_RINGVOLUME","PHONE_EVENT","PHONE_EVENT enumeration [TAPI 2.2]","_tapi3_phone_event","tapi3.phone_event","tapi3if/PE_ANSWER","tapi3if/PE_BUTTON","tapi3if/PE_CAPSCHANGE","tapi3if/PE_CLOSE","tapi3if/PE_DIALING","tapi3if/PE_DISCONNECT","tapi3if/PE_DISPLAY","tapi3if/PE_HOOKSWITCH","tapi3if/PE_LAMPMODE","tapi3if/PE_LASTITEM","tapi3if/PE_NUMBERGATHERED","tapi3if/PE_RINGMODE","tapi3if/PE_RINGVOLUME","tapi3if/PHONE_EVENT"]
old-location: tapi3\phone_event.htm
tech.root: tapi3
ms.assetid: 9508cb8f-b7c9-4d5c-a58d-afdf079f9fee
ms.date: 12/05/2018
ms.keywords: PE_ANSWER, PE_BUTTON, PE_CAPSCHANGE, PE_CLOSE, PE_DIALING, PE_DISCONNECT, PE_DISPLAY, PE_HOOKSWITCH, PE_LAMPMODE, PE_LASTITEM, PE_NUMBERGATHERED, PE_RINGMODE, PE_RINGVOLUME, PHONE_EVENT, PHONE_EVENT enumeration [TAPI 2.2], _tapi3_phone_event, tapi3.phone_event, tapi3if/PE_ANSWER, tapi3if/PE_BUTTON, tapi3if/PE_CAPSCHANGE, tapi3if/PE_CLOSE, tapi3if/PE_DIALING, tapi3if/PE_DISCONNECT, tapi3if/PE_DISPLAY, tapi3if/PE_HOOKSWITCH, tapi3if/PE_LAMPMODE, tapi3if/PE_LASTITEM, tapi3if/PE_NUMBERGATHERED, tapi3if/PE_RINGMODE, tapi3if/PE_RINGVOLUME, tapi3if/PHONE_EVENT
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
req.typenames: PHONE_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_EVENT
 - tapi3if/PHONE_EVENT
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
 - PHONE_EVENT
---

# PHONE_EVENT enumeration


## -description

The 
<b>PHONE_EVENT</b> enum indicates a type of phone event.

## -enum-fields

### -field PE_DISPLAY:0

Phone display has changed.

### -field PE_LAMPMODE

Lamp mode has changed.

### -field PE_RINGMODE

Ringing mode has changed.

### -field PE_RINGVOLUME

Ringing volume has changed.

### -field PE_HOOKSWITCH

Hookswitch status has changed.

### -field PE_CAPSCHANGE

Phone capabilities have changed.

### -field PE_BUTTON

The phone button has changed.

### -field PE_CLOSE

The phone has been closed.

### -field PE_NUMBERGATHERED

A dialed number has been gathered by the phone.

### -field PE_DIALING

The phone is dialing.

### -field PE_ANSWER

The phone has been answered.

### -field PE_DISCONNECT

The phone has been disconnected.

### -field PE_LASTITEM

Last item in enum. Allows device-specific additions to this enum.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>
