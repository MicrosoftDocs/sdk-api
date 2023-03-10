---
UID: NF:tapi3cc.ITAgent.get_AgentSessions
title: ITAgent::get_AgentSessions (tapi3cc.h)
description: The ITAgent::get_AgentSessions method (tapi3cc.h) creates a collection of current agent sessions.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_AgentSessions method","ITAgent.get_AgentSessions","ITAgent::get_AgentSessions","_tapi3_itagent_get_agentsessions","get_AgentSessions","get_AgentSessions method [TAPI 2.2]","get_AgentSessions method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_agentsessions","tapi3cc/ITAgent::get_AgentSessions"]
old-location: tapi3\itagent_get_agentsessions.htm
tech.root: tapi3
ms.assetid: 25503eae-ebee-4b57-ab5c-b3f152de9a96
ms.date: 08/10/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_AgentSessions method, ITAgent.get_AgentSessions, ITAgent::get_AgentSessions, _tapi3_itagent_get_agentsessions, get_AgentSessions, get_AgentSessions method [TAPI 2.2], get_AgentSessions method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_agentsessions, tapi3cc/ITAgent::get_AgentSessions
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
 - ITAgent::get_AgentSessions
 - tapi3cc/ITAgent::get_AgentSessions
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
 - ITAgent.get_AgentSessions
---

# ITAgent::get_AgentSessions


## -description

The 
<b>get_AgentSessions</b> method creates a collection of current agent sessions. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-enumerateagentsessions">EnumerateAgentSessions</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface pointers (agent session objects).

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

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
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface returned by <b>ITAgent::get_AgentSessions</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-enumerateagentsessions">EnumerateAgentSessions</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<b>ITAgentSession</b>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>
