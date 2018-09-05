---
UID: NF:rpcdce.RpcServerInqBindings
title: RpcServerInqBindings function
author: windows-sdk-content
description: The RpcServerInqBindings function returns the binding handles over which remote procedure calls can be received.
old-location: rpc\rpcserverinqbindings.htm
old-project: Rpc
ms.assetid: 96f081ab-6210-4ca0-a913-182477463981
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcServerInqBindings, RpcServerInqBindings function [RPC], _rpc_rpcserverinqbindings, rpc.rpcserverinqbindings, rpcdce/RpcServerInqBindings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerInqBindings
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcServerInqBindings function


## -description


The 
<b>RpcServerInqBindings</b> function returns the binding handles over which remote procedure calls can be received.


## -parameters




### -param BindingVector

Returns a pointer to a pointer to a vector of server binding handles.


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
<dt><b>RPC_S_NO_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
There are no bindings.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls 
<b>RpcServerInqBindings</b> to obtain a vector of server binding handles. The RPC run-time library creates binding handles when a server application calls the following functions to register protocol sequences:

<ul>
<li>
<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4fc2ccbe-1b01-4157-b3e7-2c61397d78f7">RpcServerUseAllProtseqsEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6f3f7726-3e12-4b0b-8454-25f06a29b245">RpcServerUseAllProtseqsIf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/118c931e-29ca-4ffb-aa32-24c6f4289cc8">RpcServerUseAllProtseqsIfEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a8cedfe9-9c16-4c35-9cc4-5ccaa9e130a8">RpcServerUseProtseqEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c5bc52c5-9799-4fab-89fa-a680639a229f">RpcServerUseProtseqEpEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28238ff2-0ed0-4cb5-8117-b6c544d8c098">RpcServerUseProtseqIfEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>
</li>
</ul>
The returned binding vector can contain binding handles with dynamic endpoints or binding handles with well-known endpoints, depending on which of the above functions the server application called.

A server uses the vector of binding handles for exporting to the name service, for registering with the local endpoint-map database, or for conversion to string bindings. If there are no binding handles (no registered protocol sequences), this routine returns the RPC_S_NO_BINDINGS status code and a <i>BindingVector</i> parameter value of NULL. The server is responsible for calling the 
<a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a> function to release the memory used by the vector.




## -see-also




<a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a>



<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>



<a href="https://msdn.microsoft.com/c89d04d7-f607-48cc-8cb6-b6aebab41671">RpcNsBindingExport</a>



<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>



<a href="https://msdn.microsoft.com/6f3f7726-3e12-4b0b-8454-25f06a29b245">RpcServerUseAllProtseqsIf</a>



<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>



<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>



<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>
 

 

