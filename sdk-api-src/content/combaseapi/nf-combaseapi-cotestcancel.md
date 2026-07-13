---
UID: NF:combaseapi.CoTestCancel
title: CoTestCancel function (combaseapi.h)
description: Determines whether the call being executed on the server has been canceled by the client.
helpviewer_keywords: ["CoTestCancel","CoTestCancel function [COM]","_com_CoTestCancel","com.cotestcancel","combaseapi/CoTestCancel"]
old-location: com\cotestcancel.htm
tech.root: com
ms.assetid: 9432621a-be31-4b8b-83b6-069539ba06b4
ms.date: 12/05/2018
ms.keywords: CoTestCancel, CoTestCancel function [COM], _com_CoTestCancel, com.cotestcancel, combaseapi/CoTestCancel
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoTestCancel
 - combaseapi/CoTestCancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoTestCancel
---

# CoTestCancel function


## -description

Determines whether the call being executed on the server has been canceled by the client.



## -returns

This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALLPENDING</b></dt>
</dl>
</td>
<td width="60%">
The call is still pending and has not yet been canceled by the client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CALL_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The call has been canceled by the client.

</td>
</tr>
</table>

## -remarks

Server objects should call <b>CoTestCancel</b> at least once before returning to detect client cancellation requests. Doing so can save the server unnecessary work if the client has issued a cancellation request, and it can reduce the client's wait time if it has set the cancel timeout as RPC_C_CANCEL_INFINITE_TIMEOUT. Furthermore, if the server object detects a cancellation request before returning from a pending call, it can clean up any memory, marshaled interfaces, or handles it has created or obtained. 

<b>CoTestCancel</b> calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a> to obtain the <a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a> interface on the current cancel object and then calls <a href="/windows/desktop/api/objidl/nf-objidl-icancelmethodcalls-testcancel">ICancelMethodCalls::TestCancel</a>. Objects that implement custom marshaling should first call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coswitchcallcontext">CoSwitchCallContext</a> to install the appropriate call context object.

This function does not test cancellation for asynchronous calls.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>
