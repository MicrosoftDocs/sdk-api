---
UID: NF:tapi3if.ITToneTerminalEvent.get_Error
title: ITToneTerminalEvent::get_Error (tapi3if.h)
description: The get_Error method returns an HRESULT cast of the error code involved in the event.
helpviewer_keywords: ["ITToneTerminalEvent interface [TAPI 2.2]","get_Error method","ITToneTerminalEvent.get_Error","ITToneTerminalEvent::get_Error","_tapi3_ittoneterminalevent_get_error","get_Error","get_Error method [TAPI 2.2]","get_Error method [TAPI 2.2]","ITToneTerminalEvent interface","tapi3.ittoneterminalevent_get_error","tapi3if/ITToneTerminalEvent::get_Error"]
old-location: tapi3\ittoneterminalevent_get_error.htm
tech.root: tapi3
ms.assetid: f91497b0-b340-4eb9-8d9f-364991343c3b
ms.date: 12/05/2018
ms.keywords: ITToneTerminalEvent interface [TAPI 2.2],get_Error method, ITToneTerminalEvent.get_Error, ITToneTerminalEvent::get_Error, _tapi3_ittoneterminalevent_get_error, get_Error, get_Error method [TAPI 2.2], get_Error method [TAPI 2.2],ITToneTerminalEvent interface, tapi3.ittoneterminalevent_get_error, tapi3if/ITToneTerminalEvent::get_Error
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
 - ITToneTerminalEvent::get_Error
 - tapi3if/ITToneTerminalEvent::get_Error
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
 - ITToneTerminalEvent.get_Error
---

# ITToneTerminalEvent::get_Error


## -description

The 
<b>get_Error</b> method returns an <b>HRESULT</b> cast of the error code involved in the event.

## -parameters

### -param phrErrorCode [out]

<b>HRESULT</b> cast of the error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent">ITToneTerminalEvent</a>