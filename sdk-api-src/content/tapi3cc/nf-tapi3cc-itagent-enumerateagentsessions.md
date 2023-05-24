---
UID: NF:tapi3cc.ITAgent.EnumerateAgentSessions
title: ITAgent::EnumerateAgentSessions (tapi3cc.h)
description: The ITAgent::EnumerateAgentSessions method (tapi3cc.h) enumerates the current agent sessions.
helpviewer_keywords: ["EnumerateAgentSessions","EnumerateAgentSessions method [TAPI 2.2]","EnumerateAgentSessions method [TAPI 2.2]","ITAgent interface","ITAgent interface [TAPI 2.2]","EnumerateAgentSessions method","ITAgent.EnumerateAgentSessions","ITAgent::EnumerateAgentSessions","_tapi3_itagent_enumerateagentsessions","tapi3.itagent_enumerateagentsessions","tapi3cc/ITAgent::EnumerateAgentSessions"]
old-location: tapi3\itagent_enumerateagentsessions.htm
tech.root: tapi3
ms.assetid: 6b639a41-c866-49ad-bc33-1215da7c8a19
ms.date: 08/10/2022
ms.keywords: EnumerateAgentSessions, EnumerateAgentSessions method [TAPI 2.2], EnumerateAgentSessions method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],EnumerateAgentSessions method, ITAgent.EnumerateAgentSessions, ITAgent::EnumerateAgentSessions, _tapi3_itagent_enumerateagentsessions, tapi3.itagent_enumerateagentsessions, tapi3cc/ITAgent::EnumerateAgentSessions
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
 - ITAgent::EnumerateAgentSessions
 - tapi3cc/ITAgent::EnumerateAgentSessions
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
 - ITAgent.EnumerateAgentSessions
---

# ITAgent::EnumerateAgentSessions


## -description

The 
<b>EnumerateAgentSessions</b> method enumerates the current agent sessions. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_agentsessions">get_AgentSessions</a> method.

## -parameters

### -param ppEnumAgentSession [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a> agent session enumerator.

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
The <b>ppEnumAgentSession</b> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a> interface returned by <b>ITAgent::EnumerateAgentSessions</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentSession</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsessionwithpin">ITAgent::CreateSessionWithPIN</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_agentsessions">get_AgentSessions</a>
