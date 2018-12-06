---
UID: NF:rpcdce.RpcBindingFree
title: RpcBindingFree function
author: windows-sdk-content
description: The RpcBindingFree function releases binding-handle resources.
old-location: rpc\rpcbindingfree.htm
tech.root: rpc
ms.assetid: 0f85e64f-b4a6-4982-8df5-88caa0a312f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcBindingFree, RpcBindingFree function [RPC], _rpc_rpcbindingfree, rpc.rpcbindingfree, rpcdce/RpcBindingFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
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
 - RpcBindingFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingFree function


## -description


The 
<b>RpcBindingFree</b> function releases binding-handle resources.


## -parameters




### -param Binding

Pointer to the server binding to be freed.


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
<b>RpcBindingFree</b> function releases memory used by a server binding handle. Referenced binding information that was dynamically created during program execution is released as well. An application calls the 
<b>RpcBindingFree</b> function when it is finished using the binding handle. RPC binding handles must not be freed until all calls using the handle have completed; failure to do so will cause unpredictable results.

Binding handles are dynamically created by calling the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/835cac4b-9cf8-463a-8eff-d08bbee5f98e">RpcBindingCopy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9fdcdb99-be6c-4a3b-97dd-8d0eadd2754d">RpcBindingServerFromClient</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1acdd266-9ca2-43d4-b677-7c30b4dca4ee">RpcNsBindingSelect</a>
</li>
</ul>
If the operation successfully frees the binding, the <i>Binding</i> parameter returns a value of <b>NULL</b>.

<div class="alert"><b>Note</b>  Microsoft RPC supports 
<b>RpcBindingFree</b> only in client applications, or in server applications for binding handles generated with RpcBindingServerFromClient.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/835cac4b-9cf8-463a-8eff-d08bbee5f98e">RpcBindingCopy</a>



<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a>



<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>



<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>



<a href="https://msdn.microsoft.com/1acdd266-9ca2-43d4-b677-7c30b4dca4ee">RpcNsBindingSelect</a>



<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a>
 

 

