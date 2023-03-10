---
UID: NF:tapi3if.ITFileTerminalEvent.get_Cause
title: ITFileTerminalEvent::get_Cause (tapi3if.h)
description: The get_Cause method gets the cause associated with this event. (ITFileTerminalEvent.get_Cause)
helpviewer_keywords: ["ITFileTerminalEvent interface [TAPI 2.2]","get_Cause method","ITFileTerminalEvent.get_Cause","ITFileTerminalEvent::get_Cause","_tapi3_itfileterminalevent_get_cause","get_Cause","get_Cause method [TAPI 2.2]","get_Cause method [TAPI 2.2]","ITFileTerminalEvent interface","tapi3.itfileterminalevent_get_cause","tapi3if/ITFileTerminalEvent::get_Cause"]
old-location: tapi3\itfileterminalevent_get_cause.htm
tech.root: tapi3
ms.assetid: 90594778-712e-4d26-9fe5-cb5cfd240359
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Cause method, ITFileTerminalEvent.get_Cause, ITFileTerminalEvent::get_Cause, _tapi3_itfileterminalevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_cause, tapi3if/ITFileTerminalEvent::get_Cause
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
 - ITFileTerminalEvent::get_Cause
 - tapi3if/ITFileTerminalEvent::get_Cause
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
 - ITFileTerminalEvent.get_Cause
---

# ITFileTerminalEvent::get_Cause


## -description

The 
<b>get_Cause</b> method gets the cause associated with this event.

## -parameters

### -param pCause [out]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-ft_state_event_cause">FT_STATE_EVENT_CAUSE</a> descriptor of the cause of this event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>
