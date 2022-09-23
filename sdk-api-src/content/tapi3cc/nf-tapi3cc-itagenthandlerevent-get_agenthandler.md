---
UID: NF:tapi3cc.ITAgentHandlerEvent.get_AgentHandler
title: ITAgentHandlerEvent::get_AgentHandler (tapi3cc.h)
description: The ITAgentHandlerEvent::get_AgentHandler method (tapi3cc.h) gets the ITAgentHandler interface pointer.
helpviewer_keywords: ["ITAgentHandlerEvent interface [TAPI 2.2]","get_AgentHandler method","ITAgentHandlerEvent.get_AgentHandler","ITAgentHandlerEvent::get_AgentHandler","_tapi3_itagenthandlerevent_get_agenthandler","get_AgentHandler","get_AgentHandler method [TAPI 2.2]","get_AgentHandler method [TAPI 2.2]","ITAgentHandlerEvent interface","tapi3.itagenthandlerevent_get_agenthandler","tapi3cc/ITAgentHandlerEvent::get_AgentHandler"]
old-location: tapi3\itagenthandlerevent_get_agenthandler.htm
tech.root: tapi3
ms.assetid: 7288edb3-e7df-4e31-815d-dc8fc44bb5bc
ms.date: 08/10/2022
ms.keywords: ITAgentHandlerEvent interface [TAPI 2.2],get_AgentHandler method, ITAgentHandlerEvent.get_AgentHandler, ITAgentHandlerEvent::get_AgentHandler, _tapi3_itagenthandlerevent_get_agenthandler, get_AgentHandler, get_AgentHandler method [TAPI 2.2], get_AgentHandler method [TAPI 2.2],ITAgentHandlerEvent interface, tapi3.itagenthandlerevent_get_agenthandler, tapi3cc/ITAgentHandlerEvent::get_AgentHandler
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
 - ITAgentHandlerEvent::get_AgentHandler
 - tapi3cc/ITAgentHandlerEvent::get_AgentHandler
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
 - ITAgentHandlerEvent.get_AgentHandler
---

# ITAgentHandlerEvent::get_AgentHandler


## -description

The 
<b>get_AgentHandler</b> method gets the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface pointer.

## -parameters

### -param ppAgentHandler [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface on which the event occurred.

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
The <i>ppAgentHandler</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface returned by <b>ITAgentHandlerEvent::get_AgentHandler</b>. The application must call <b>Release</b> on the 
<b>ITAgentHandler</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandlerevent">ITAgentHandlerEvent</a>
