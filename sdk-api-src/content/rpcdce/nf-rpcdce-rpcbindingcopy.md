---
UID: NF:rpcdce.RpcBindingCopy
title: RpcBindingCopy function
author: windows-sdk-content
description: The RpcBindingCopy function copies binding information and creates a new binding handle.
old-location: rpc\rpcbindingcopy.htm
old-project: Rpc
ms.assetid: 835cac4b-9cf8-463a-8eff-d08bbee5f98e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcBindingCopy, RpcBindingCopy function [RPC], _rpc_rpcbindingcopy, rpc.rpcbindingcopy, rpcdce/RpcBindingCopy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcBindingCopy
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcBindingCopy function


## -description


The 
<b>RpcBindingCopy</b> function copies binding information and creates a new binding handle.


## -parameters




### -param SourceBinding

Server binding handle whose referenced binding information is copied.


### -param DestinationBinding

Returns a pointer to the server binding handle that refers to the copied binding information.


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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcBindingCopy</b> function copies the server-binding information referenced by the <i>SourceBinding</i> parameter. 
<b>RpcBindingCopy</b> uses the <i>DestinationBinding</i> parameter to return a new server binding handle for the copied binding information. 
<b>RpcBindingCopy</b> also copies the authentication information from the <i>SourceBinding</i> parameter to the <i>DestinationBinding</i> parameter.

An application uses 
<b>RpcBindingCopy</b> when it wants to prevent a change being made to binding information by one thread from affecting the binding information used by other threads.

Once an application calls 
<b>RpcBindingCopy</b>, operations performed on the <i>SourceBinding</i> binding handle do not affect the binding information referenced by the <i>DestinationBinding</i> binding handle. Similarly, operations performed on the <i>DestinationBinding</i> binding handle do not affect the binding information referenced by the <i>SourceBinding</i> binding handle.

If an application wants one thread's changes to binding information to affect the binding information used by other threads, the application should share a single binding handle across the threads. In this case, the application is responsible for binding-handle concurrency control.

When an application is finished using the binding handle specified by the <i>DestinationBinding</i> parameter, the application should call the 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> function to release the memory used by the <i>DestinationBinding</i> binding handle and its referenced binding information.

<div class="alert"><b>Note</b>  Microsoft RPC supports 
<b>RpcBindingCopy</b> only in client applications, not in server applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>
 

 

