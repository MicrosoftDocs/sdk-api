---
UID: NF:tapi3if.ITPhoneEvent.get_ButtonLampId
title: ITPhoneEvent::get_ButtonLampId (tapi3if.h)
description: The get_ButtonLampId method returns a long value indicating which button or lamp triggered the event. This information is available only when ITPhoneEvent::get_Event returns PE_LAMPMODE or PE_BUTTON.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_ButtonLampId method","ITPhoneEvent.get_ButtonLampId","ITPhoneEvent::get_ButtonLampId","_tapi3_itphoneevent_get_buttonlampid","get_ButtonLampId","get_ButtonLampId method [TAPI 2.2]","get_ButtonLampId method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_buttonlampid","tapi3if/ITPhoneEvent::get_ButtonLampId"]
old-location: tapi3\itphoneevent_get_buttonlampid.htm
tech.root: tapi3
ms.assetid: 43b87d10-8cb9-4795-8778-70c8f8ae6300
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_ButtonLampId method, ITPhoneEvent.get_ButtonLampId, ITPhoneEvent::get_ButtonLampId, _tapi3_itphoneevent_get_buttonlampid, get_ButtonLampId, get_ButtonLampId method [TAPI 2.2], get_ButtonLampId method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_buttonlampid, tapi3if/ITPhoneEvent::get_ButtonLampId
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
 - ITPhoneEvent::get_ButtonLampId
 - tapi3if/ITPhoneEvent::get_ButtonLampId
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
 - ITPhoneEvent.get_ButtonLampId
---

# ITPhoneEvent::get_ButtonLampId


## -description

The 
<b>get_ButtonLampId</b> method returns a long value indicating which button or lamp triggered the event. This information is available only when 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> returns PE_LAMPMODE or PE_BUTTON.

## -parameters

### -param plButtonLampId [out]

Button or lamp ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>