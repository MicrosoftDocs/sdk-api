---
UID: NF:tapi3if.ITASRTerminalEvent.get_Error
title: ITASRTerminalEvent::get_Error (tapi3if.h)
description: The get_Error method returns an HRESULT cast of the error associated with the terminal event.
helpviewer_keywords: ["ITASRTerminalEvent interface [TAPI 2.2]","get_Error method","ITASRTerminalEvent.get_Error","ITASRTerminalEvent::get_Error","_tapi3_itasrterminalevent_get_error","get_Error","get_Error method [TAPI 2.2]","get_Error method [TAPI 2.2]","ITASRTerminalEvent interface","tapi3.itasrterminalevent_get_error","tapi3if/ITASRTerminalEvent::get_Error"]
old-location: tapi3\itasrterminalevent_get_error.htm
tech.root: tapi3
ms.assetid: 7bccf537-a54b-4c40-866b-0f7a42149841
ms.date: 12/05/2018
ms.keywords: ITASRTerminalEvent interface [TAPI 2.2],get_Error method, ITASRTerminalEvent.get_Error, ITASRTerminalEvent::get_Error, _tapi3_itasrterminalevent_get_error, get_Error, get_Error method [TAPI 2.2], get_Error method [TAPI 2.2],ITASRTerminalEvent interface, tapi3.itasrterminalevent_get_error, tapi3if/ITASRTerminalEvent::get_Error
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
 - ITASRTerminalEvent::get_Error
 - tapi3if/ITASRTerminalEvent::get_Error
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
 - ITASRTerminalEvent.get_Error
---

# ITASRTerminalEvent::get_Error


## -description

The 
<b>get_Error</b> method returns an HRESULT cast of the error associated with the terminal event.

## -parameters

### -param phrErrorCode [out]

Pointer to error code.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent">ITASRTerminalEvent</a>