---
UID: NF:rpcasync.RpcAsyncAbortCall
title: RpcAsyncAbortCall function
author: windows-driver-content
description: The server calls RpcAsyncAbortCall to abort an asynchronous call.
old-location: rpc\rpcasyncabortcall.htm
old-project: Rpc
ms.assetid: 651c53f3-8bb5-4162-a8a8-2da5a0d05d21
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcAsyncAbortCall, RpcAsyncAbortCall function [RPC], _rpc_rpcasyncabortcall, rpc.rpcasyncabortcall, rpcasync/RpcAsyncAbortCall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcAsyncAbortCall
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcAsyncAbortCall function


## -description



			The server calls 
<b>RpcAsyncAbortCall</b> to abort an asynchronous call.


## -parameters




### -param pAsync

Pointer to the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.


### -param ExceptionCode

A nonzero application-specific exception code. Can be an application-defined error code, or a standard RPC error code. For more information, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.


## -returns



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
Call cancelation successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Asynchronous handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The server calls 
<b>RpcAsyncAbortCall</b> when circumstances require it to abort an asynchronous call before completion. For example, the caller may not have the necessary permissions to make the request, or the server may be too busy to process the call. Use the <i>ExceptionCode</i> parameter to specify the reason for the abort. The run-time environment propagates the exception code to the client as a fault.

When an asynchronous call is aborted with 
<b>RpcAsyncAbortCall</b>, no marshaling of the output arguments is performed, and all input arguments are freed by RPC. When 
<b>RpcAsyncAbortCall</b> is called, a call to the 
<b>RpcAsyncCompleteCall</b> function is not necessary. The 
<b>RpcAsyncAbortCall</b> function should be called only once for any asynchronous call; a second call may crash the process or fail in other unexpected ways.




## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>



<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a>



<a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a>



<a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>



<a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a>



<a href="https://msdn.microsoft.com/97121e6c-af5c-4da8-ad28-24b961c105d2">RpcAsyncInitializeHandle</a>



<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

