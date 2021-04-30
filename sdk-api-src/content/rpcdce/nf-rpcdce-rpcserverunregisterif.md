---
UID: NF:rpcdce.RpcServerUnregisterIf
title: RpcServerUnregisterIf function (rpcdce.h)
description: The RpcServerUnregisterIf function removes an interface from the RPC run-time library registry.
helpviewer_keywords: ["RpcServerUnregisterIf","RpcServerUnregisterIf function [RPC]","_rpc_rpcserverunregisterif","rpc.rpcserverunregisterif","rpcdce/RpcServerUnregisterIf"]
old-location: rpc\rpcserverunregisterif.htm
tech.root: Rpc
ms.assetid: bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b
ms.date: 12/05/2018
ms.keywords: RpcServerUnregisterIf, RpcServerUnregisterIf function [RPC], _rpc_rpcserverunregisterif, rpc.rpcserverunregisterif, rpcdce/RpcServerUnregisterIf
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcServerUnregisterIf
 - rpcdce/RpcServerUnregisterIf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerUnregisterIf
---

# RpcServerUnregisterIf function


## -description

The 
<b>RpcServerUnregisterIf</b> function removes an interface from the RPC run-time library registry.

## -parameters

### -param IfSpec

Interface to remove from the registry. 




Specify a <b>null</b> value to remove all interfaces previously registered with the type UUID value specified in the <i>MgrTypeUuid</i> parameter.

### -param MgrTypeUuid

Pointer to the type UUID of the manager entry-point vector (EPV) to remove from the registry. The value of <i>MgrTypeUuid</i> should be the same value as was provided in a call to the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a> function, <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a> function, or the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a> function. 




Specify a <b>null</b> value to remove the interface specified in the <i>IfSpec</i> parameter for all previously registered type UUIDs from the registry.

Specify a nil UUID to remove the MIDL-generated default manager EPV from the registry. In this case, all manager EPVs registered with a non-nil type UUID remain registered.

### -param WaitForCallsToComplete

Flag that indicates whether to remove the interface from the registry immediately or to wait until all current calls are complete. 




Specify a value of zero to disregard calls in progress and remove the interface from the registry immediately. Specify any nonzero value to wait until all active calls complete.

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
<dt><b>RPC_S_UNKNOWN_MGR_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The manager type is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_IF</b></dt>
</dl>
</td>
<td width="60%">
The interface is unknown.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server calls 
<b>RpcServerUnregisterIf</b> to remove the association between an interface and a manager EPV. To specify the manager EPV to remove in the <i>MgrTypeUuid</i> parameter, provide the type UUID value that was specified in a call to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>. After it is removed from the registry, an interface is no longer available to client applications.

When an interface is removed from the registry, the RPC run-time library stops accepting new calls for that interface. Calls that are currently executing on the interface are allowed to complete, including callbacks.

The following table summarizes the behavior of 
<b>RpcServerUnregisterIf</b>.

<table>
<tr>
<th>IfSpec</th>
<th>MgrTypeUuid</th>
<th>Behavior</th>
</tr>
<tr>
<td>Non-<b>null</b></td>
<td>Non-<b>null</b></td>
<td>Removes from the registry the manager EPV associated with the specified parameters.</td>
</tr>
<tr>
<td>Non-<b>null</b></td>
<td><b>NULL</b></td>
<td>Removes all manager EPVs associated with the <i>IfSpec</i> parameter.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>Non-<b>null</b></td>
<td>Removes all manager EPVs associated with the <i>MgrTypeUuid</i> parameter.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
<td>Removes all manager EPVs. This call has the effect of preventing the server from receiving any new remote procedure calls because all the manager EPVs for all interfaces have been unregistered.</td>
</tr>
</table>
 


<div> </div>


<div class="alert"><b>Note</b>  If the value of <i>IfSpec</i> is <b>NULL</b>, this function will leave <i>auto-listen</i> interfaces registered. <i>Auto-listen</i> interfaces must be removed from the registry individually. See 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a> for more details.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Rpc/rpc-mgr-epv">RPC_MGR_EPV</a>



<a href="/windows/desktop/Rpc/registering-interfaces">Registering Interfaces</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterifex">RpcServerUnregisterIfEx</a>