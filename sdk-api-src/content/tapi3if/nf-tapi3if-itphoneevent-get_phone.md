---
UID: NF:tapi3if.ITPhoneEvent.get_Phone
title: ITPhoneEvent::get_Phone (tapi3if.h)
description: The get_Phone method returns a pointer to the ITPhone interface on the phone object that fired this event.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_Phone method","ITPhoneEvent.get_Phone","ITPhoneEvent::get_Phone","_tapi3_itphoneevent_get_phone","get_Phone","get_Phone method [TAPI 2.2]","get_Phone method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_phone","tapi3if/ITPhoneEvent::get_Phone"]
old-location: tapi3\itphoneevent_get_phone.htm
tech.root: tapi3
ms.assetid: 81b61c98-839a-488b-a0da-085f8891197c
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_Phone method, ITPhoneEvent.get_Phone, ITPhoneEvent::get_Phone, _tapi3_itphoneevent_get_phone, get_Phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_phone, tapi3if/ITPhoneEvent::get_Phone
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
 - ITPhoneEvent::get_Phone
 - tapi3if/ITPhoneEvent::get_Phone
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
 - ITPhoneEvent.get_Phone
---

# ITPhoneEvent::get_Phone


## -description

The 
<b>get_Phone</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface on the phone object that fired this event.

## -parameters

### -param ppPhone [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface returned by <b>ITPhoneEvent::get_Phone</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>