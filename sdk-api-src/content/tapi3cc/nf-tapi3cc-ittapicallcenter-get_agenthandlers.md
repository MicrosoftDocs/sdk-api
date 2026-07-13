---
UID: NF:tapi3cc.ITTAPICallCenter.get_AgentHandlers
title: ITTAPICallCenter::get_AgentHandlers (tapi3cc.h)
description: The ITTAPICallCenter::get_AgentHandlers method (tapi3cc.h) creates a collection of agent handlers that are currently associated with the call center.
helpviewer_keywords: ["ITTAPICallCenter interface [TAPI 2.2]","get_AgentHandlers method","ITTAPICallCenter.get_AgentHandlers","ITTAPICallCenter::get_AgentHandlers","_tapi3_ittapicallcenter_get_agenthandlers","get_AgentHandlers","get_AgentHandlers method [TAPI 2.2]","get_AgentHandlers method [TAPI 2.2]","ITTAPICallCenter interface","tapi3.ittapicallcenter_get_agenthandlers","tapi3cc/ITTAPICallCenter::get_AgentHandlers"]
old-location: tapi3\ittapicallcenter_get_agenthandlers.htm
tech.root: tapi3
ms.assetid: 61972ea2-d3ab-4893-8fc6-cd3c10f8584e
ms.date: 08/10/2022
ms.keywords: ITTAPICallCenter interface [TAPI 2.2],get_AgentHandlers method, ITTAPICallCenter.get_AgentHandlers, ITTAPICallCenter::get_AgentHandlers, _tapi3_ittapicallcenter_get_agenthandlers, get_AgentHandlers, get_AgentHandlers method [TAPI 2.2], get_AgentHandlers method [TAPI 2.2],ITTAPICallCenter interface, tapi3.ittapicallcenter_get_agenthandlers, tapi3cc/ITTAPICallCenter::get_AgentHandlers
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
 - ITTAPICallCenter::get_AgentHandlers
 - tapi3cc/ITTAPICallCenter::get_AgentHandlers
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
 - ITTAPICallCenter.get_AgentHandlers
---

# ITTAPICallCenter::get_AgentHandlers


## -description

The 
<b>get_AgentHandlers</b> method creates a collection of agent handlers that are currently associated with the call center. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-enumerateagenthandlers">EnumerateAgentHandlers</a> method.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface pointers.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not valid.

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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface returned by <b>ITTAPICallCenter::get_AgentHandlers</b>. The application must call <b>Release</b> on the 
<b>ITAgentHandler</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-ittapicallcenter">ITTAPICallCenter</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
