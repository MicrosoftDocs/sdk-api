---
UID: NF:tapi3cc.ITAgentHandlerEvent.get_Event
title: ITAgentHandlerEvent::get_Event (tapi3cc.h)
description: The get_Event method gets the description for the event that has occurred.helpviewer_keywords: ["ITAgentHandlerEvent interface [TAPI 2.2]","get_Event method","ITAgentHandlerEvent.get_Event","ITAgentHandlerEvent::get_Event","_tapi3_itagenthandlerevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITAgentHandlerEvent interface","tapi3.itagenthandlerevent_get_event","tapi3cc/ITAgentHandlerEvent::get_Event"]
old-location: tapi3\itagenthandlerevent_get_event.htm
tech.root: Tapi
ms.assetid: 3362964c-15d3-497c-876b-46e8d26389c0
ms.date: 12/05/2018
ms.keywords: ITAgentHandlerEvent interface [TAPI 2.2],get_Event method, ITAgentHandlerEvent.get_Event, ITAgentHandlerEvent::get_Event, _tapi3_itagenthandlerevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentHandlerEvent interface, tapi3.itagenthandlerevent_get_event, tapi3cc/ITAgentHandlerEvent::get_Event
f1_keywords:
- tapi3cc/ITAgentHandlerEvent.get_Event
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITAgentHandlerEvent.get_Event
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentHandlerEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the description for the event that has occurred.


## -parameters




### -param pEvent [out]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agenthandler_event">AGENTHANDLER_EVENT</a> descriptor.


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agenthandler_event">AGENTHANDLER_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandlerevent">ITAgentHandlerEvent</a>
 

 

