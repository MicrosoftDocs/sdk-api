---
UID: NF:tapi3.ITAgent.CreateSessionWithPIN
title: ITAgent::CreateSessionWithPIN (tapi3.h)
description: The ITAgent::CreateSessionWithPIN method (tapi3.h) creates a new agent session for the input ACD group and address, with Personal Identification Number (PIN).
helpviewer_keywords: ["CreateSessionWithPIN","CreateSessionWithPIN method [TAPI 2.2]","CreateSessionWithPIN method [TAPI 2.2]","ITAgent interface","ITAgent interface [TAPI 2.2]","CreateSessionWithPIN method","ITAgent.CreateSessionWithPIN","ITAgent::CreateSessionWithPIN","_tapi3_itagent_createsessionwithpin","tapi3.itagent_createsessionwithpin","tapi3cc/ITAgent::CreateSessionWithPIN"]
old-location: tapi3\itagent_createsessionwithpin.htm
tech.root: tapi3
ms.assetid: d901ad31-8ccc-4bca-9413-dff838a33088
ms.date: 08/09/2022
ms.keywords: CreateSessionWithPIN, CreateSessionWithPIN method [TAPI 2.2], CreateSessionWithPIN method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],CreateSessionWithPIN method, ITAgent.CreateSessionWithPIN, ITAgent::CreateSessionWithPIN, _tapi3_itagent_createsessionwithpin, tapi3.itagent_createsessionwithpin, tapi3cc/ITAgent::CreateSessionWithPIN
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
 - ITAgent::CreateSessionWithPIN
 - tapi3/ITAgent::CreateSessionWithPIN
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
 - ITAgent.CreateSessionWithPIN
---

# ITAgent::CreateSessionWithPIN


## -description

The 
<b>CreateSessionWithPIN</b> method creates a new agent session for the input ACD group and address, with Personal Identification Number (PIN).

## -parameters

### -param pACDGroup [in]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface.

### -param pAddress [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface for object available for receiving ACD calls.

### -param pPIN [in]

Pointer to a <b>BSTR</b> representation of agent's PIN.

### -param ppAgentSession [out]

Pointer to session created.

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
<dt><b>TAPI_E_CALLCENTER_NO_AGENT_ID</b></dt>
</dl>
</td>
<td width="60%">
Agent not created by 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagentwithid">CreateAgentWithID</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPIN</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPIN</i> or <i>ppAgentSession</i> parameter is not a valid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for <i>pPIN</i> and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface returned by <b>ITAgent::CreateSessionWithPIN</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>
