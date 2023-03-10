---
UID: NF:tapi3if.ITFileTerminalEvent.get_Call
title: ITFileTerminalEvent::get_Call (tapi3if.h)
description: The get_Call method gets a pointer to the call information interface for the call on which the event has occurred. (ITFileTerminalEvent.get_Call)
helpviewer_keywords: ["ITFileTerminalEvent interface [TAPI 2.2]","get_Call method","ITFileTerminalEvent.get_Call","ITFileTerminalEvent::get_Call","_tapi3_itfileterminalevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITFileTerminalEvent interface","tapi3.itfileterminalevent_get_call","tapi3if/ITFileTerminalEvent::get_Call"]
old-location: tapi3\itfileterminalevent_get_call.htm
tech.root: tapi3
ms.assetid: 4a9745a7-8119-41a0-b09a-3475f2390d4d
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Call method, ITFileTerminalEvent.get_Call, ITFileTerminalEvent::get_Call, _tapi3_itfileterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_call, tapi3if/ITFileTerminalEvent::get_Call
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
 - ITFileTerminalEvent::get_Call
 - tapi3if/ITFileTerminalEvent::get_Call
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
 - ITFileTerminalEvent.get_Call
---

# ITFileTerminalEvent::get_Call


## -description

The 
<b>get_Call</b> method gets a pointer to the call information interface for the call on which the event has occurred.

## -parameters

### -param ppCall [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a terminal must generate an event, it requires a selected track in order to pass the event to an MSP which will then pass it to the application through TAPI. The first track that accepts the task of sending the event will be used. If the terminal has more than one track and the tracks are selected onto streams that belong to different calls, the call object pointer eventually returned could be for any of those calls.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>
