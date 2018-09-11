---
UID: NF:rpcasync.RpcAsyncInitializeHandle
title: RpcAsyncInitializeHandle function
author: windows-sdk-content
description: The client calls the RpcAsyncInitializeHandle function to initialize the RPC_ASYNC_STATE structure to be used to make an asynchronous call.
old-location: rpc\rpcasyncinitializehandle.htm
tech.root: Rpc
ms.assetid: 97121e6c-af5c-4da8-ad28-24b961c105d2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcAsyncInitializeHandle, RpcAsyncInitializeHandle function [RPC], _rpc_rpcasyncinitializehandle, rpc.rpcasyncinitializehandle, rpcasync/RpcAsyncInitializeHandle
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
 - RpcAsyncInitializeHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcAsyncInitializeHandle function


## -description


The client calls the 
<b>RpcAsyncInitializeHandle</b> function to initialize the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure to be used to make an asynchronous call.


## -parameters




### -param pAsync

Pointer to the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.


### -param Size

Size of the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure.


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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The size is either too small or too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>pAsync</i> points to invalid memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The client creates a new 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure and a pointer to that structure and calls 
<b>RpcAsyncInitializeHandle</b> with the pointer as an input parameter. The 
<b>RpcAsyncInitializeHandle</b> function initializes the fields that it uses to maintain the state of an asynchronous remote call. When the call to 
<b>RpcAsyncInitializeHandle</b> returns successfully, the client can set the notification type and any fields related to that notification type in the 
<b>RPC_ASYNC_STATE</b> structure. The client application uses a pointer to this structure to make an asynchronous call.

The client should not attempt to alter the <b>Size</b>, <b>Signature</b>, <b>Lock</b>, and <b>StubInfo</b> members of the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure; doing so will invalidate the handle.

<div class="alert"><b>Note</b>  In Windows 2000, after an asynchronous call is completed, the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure must be reinitialized prior to being used for another asynchronous call. In Windows XP and later, the 
<b>RPC_ASYNC_STATE</b> structure is ready for immediate re-use subsequent to a completed asynchronous call.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>



<a href="https://msdn.microsoft.com/651c53f3-8bb5-4162-a8a8-2da5a0d05d21">RpcAsyncAbortCall</a>



<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a>



<a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a>



<a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>



<a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a>



<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

