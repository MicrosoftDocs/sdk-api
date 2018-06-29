---
UID: NF:rpcasync.RpcAsyncGetCallHandle
title: RpcAsyncGetCallHandle macro
author: windows-sdk-content
description: The RpcAsyncGetCallHandle macro returns the binding handle on an asynchronous remote procedure call.
old-location: rpc\rpcasyncgetcallhandle.htm
old-project: Rpc
ms.assetid: 5a218d25-187e-4899-8a27-a955f77af8c2
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcAsyncGetCallHandle, RpcAsyncGetCallHandle macro [RPC], _rpc_rpcasyncgetcallhandle, rpc.rpcasyncgetcallhandle, rpcasync/RpcAsyncGetCallHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: rpcasync.h
req.include-header: Rpc.h
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
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RpcAsyncGetCallHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RpcAsyncGetCallHandle macro


## -description


The <b>RpcAsyncGetCallHandle</b> macro returns the 
    binding handle on an asynchronous remote procedure call.


## -parameters




### -param pAsync

Pointer to the <a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that 
       contains asynchronous call information.


## -remarks



Given an asynchronous handle, it returns the corresponding binding handle. For example, the 
     <a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a> function uses the 
     <i>pAsync</i> parameter of 
     <b>RpcAsyncGetCallHandle</b> as a parameter to test for 
     cancel requests.




## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/783895fc-d57c-46eb-a3ad-25369876b78a">RPC Macros</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>



<a href="https://msdn.microsoft.com/651c53f3-8bb5-4162-a8a8-2da5a0d05d21">RpcAsyncAbortCall</a>



<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a>



<a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a>



<a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a>



<a href="https://msdn.microsoft.com/97121e6c-af5c-4da8-ad28-24b961c105d2">RpcAsyncInitializeHandle</a>



<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

