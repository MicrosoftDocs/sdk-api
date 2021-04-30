---
UID: NF:rpcdce.RpcServerUnregisterIfEx
title: RpcServerUnregisterIfEx function (rpcdce.h)
description: The RpcServerUnregisterIfEx function removes an interface from the RPC run-time library registry. This function extends the functionality of the RpcServerUnregisterIf function.
helpviewer_keywords: ["RpcServerUnregisterIfEx","RpcServerUnregisterIfEx function [RPC]","_rpc_rpcserverunregisterifex","rpc.rpcserverunregisterifex","rpcdce/RpcServerUnregisterIfEx"]
old-location: rpc\rpcserverunregisterifex.htm
tech.root: Rpc
ms.assetid: f01eab2c-cd33-4427-9f0c-903e4d3474e9
ms.date: 12/05/2018
ms.keywords: RpcServerUnregisterIfEx, RpcServerUnregisterIfEx function [RPC], _rpc_rpcserverunregisterifex, rpc.rpcserverunregisterifex, rpcdce/RpcServerUnregisterIfEx
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - RpcServerUnregisterIfEx
 - rpcdce/RpcServerUnregisterIfEx
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
 - RpcServerUnregisterIfEx
---

# RpcServerUnregisterIfEx function


## -description

The 
<b>RpcServerUnregisterIfEx</b> function removes an interface from the RPC run-time library registry. This function extends the functionality of the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a> function.

## -parameters

### -param IfSpec [in]

Interface to remove from the registry. 




Specify a null value to remove all interfaces previously registered with the type UUID value specified in the <i>MgrTypeUuid</i> parameter.

### -param MgrTypeUuid [in]

Pointer to the type UUID of the manager entry-point vector (EPV) to remove from the registry. The value of <i>MgrTypeUuid</i> should be the same value as was provided in a call to the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a> function, <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a> function, or the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a> function. 




Specify a null value to remove the interface specified in the <i>IfSpec</i> parameter for all previously registered type UUIDs from the registry.

Specify a nil UUID to remove the MIDL-generated default manager EPV from the registry. In this case, all manager EPVs registered with a non-nil type UUID remain registered.

### -param RundownContextHandles [in]

Specifies whether rundown is called for active context handles. If non-zero, the rundown is called once all calls on the interface have completed. If set to zero, the RPC run time assumes the server has already destroyed its portion of the context handle and it will not call the rundown routines.

## -returns

Returns RPC status. 
<b>RpcServerUnregisterIfEx</b> does not fail unless supplied with invalid values.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcServerUnregisterIfEx</b> function waits for all calls on a given interface to complete before unregistering the context handles.

The 
<b>RpcServerUnregisterIfEx</b> function supplies all the functionality provided in the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a> function. In addition, the 
<b>RpcServerUnregisterIfEx</b> function unregisters all context handles registered by the given interface. The interface must use the <b>strict_context_handle</b> attribute, otherwise the results are undefined.

<b>RpcServerUnregisterIfEx</b> is the only function that provides safe unloading of a DLL with active context handles outside of process shutdown. It is available on Windows XP and later versions of Windows only.

## -see-also

<a href="/windows/desktop/Rpc/rpc-mgr-epv">RPC_MGR_EPV</a>



<a href="/windows/desktop/Rpc/registering-interfaces">Registering Interfaces</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a>



<a href="/windows/desktop/Rpc/using-context-handles">Using Context
		  Handles</a>