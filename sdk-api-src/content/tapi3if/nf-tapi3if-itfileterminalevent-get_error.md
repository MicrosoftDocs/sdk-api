---
UID: NF:tapi3if.ITFileTerminalEvent.get_Error
title: ITFileTerminalEvent::get_Error (tapi3if.h)
description: The get_Error method gets the error code for the event.
helpviewer_keywords: ["ITFileTerminalEvent interface [TAPI 2.2]","get_Error method","ITFileTerminalEvent.get_Error","ITFileTerminalEvent::get_Error","_tapi3_itfileterminalevent_get_error","get_Error","get_Error method [TAPI 2.2]","get_Error method [TAPI 2.2]","ITFileTerminalEvent interface","tapi3.itfileterminalevent_get_error","tapi3if/ITFileTerminalEvent::get_Error"]
old-location: tapi3\itfileterminalevent_get_error.htm
tech.root: tapi3
ms.assetid: 1eabd161-12d1-4537-beb1-3a05996aa506
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Error method, ITFileTerminalEvent.get_Error, ITFileTerminalEvent::get_Error, _tapi3_itfileterminalevent_get_error, get_Error, get_Error method [TAPI 2.2], get_Error method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_error, tapi3if/ITFileTerminalEvent::get_Error
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
 - ITFileTerminalEvent::get_Error
 - tapi3if/ITFileTerminalEvent::get_Error
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
 - ITFileTerminalEvent.get_Error
---

# ITFileTerminalEvent::get_Error


## -description

The 
<b>get_Error</b> method gets the error code for the event.

## -parameters

### -param phrErrorCode [out]

HRESULT cast of error code associated with this event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>