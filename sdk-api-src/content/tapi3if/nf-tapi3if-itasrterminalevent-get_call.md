---
UID: NF:tapi3if.ITASRTerminalEvent.get_Call
title: ITASRTerminalEvent::get_Call (tapi3if.h)
description: The get_Call method returns a pointer to the ITCallInfo interface for the call object involved in the terminal event.
helpviewer_keywords: ["ITASRTerminalEvent interface [TAPI 2.2]","get_Call method","ITASRTerminalEvent.get_Call","ITASRTerminalEvent::get_Call","_tapi3_itasrterminalevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITASRTerminalEvent interface","tapi3.itasrterminalevent_get_call","tapi3if/ITASRTerminalEvent::get_Call"]
old-location: tapi3\itasrterminalevent_get_call.htm
tech.root: tapi3
ms.assetid: 8736e3bc-9f79-4b0f-84a7-00e6d20550e2
ms.date: 12/05/2018
ms.keywords: ITASRTerminalEvent interface [TAPI 2.2],get_Call method, ITASRTerminalEvent.get_Call, ITASRTerminalEvent::get_Call, _tapi3_itasrterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITASRTerminalEvent interface, tapi3.itasrterminalevent_get_call, tapi3if/ITASRTerminalEvent::get_Call
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
 - ITASRTerminalEvent::get_Call
 - tapi3if/ITASRTerminalEvent::get_Call
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
 - ITASRTerminalEvent.get_Call
---

# ITASRTerminalEvent::get_Call


## -description

The 
<b>get_Call</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call object involved in the terminal event.

## -parameters

### -param ppCall [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent">ITASRTerminalEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>