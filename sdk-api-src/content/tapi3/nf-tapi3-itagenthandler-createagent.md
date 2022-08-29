---
UID: NF:tapi3.ITAgentHandler.CreateAgent
title: ITAgentHandler::CreateAgent (tapi3.h)
description: The CreateAgent method (tapi3.h) creates an Agent object.
helpviewer_keywords: ["CreateAgent","CreateAgent method [TAPI 2.2]","CreateAgent method [TAPI 2.2]","ITAgentHandler interface","ITAgentHandler interface [TAPI 2.2]","CreateAgent method","ITAgentHandler.CreateAgent","ITAgentHandler::CreateAgent","_tapi3_itagenthandler_createagent","tapi3.itagenthandler_createagent","tapi3cc/ITAgentHandler::CreateAgent"]
old-location: tapi3\itagenthandler_createagent.htm
tech.root: tapi3
ms.assetid: f3242013-59a6-40f9-9bb1-0bc30f27311c
ms.date: 08/09/2022
ms.keywords: CreateAgent, CreateAgent method [TAPI 2.2], CreateAgent method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],CreateAgent method, ITAgentHandler.CreateAgent, ITAgentHandler::CreateAgent, _tapi3_itagenthandler_createagent, tapi3.itagenthandler_createagent, tapi3cc/ITAgentHandler::CreateAgent
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
 - ITAgentHandler::CreateAgent
 - tapi3/ITAgentHandler::CreateAgent
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
 - ITAgentHandler.CreateAgent
---

# ITAgentHandler::CreateAgent


## -description

The 
<b>CreateAgent</b> method creates an Agent object.

## -parameters

### -param ppAgent [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface.

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
The <i>ppAgent</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface returned by <b>ITAgentHandler::CreateAgent</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagentwithid">CreateAgentWithID</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>
