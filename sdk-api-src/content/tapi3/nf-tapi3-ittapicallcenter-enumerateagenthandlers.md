---
UID: NF:tapi3.ITTAPICallCenter.EnumerateAgentHandlers
title: ITTAPICallCenter::EnumerateAgentHandlers (tapi3.h)
description: The ITTAPICallCenter::EnumerateAgentHandlers (tapi3.h) method enumerates agent handlers that are currently associated with the call center.
helpviewer_keywords: ["EnumerateAgentHandlers","EnumerateAgentHandlers method [TAPI 2.2]","EnumerateAgentHandlers method [TAPI 2.2]","ITTAPICallCenter interface","ITTAPICallCenter interface [TAPI 2.2]","EnumerateAgentHandlers method","ITTAPICallCenter.EnumerateAgentHandlers","ITTAPICallCenter::EnumerateAgentHandlers","_tapi3_ittapicallcenter_enumerateagenthandlers","tapi3.ittapicallcenter_enumerateagenthandlers","tapi3cc/ITTAPICallCenter::EnumerateAgentHandlers"]
old-location: tapi3\ittapicallcenter_enumerateagenthandlers.htm
tech.root: tapi3
ms.assetid: 5bd0a926-0d99-4efe-a995-28654c97c97a
ms.date: 08/10/2022
ms.keywords: EnumerateAgentHandlers, EnumerateAgentHandlers method [TAPI 2.2], EnumerateAgentHandlers method [TAPI 2.2],ITTAPICallCenter interface, ITTAPICallCenter interface [TAPI 2.2],EnumerateAgentHandlers method, ITTAPICallCenter.EnumerateAgentHandlers, ITTAPICallCenter::EnumerateAgentHandlers, _tapi3_ittapicallcenter_enumerateagenthandlers, tapi3.ittapicallcenter_enumerateagenthandlers, tapi3cc/ITTAPICallCenter::EnumerateAgentHandlers
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
 - ITTAPICallCenter::EnumerateAgentHandlers
 - tapi3/ITTAPICallCenter::EnumerateAgentHandlers
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
 - ITTAPICallCenter.EnumerateAgentHandlers
---

# ITTAPICallCenter::EnumerateAgentHandlers


## -description

The 
<b>EnumerateAgentHandlers</b> method enumerates agent handlers that are currently associated with the call center. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-get_agenthandlers">get_AgentHandlers</a> method.

## -parameters

### -param ppEnumHandler [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a> enumerator.

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
The <i>ppEnumHandler</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

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
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a> interface returned by <b>tapi3.ittapicallcenter_enumerateagenthandlers</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentHandler</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-ittapicallcenter">ITTAPICallCenter</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
