---
UID: NF:tapi3cc.ITAgentSessionEvent.get_Event
title: ITAgentSessionEvent::get_Event (tapi3cc.h)
description: The ITAgentSessionEvent::get_Event method (tapi3cc.h) gets an AGENT_SESSION_EVENT descriptor of the event that occurred.
helpviewer_keywords: ["ITAgentSessionEvent interface [TAPI 2.2]","get_Event method","ITAgentSessionEvent.get_Event","ITAgentSessionEvent::get_Event","_tapi3_itagentsessionevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITAgentSessionEvent interface","tapi3.itagentsessionevent_get_event","tapi3cc/ITAgentSessionEvent::get_Event"]
old-location: tapi3\itagentsessionevent_get_event.htm
tech.root: tapi3
ms.assetid: 34779590-c2f6-4bd7-932b-5ac6365bcb20
ms.date: 08/10/2022
ms.keywords: ITAgentSessionEvent interface [TAPI 2.2],get_Event method, ITAgentSessionEvent.get_Event, ITAgentSessionEvent::get_Event, _tapi3_itagentsessionevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentSessionEvent interface, tapi3.itagentsessionevent_get_event, tapi3cc/ITAgentSessionEvent::get_Event
req.header: tapi3cc.h
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
 - ITAgentSessionEvent::get_Event
 - tapi3cc/ITAgentSessionEvent::get_Event
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
 - ITAgentSessionEvent.get_Event
---

# ITAgentSessionEvent::get_Event


## -description

The 
<b>get_Event</b> method gets an 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_session_event">AGENT_SESSION_EVENT</a> descriptor of the event that occurred.

## -parameters

### -param pEvent [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_session_event">AGENT_SESSION_EVENT</a> descriptor of the event.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_session_event">AGENT_SESSION_EVENT</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsessionevent">ITAgentSessionEvent</a>
