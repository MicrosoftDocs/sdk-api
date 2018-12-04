---
UID: NF:rpcasync.RpcAsyncCompleteCall
title: RpcAsyncCompleteCall function
author: windows-sdk-content
description: The client and the server call the RpcAsyncCompleteCall function to complete an asynchronous remote procedure call.
old-location: rpc\rpcasynccompletecall.htm
tech.root: rpc
ms.assetid: 76b6bc3a-f5d1-4780-8071-9b221a6fd7d8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RpcAsyncCompleteCall, RpcAsyncCompleteCall function [RPC], _rpc_rpcasynccompletecall, rpc.rpcasynccompletecall, rpcasync/RpcAsyncCompleteCall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcAsyncCompleteCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcAsyncCompleteCall function


## -description


The client and the server call the 
<b>RpcAsyncCompleteCall</b> function to complete an asynchronous remote procedure call.


## -parameters




### -param pAsync

Pointer to the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.


### -param Reply

Pointer to a buffer containing the return value of the remote procedure call.


## -returns



In addition to the following values, 
<b>RpcAsyncCompleteCall</b> can also return any general RPC or application-specific error. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous call handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ASYNC_CALL_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call has not yet completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The call was canceled.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Completes the asynchronous RPC call. Both client and server call this function.

Client: <i>Reply</i> points to a buffer that will receive the reply. If the client calls this function before the reply has arrived, the call returns RPC_S_ASYNC_CALL_PENDING. The buffer must be valid and it must be big enough to receive the return value. If this call is successful, the 
				<a href="https://msdn.microsoft.com/f92ef78a-321b-460e-a18a-b63a5e199ad0">[out]</a> and the 
				<a href="https://msdn.microsoft.com/85d5617e-8b73-449a-9627-2c8d5ab2b629">[in,</a> <b>out]</b> parameters are valid. If the call does not return RPC_S_ASYNC_CALL_PENDING, this 
<b>RpcAsyncCompleteCall</b> invocation is final for the RPC call. After this function call, regardless of success or failure, all resources allocated by the RPC runtime are freed. Subsequent calls to the 
<b>RpcAsyncCompleteCall</b> or 
<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a> functions have undefined results until a new call on the RPC_ASYNC_STATE structure is initiated.

Server: <i>Reply</i> points to a buffer that contains the return value that needs to be sent to the client. You only need to set a valid buffer for <i>Reply</i> if your function is declared with a return type.  Before a call to 
<b>RpcAsyncCompleteCall</b> is made, the <a href="https://msdn.microsoft.com/f92ef78a-321b-460e-a18a-b63a5e199ad0">[out]</a> and 
				<a href="https://msdn.microsoft.com/85d5617e-8b73-449a-9627-2c8d5ab2b629">[in,</a> <b>out]</b> parameters must be updated. These parameters, and the asynchronous handle, should not be touched after the call to 
<b>RpcAsyncCompleteCall</b> returns. The invocation of <b>RpcAsyncCompleteCall</b> on the server is final. If the  <b>RpcAsyncCompleteCall</b> function call fails, the RPC runtime frees the parameters.

Any <a href="https://msdn.microsoft.com/f92ef78a-321b-460e-a18a-b63a5e199ad0">[out]</a> parameters, including 
				<a href="https://msdn.microsoft.com/3ea9ce62-8bd4-40fe-b838-bfebd52b5a15">[comm_status]</a> and 
				<a href="https://msdn.microsoft.com/">[fault_status]</a> parameters, are only valid if the return value of 
<b>RpcAsyncCompleteCall</b> is RPC_S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/7dfc9f84-ce3c-49f3-8f72-b212095133fd">Error Handling</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>



<a href="https://msdn.microsoft.com/651c53f3-8bb5-4162-a8a8-2da5a0d05d21">RpcAsyncAbortCall</a>



<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a>



<a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>



<a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a>



<a href="https://msdn.microsoft.com/97121e6c-af5c-4da8-ad28-24b961c105d2">RpcAsyncInitializeHandle</a>



<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

