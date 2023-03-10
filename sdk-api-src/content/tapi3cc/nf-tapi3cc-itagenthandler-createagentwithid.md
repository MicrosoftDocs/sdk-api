---
UID: NF:tapi3cc.ITAgentHandler.CreateAgentWithID
title: ITAgentHandler::CreateAgentWithID (tapi3cc.h)
description: The ITAgentHandler::CreateAgentWithID method (tapi3cc.h) creates an Agent object based on an agent identifier.
helpviewer_keywords: ["CreateAgentWithID","CreateAgentWithID method [TAPI 2.2]","CreateAgentWithID method [TAPI 2.2]","ITAgentHandler interface","ITAgentHandler interface [TAPI 2.2]","CreateAgentWithID method","ITAgentHandler.CreateAgentWithID","ITAgentHandler::CreateAgentWithID","_tapi3_itagenthandler_createagentwithid","tapi3.itagenthandler_createagentwithid","tapi3cc/ITAgentHandler::CreateAgentWithID"]
old-location: tapi3\itagenthandler_createagentwithid.htm
tech.root: tapi3
ms.assetid: 95c70e48-b990-47c7-a8b8-5fa3a84ec5ba
ms.date: 08/10/2022
ms.keywords: CreateAgentWithID, CreateAgentWithID method [TAPI 2.2], CreateAgentWithID method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],CreateAgentWithID method, ITAgentHandler.CreateAgentWithID, ITAgentHandler::CreateAgentWithID, _tapi3_itagenthandler_createagentwithid, tapi3.itagenthandler_createagentwithid, tapi3cc/ITAgentHandler::CreateAgentWithID
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
 - ITAgentHandler::CreateAgentWithID
 - tapi3cc/ITAgentHandler::CreateAgentWithID
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
 - ITAgentHandler.CreateAgentWithID
---

# ITAgentHandler::CreateAgentWithID


## -description

The 
<b>CreateAgentWithID</b> method creates an Agent object based on an agent identifier. This identifier is a string identifying the agent on a legacy ACD system. If the system also requires a PIN or password for logging into groups, you use this method to set the PIN or password.

## -parameters

### -param pID [in]

Pointer to <b>BSTR</b> containing the agent identifier.

### -param pPIN [in]

Pointer to <b>BSTR</b> containing the agent PIN.

### -param ppAgent [out]

Pointer to 
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPIN</i> parameter is <b>NULL</b>.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pID</i> and <i>pPIN</i> parameters, and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variables are no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface returned by <b>ITAgentHandler::CreateAgentWithID</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagent">CreateAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>
