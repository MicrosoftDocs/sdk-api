---
UID: NF:tapi3if.ITPhoneEvent.get_RingMode
title: ITPhoneEvent::get_RingMode (tapi3if.h)
description: The get_RingMode method returns a long value specifying the ring mode to which the phone has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_RINGMODE.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_RingMode method","ITPhoneEvent.get_RingMode","ITPhoneEvent::get_RingMode","_tapi3_itphoneevent_get_ringmode","get_RingMode","get_RingMode method [TAPI 2.2]","get_RingMode method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_ringmode","tapi3if/ITPhoneEvent::get_RingMode"]
old-location: tapi3\itphoneevent_get_ringmode.htm
tech.root: tapi3
ms.assetid: cd43ce66-bcbf-4863-87cc-db10dd81ba99
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_RingMode method, ITPhoneEvent.get_RingMode, ITPhoneEvent::get_RingMode, _tapi3_itphoneevent_get_ringmode, get_RingMode, get_RingMode method [TAPI 2.2], get_RingMode method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_ringmode, tapi3if/ITPhoneEvent::get_RingMode
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
 - ITPhoneEvent::get_RingMode
 - tapi3if/ITPhoneEvent::get_RingMode
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
 - ITPhoneEvent.get_RingMode
---

# ITPhoneEvent::get_RingMode


## -description

The 
<b>get_RingMode</b> method returns a long value specifying the ring mode to which the phone has transitioned. This information is available only when the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> method returns PE_RINGMODE.

## -parameters

### -param plRingMode [out]

Ring mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>