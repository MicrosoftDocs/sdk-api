---
UID: NF:tapi3.ITAgentEvent.get_Agent
title: ITAgentEvent::get_Agent (tapi3.h)
description: The get_Agent method gets the interface for the agent on which the event occurred.
helpviewer_keywords: ["ITAgentEvent interface [TAPI 2.2]","get_Agent method","ITAgentEvent.get_Agent","ITAgentEvent::get_Agent","_tapi3_itagentevent_get_agent","get_Agent","get_Agent method [TAPI 2.2]","get_Agent method [TAPI 2.2]","ITAgentEvent interface","tapi3.itagentevent_get_agent","tapi3cc/ITAgentEvent::get_Agent"]
old-location: tapi3\itagentevent_get_agent.htm
tech.root: tapi3
ms.assetid: 90a1684d-5cb0-4d1b-ac38-b03f9f1ff838
ms.date: 12/05/2018
ms.keywords: ITAgentEvent interface [TAPI 2.2],get_Agent method, ITAgentEvent.get_Agent, ITAgentEvent::get_Agent, _tapi3_itagentevent_get_agent, get_Agent, get_Agent method [TAPI 2.2], get_Agent method [TAPI 2.2],ITAgentEvent interface, tapi3.itagentevent_get_agent, tapi3cc/ITAgentEvent::get_Agent
f1_keywords:
- tapi3/ITAgentEvent.get_Agent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITAgentEvent.get_Agent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentEvent::get_Agent


## -description


The 
<b>get_Agent</b> method gets the interface for the agent on which the event occurred.


## -parameters




### -param ppAgent [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface.


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
The <i>ppAgent</i> parameter is not a valid pointer.

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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface returned by <b>ITAgentEvent::get_Agent</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagentevent">ITAgentEvent</a>
 

 

