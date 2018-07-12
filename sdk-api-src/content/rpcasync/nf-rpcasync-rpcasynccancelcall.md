---
UID: NF:rpcasync.RpcAsyncCancelCall
title: RpcAsyncCancelCall function
author: windows-sdk-content
description: The client calls the RpcAsyncCancelCall function to cancel an asynchronous call.
old-location: rpc\rpcasynccancelcall.htm
old-project: rpc
ms.assetid: e55d586f-969b-4e9a-97d9-b6c74b2a8b6d
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RpcAsyncCancelCall, RpcAsyncCancelCall function [RPC], _rpc_rpcasynccancelcall, rpc.rpcasynccancelcall, rpcasync/RpcAsyncCancelCall
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcAsyncCancelCall
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcAsyncCancelCall function


## -description


The client calls the 
<b>RpcAsyncCancelCall</b> function to cancel an asynchronous call.


## -parameters




### -param pAsync

Pointer to the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.


### -param fAbort

TBD




#### - fAbortCall

If <b>TRUE</b>, the call is canceled immediately. If <b>FALSE</b>, wait for the server to complete the call.


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
The cancellation request was processed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



There are two ways for a client to request cancellation of an asynchronous call—<b>abortive</b> and <b>nonabortive</b>. In an abortive cancel (<i>fAbortCall</i> is <b>TRUE</b>), the 
<b>RpcAsyncCancelCall</b> function sends a cancel notification to the server and client side and the asynchronous call is canceled immediately, without waiting for a response from the server. Note that in a multithreaded application, an async call can only be canceled by the client after the thread that originated the call has returned from it with success.  This is necessary to ensure that the call will not be canceled asynchronously by another thread after it has failed synchronously while being issued.  In general, if an async call fails synchronously it should not be canceled asynchronously.  The client application must ensure this behavior if calls may be issued and canceled on different threads.

The server checks for cancel requests from the client by calling 
<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>. Depending on the state of the call at the time the cancel request was issued and how often the server checks for cancels, the call may or may not complete normally. The client application must call 
<a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a> to complete the call and the return value will indicate whether the call completed, failed, or was canceled. However, the client must still wait for the original call to complete before calling <b>RpcAsyncCompleteCall</b>.

In a nonabortive cancel (<i>fAbortCall</i> is <b>FALSE</b>) the 
<b>RpcAsyncCancelCall</b> function notifies the server of the cancel and the client waits for the server to complete the call. There is no built-in time-out mechanism. If you want the call to time out, the client should first issue a nonabortive cancel using its own time-out mechanism. If the call times out, then the client can issue an abortive cancel.




## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>



<a href="https://msdn.microsoft.com/651c53f3-8bb5-4162-a8a8-2da5a0d05d21">RpcAsyncAbortCall</a>



<a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a>



<a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>



<a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a>



<a href="https://msdn.microsoft.com/97121e6c-af5c-4da8-ad28-24b961c105d2">RpcAsyncInitializeHandle</a>



<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

