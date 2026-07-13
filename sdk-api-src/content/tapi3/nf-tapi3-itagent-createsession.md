---
UID: NF:tapi3.ITAgent.CreateSession
title: ITAgent::CreateSession (tapi3.h)
description: The ITAgent::CreateSession method (tapi3.h) creates a new agent session for the input ACD group and address.
helpviewer_keywords: ["CreateSession","CreateSession method [TAPI 2.2]","CreateSession method [TAPI 2.2]","ITAgent interface","ITAgent interface [TAPI 2.2]","CreateSession method","ITAgent.CreateSession","ITAgent::CreateSession","_tapi3_itagent_createsession","tapi3.itagent_createsession","tapi3cc/ITAgent::CreateSession"]
old-location: tapi3\itagent_createsession.htm
tech.root: tapi3
ms.assetid: 68cc2ffe-3c63-4723-8652-0e28da2b17b6
ms.date: 08/09/2022
ms.keywords: CreateSession, CreateSession method [TAPI 2.2], CreateSession method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],CreateSession method, ITAgent.CreateSession, ITAgent::CreateSession, _tapi3_itagent_createsession, tapi3.itagent_createsession, tapi3cc/ITAgent::CreateSession
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
 - ITAgent::CreateSession
 - tapi3/ITAgent::CreateSession
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
 - ITAgent.CreateSession
---

# ITAgent::CreateSession


## -description

The 
<b>CreateSession</b> method creates a new agent session for the input ACD group and address.

## -parameters

### -param pACDGroup [in]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface.

### -param pAddress [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> object available for receiving ACD calls.

### -param ppAgentSession [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface for object created.

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
The <i>ppAgentSession</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed to open a line for the target Address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pACDGroup</i> or <i>pAddress</i> argument is not valid.

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

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface returned by <b>ITAgent::CreateSession</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.

Some telephone environments require a personal identification number to open a session. See 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsessionwithpin">CreateSessionWithPIN</a>.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsessionwithpin">ITAgent::CreateSessionWithPIN</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>
