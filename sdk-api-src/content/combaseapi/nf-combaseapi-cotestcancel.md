---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

