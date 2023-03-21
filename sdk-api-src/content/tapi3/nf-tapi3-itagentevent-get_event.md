---
UID: NF:tapi3.ITAgentEvent.get_Event
title: ITAgentEvent::get_Event (tapi3.h)
description: The ITAgentEvent::get_Event method (tapi3.h) gets an AGENT_EVENT descriptor of the event that occurred.
helpviewer_keywords: ["ITAgentEvent interface [TAPI 2.2]","get_Event method","ITAgentEvent.get_Event","ITAgentEvent::get_Event","_tapi3_itagentevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITAgentEvent interface","tapi3.itagentevent_get_event","tapi3cc/ITAgentEvent::get_Event"]
old-location: tapi3\itagentevent_get_event.htm
tech.root: tapi3
ms.assetid: d402b2b4-2817-4ebe-b735-69ea9e975f54
ms.date: 08/09/2022
ms.keywords: ITAgentEvent interface [TAPI 2.2],get_Event method, ITAgentEvent.get_Event, ITAgentEvent::get_Event, _tapi3_itagentevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentEvent interface, tapi3.itagentevent_get_event, tapi3cc/ITAgentEvent::get_Event
req.header: tapi3.h
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
 - ITAgentEvent::get_Event
 - tapi3/ITAgentEvent::get_Event
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
 - ITAgentEvent.get_Event
---

# ITAgentEvent::get_Event


## -description

Gets an 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_event">AGENT_EVENT</a> descriptor of the event that occurred.

## -parameters

### -param pEvent [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_event">AGENT_EVENT</a> descriptor of event.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_event">AGENT_EVENT</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentevent">ITAgentEvent</a>
