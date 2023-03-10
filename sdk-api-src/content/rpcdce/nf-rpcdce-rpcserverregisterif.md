---
UID: NF:rpcdce.RpcServerRegisterIf
title: RpcServerRegisterIf function (rpcdce.h)
description: The RpcServerRegisterIf function registers an interface with the RPC run-time library.
helpviewer_keywords: ["RpcServerRegisterIf","RpcServerRegisterIf function [RPC]","_rpc_rpcserverregisterif","rpc.rpcserverregisterif","rpcdce/RpcServerRegisterIf"]
old-location: rpc\rpcserverregisterif.htm
tech.root: Rpc
ms.assetid: f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d
ms.date: 12/05/2018
ms.keywords: RpcServerRegisterIf, RpcServerRegisterIf function [RPC], _rpc_rpcserverregisterif, rpc.rpcserverregisterif, rpcdce/RpcServerRegisterIf
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
 - RpcServerRegisterIf
 - rpcdce/RpcServerRegisterIf
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
 - RpcServerRegisterIf
---

# RpcServerRegisterIf function


## -description

The 
<b>RpcServerRegisterIf</b> function registers an interface with the RPC run-time library.

## -parameters

### -param IfSpec

MIDL-generated structure indicating the interface to register.

### -param MgrTypeUuid

Pointer to a type UUID to associate with the <i>MgrEpv</i> parameter. Specifying a null parameter value (or a nil UUID) registers <i>IfSpec</i> with a nil-type UUID.

### -param MgrEpv

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a null value. For more information, please see <a href="/windows/desktop/Rpc/rpc-mgr-epv">RPC_MGR_EPV</a>.

## -returns

Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server can register an unlimited number of interfaces with the RPC run-time library. Registration makes an interface available to clients using a binding handle to the server. To register an interface, the server application code calls 
<b>RpcServerRegisterIf</b>. For each implementation of an interface that a server offers, it must register a separate manager EPV.

When calling 
<b>RpcServerRegisterIf</b>, the server provides the following information:

<ul>
<li>Interface specification 


The interface specification is a data structure that the MIDL compiler generates. The server specifies the interface using the <i>IfSpec</i> parameter.

</li>
<li>Manager type UUID and manager EPV 


The manager type UUID and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client.

The server specifies the manager type UUID and EPV using the <i>MgrTypeUuid</i> and <i>MgrEpv</i> parameters. Note that when specifying a non-nil manager-type UUID, the server must also call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a> function to register objects of this non-nil type.

</li>
</ul>
If your server application needs to register an auto-listen interface or use a callback function for authentication purposes, use 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a>.

## -see-also

<a href="/windows/desktop/Rpc/registering-interfaces">Registering Interfaces</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif3">RpcServerRegisterIf3</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterifex">RpcServerUnregisterIfEx</a>