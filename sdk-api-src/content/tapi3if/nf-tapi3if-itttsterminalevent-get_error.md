---
UID: NF:tapi3if.ITTTSTerminalEvent.get_Error
title: ITTTSTerminalEvent::get_Error (tapi3if.h)
description: The get_Error method gets an HRESULT cast of the error code involved in the terminal event.
helpviewer_keywords: ["ITTTSTerminalEvent interface [TAPI 2.2]","get_Error method","ITTTSTerminalEvent.get_Error","ITTTSTerminalEvent::get_Error","_tapi3_itttsterminalevent_get_error","get_Error","get_Error method [TAPI 2.2]","get_Error method [TAPI 2.2]","ITTTSTerminalEvent interface","tapi3.itttsterminalevent_get_error","tapi3if/ITTTSTerminalEvent::get_Error"]
old-location: tapi3\itttsterminalevent_get_error.htm
tech.root: tapi3
ms.assetid: 1a120114-a902-4e66-81e5-9f10205714ad
ms.date: 12/05/2018
ms.keywords: ITTTSTerminalEvent interface [TAPI 2.2],get_Error method, ITTTSTerminalEvent.get_Error, ITTTSTerminalEvent::get_Error, _tapi3_itttsterminalevent_get_error, get_Error, get_Error method [TAPI 2.2], get_Error method [TAPI 2.2],ITTTSTerminalEvent interface, tapi3.itttsterminalevent_get_error, tapi3if/ITTTSTerminalEvent::get_Error
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
 - ITTTSTerminalEvent::get_Error
 - tapi3if/ITTTSTerminalEvent::get_Error
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
 - ITTTSTerminalEvent.get_Error
---

# ITTTSTerminalEvent::get_Error


## -description

The 
<b>get_Error</b> method gets an <b>HRESULT</b> cast of the error code involved in the terminal event.

## -parameters

### -param phrErrorCode [out]

Pointer to the <b>HRESULT</b> cast of the error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent">ITTTSTerminalEvent</a>