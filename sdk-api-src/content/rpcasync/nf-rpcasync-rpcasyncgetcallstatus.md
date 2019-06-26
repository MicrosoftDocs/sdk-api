---
UID: NF:rpcasync.RpcAsyncGetCallStatus
title: RpcAsyncGetCallStatus function (rpcasync.h)
author: windows-sdk-content
description: The client calls the RpcAsyncGetCallStatus function to determine the current status of an asynchronous remote call.
old-location: rpc\rpcasyncgetcallstatus.htm
tech.root: Rpc
ms.assetid: caa3add7-d07f-4d56-ad96-51dc67f66117
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RpcAsyncGetCallStatus, RpcAsyncGetCallStatus function [RPC], _rpc_rpcasyncgetcallstatus, rpc.rpcasyncgetcallstatus, rpcasync/RpcAsyncGetCallStatus
ms.topic: function
f1_keywords: 
 - "rpcasync/RpcAsyncGetCallStatus"
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
 - RpcAsyncGetCallStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcAsyncGetCallStatus function


## -description


The client calls the 
<b>RpcAsyncGetCallStatus</b> function to determine the current status of an asynchronous remote call.


## -parameters




### -param pAsync

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/ns-rpcasync-_rpc_async_state">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.


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
<dt><b>Other error codes</b></dt>
</dl>
</td>
<td width="60%">
The call failed. The client application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a> to receive the application-specific error code.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



This client-side function returns the current status of the asynchronous call. Note that if the return value is anything other than RPC_S_ASYNC_CALL_PENDING the call is complete.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/ns-rpcasync-_rpc_async_state">RPC_ASYNC_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>
 

 

