---
UID: NF:tapi3if.ITPhoneEvent.get_Event
title: ITPhoneEvent::get_Event (tapi3if.h)
description: The get_Event method returns a PHONE_EVENT value specifying the type of phone event that occurred.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_Event method","ITPhoneEvent.get_Event","ITPhoneEvent::get_Event","_tapi3_itphoneevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_event","tapi3if/ITPhoneEvent::get_Event"]
old-location: tapi3\itphoneevent_get_event.htm
tech.root: tapi3
ms.assetid: 01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_Event method, ITPhoneEvent.get_Event, ITPhoneEvent::get_Event, _tapi3_itphoneevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_event, tapi3if/ITPhoneEvent::get_Event
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
 - ITPhoneEvent::get_Event
 - tapi3if/ITPhoneEvent::get_Event
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
 - ITPhoneEvent.get_Event
---

# ITPhoneEvent::get_Event


## -description

The 
<b>get_Event</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_event">PHONE_EVENT</a> value specifying the type of phone event that occurred.

## -parameters

### -param pEvent [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_event">PHONE_EVENT</a> descriptor of the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>