---
UID: NF:combaseapi.CoCancelCall
title: CoCancelCall function (combaseapi.h)
description: Requests cancellation of an outbound DCOM method call pending on a specified thread.
helpviewer_keywords: ["CoCancelCall","CoCancelCall function [COM]","_com_CoCancelCall","com.cocancelcall","combaseapi/CoCancelCall"]
old-location: com\cocancelcall.htm
tech.root: com
ms.assetid: 1707261c-2d8d-4f35-865d-61c8870c0624
ms.date: 12/05/2018
ms.keywords: CoCancelCall, CoCancelCall function [COM], _com_CoCancelCall, com.cocancelcall, combaseapi/CoCancelCall
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
 - CoCancelCall
 - combaseapi/CoCancelCall
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
 - CoCancelCall
---

# CoCancelCall function


## -description

Requests cancellation of an outbound DCOM method call pending on a specified thread.

## -parameters

### -param dwThreadId [in]

The identifier of the thread on which the pending DCOM call is to be canceled. If this parameter is 0, the call is on the current thread.

### -param ulTimeout [in]

The number of seconds <b>CoCancelCall</b> waits for the server to complete the outbound call after the client requests cancellation.

## -returns

This function can return the standard return values E_FAIL, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The cancellation request was made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
There is no cancel object corresponding to the specified thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CANCEL_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Call cancellation is not enabled on the specified thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CALL_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The call was completed during the timeout interval.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CALL_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The call was already canceled.

</td>
</tr>
</table>

## -remarks

<b>CoCancelCall</b> calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject">CoGetCancelObject</a> and then <a href="/windows/desktop/api/objidl/nf-objidl-icancelmethodcalls-cancel">ICancelMethodCalls::Cancel</a> on the cancel object for the call being executed.

This function does not locate cancel objects for asynchronous calls.

The object server can determine if the call has been canceled by periodically calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel">CoTestCancel</a>. If the call has been canceled, the object server should clean up and return control to the client.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel">CoTestCancel</a>