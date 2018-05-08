---
UID: NF:rpcdce.RpcBindingServerFromClient
title: RpcBindingServerFromClient function
author: windows-driver-content
description: An application calls RpcBindingServerFromClient to convert a client binding handle into a partially-bound server binding handle.
old-location: rpc\rpcbindingserverfromclient.htm
old-project: Rpc
ms.assetid: 9fdcdb99-be6c-4a3b-97dd-8d0eadd2754d
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcBindingServerFromClient, RpcBindingServerFromClient function [RPC], _rpc_rpcbindingserverfromclient, rpc.rpcbindingserverfromclient, rpcdce/RpcBindingServerFromClient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcBindingServerFromClient
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcBindingServerFromClient function


## -description


An application calls 
<b>RpcBindingServerFromClient</b> to convert a client binding handle into a partially-bound server binding handle.


## -parameters




### -param ClientBinding

Client binding handle to convert to a server binding handle. If a value of zero is specified, the server impersonates the client that is being served by this server thread.

<div class="alert"><b>Note</b>  This parameter cannot be <b>NULL</b> in Windows NT 4.0.</div>
<div> </div>

### -param ServerBinding

Returns a server binding handle.


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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Cannot determine the client's host. See Remarks for a list of supported protocol sequences.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The following protocol sequences support 
<b>RpcBindingServerFromClient</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a>
</li>
<li>
<a href="midl.ncadg_ipx">ncadg_ipx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/45e93e25-e84d-4242-80b0-c4b61e80f716">ncacn_spx</a>.</li>
<li>
<a href="https://msdn.microsoft.com/02961bb8-faf0-42e5-b134-dd2983e6d146">ncacn_np</a> (effective with Windows 2000)</li>
<li>
<a href="midl.ncacn_http">ncacn_http</a>
</li>
<li>ncalrpc</li>
</ul>
An application gets a client binding handle from the RPC run-time. When the remote procedure call arrives at a server, the run-time creates a client binding handle that contains information about the calling client. The run-time passes this handle to the server manager function as the first argument.

Calling 
<b>RpcBindingServerFromClient</b> converts this client handle to a server handle that has these properties:

<ul>
<li>The server handle is a partially-bound handle. It contains a network address for the calling client, but lacks an endpoint.</li>
<li>The server handle contains the same object 
<a href="midl.uuid">UUID</a> used by the calling client. This can be the nil UUID. For more information on how a client specifies an object UUID for a call, see 
<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingsetObject</a>, 
<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>, 
<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a>, and 
<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>.</li>
<li>The server handle contains no authentication information.</li>
</ul>
The server application must call 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> to free the resources used by the server binding handle once it is no longer needed.

<div class="alert"><b>Note</b>  To query a client's address, an application starts by calling the RpcBindingServerFromClient function to obtain a partially bound server binding handle.  The server binding handle can be used to obtain a string binding by invoking RpcBindingToStringBinding.  The server can then call RpcStringBindingParse to extract the client's network address from the string binding.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>



<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a>



<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>



<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>



<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a>
 

 

