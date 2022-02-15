---
UID: NF:tapi3if.ITToneTerminalEvent.get_Call
title: ITToneTerminalEvent::get_Call (tapi3if.h)
description: The get_Call method retrieves an interface pointer for the call object on which the event occurred.
helpviewer_keywords: ["ITToneTerminalEvent interface [TAPI 2.2]","get_Call method","ITToneTerminalEvent.get_Call","ITToneTerminalEvent::get_Call","_tapi3_ittoneterminalevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITToneTerminalEvent interface","tapi3.ittoneterminalevent_get_call","tapi3if/ITToneTerminalEvent::get_Call"]
old-location: tapi3\ittoneterminalevent_get_call.htm
tech.root: tapi3
ms.assetid: adbbce76-827d-439c-865d-9dcfe40c9722
ms.date: 12/05/2018
ms.keywords: ITToneTerminalEvent interface [TAPI 2.2],get_Call method, ITToneTerminalEvent.get_Call, ITToneTerminalEvent::get_Call, _tapi3_ittoneterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITToneTerminalEvent interface, tapi3.ittoneterminalevent_get_call, tapi3if/ITToneTerminalEvent::get_Call
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
 - ITToneTerminalEvent::get_Call
 - tapi3if/ITToneTerminalEvent::get_Call
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
 - ITToneTerminalEvent.get_Call
---

# ITToneTerminalEvent::get_Call


## -description

The 
<b>get_Call</b> method retrieves an interface pointer for the call object on which the event occurred.

## -parameters

### -param ppCall [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITToneTerminalEvent::get_Call</b>. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent">ITToneTerminalEvent</a>