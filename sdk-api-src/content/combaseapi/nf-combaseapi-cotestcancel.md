---
UID: NF:combaseapi.CoTestCancel
title: CoTestCancel function
author: windows-sdk-content
description: Determines whether the call being executed on the server has been canceled by the client.
old-location: com\cotestcancel.htm
old-project: com
ms.assetid: 9432621a-be31-4b8b-83b6-069539ba06b4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CoTestCancel, CoTestCancel function [COM], _com_CoTestCancel, com.cotestcancel, combaseapi/CoTestCancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoTestCancel
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoTestCancel function


## -description


Determines whether the call being executed on the server has been canceled by the client.


## -parameters






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

<b>CoTestCancel</b> calls <a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a> to obtain the <a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a> interface on the current cancel object and then calls <a href="https://msdn.microsoft.com/31141d97-241e-4717-b707-e37d86c2267d">ICancelMethodCalls::TestCancel</a>. Objects that implement custom marshaling should first call <a href="https://msdn.microsoft.com/146855a2-97ec-4e71-88dc-316eaa1a24a0">CoSwitchCallContext</a> to install the appropriate call context object.

This function does not test cancellation for asynchronous calls.




## -see-also




<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 

