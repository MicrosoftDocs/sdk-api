---
UID: NF:tapi3if.ITTTSTerminalEvent.get_Call
title: ITTTSTerminalEvent::get_Call (tapi3if.h)
description: The get_Call method returns an ITCallInfo interface pointer for the call involved in the terminal event.
helpviewer_keywords: ["ITTTSTerminalEvent interface [TAPI 2.2]","get_Call method","ITTTSTerminalEvent.get_Call","ITTTSTerminalEvent::get_Call","_tapi3_itttsterminalevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITTTSTerminalEvent interface","tapi3.itttsterminalevent_get_call","tapi3if/ITTTSTerminalEvent::get_Call"]
old-location: tapi3\itttsterminalevent_get_call.htm
tech.root: tapi3
ms.assetid: 7e9ffff3-1282-4d05-83c9-7f824406fcfa
ms.date: 12/05/2018
ms.keywords: ITTTSTerminalEvent interface [TAPI 2.2],get_Call method, ITTTSTerminalEvent.get_Call, ITTTSTerminalEvent::get_Call, _tapi3_itttsterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITTTSTerminalEvent interface, tapi3.itttsterminalevent_get_call, tapi3if/ITTTSTerminalEvent::get_Call
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
 - ITTTSTerminalEvent::get_Call
 - tapi3if/ITTTSTerminalEvent::get_Call
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
 - ITTTSTerminalEvent.get_Call
---

# ITTTSTerminalEvent::get_Call


## -description

The 
<b>get_Call</b> method returns an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointer for the call involved in the terminal event.

## -parameters

### -param ppCall [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITTTSTerminalEvent::get_Call</b>. The application must call <b>Release</b> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent">ITTTSTerminalEvent</a>