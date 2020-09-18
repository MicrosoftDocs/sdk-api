---
UID: NF:rpcdce.RpcServerRegisterIfEx
title: RpcServerRegisterIfEx function (rpcdce.h)
description: The RpcServerRegisterIfEx function registers an interface with the RPC run-time library.
helpviewer_keywords: ["RpcServerRegisterIfEx","RpcServerRegisterIfEx function [RPC]","_rpc_rpcserverregisterifex","rpc.rpcserverregisterifex","rpcdce/RpcServerRegisterIfEx"]
old-location: rpc\rpcserverregisterifex.htm
tech.root: Rpc
ms.assetid: 1666bc0a-72bf-40da-b054-c10b477c4367
ms.date: 12/05/2018
ms.keywords: RpcServerRegisterIfEx, RpcServerRegisterIfEx function [RPC], _rpc_rpcserverregisterifex, rpc.rpcserverregisterifex, rpcdce/RpcServerRegisterIfEx
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
 - RpcServerRegisterIfEx
 - rpcdce/RpcServerRegisterIfEx
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
 - RpcServerRegisterIfEx
---

# RpcServerRegisterIfEx function


## -description

The 
<b>RpcServerRegisterIfEx</b> function registers an interface with the RPC run-time library.

## -parameters

### -param IfSpec

MIDL-generated structure indicating the interface to register.

### -param MgrTypeUuid

Pointer to a type UUID to associate with the <i>MgrEpv</i> parameter. Specifying a <b>null</b> parameter value (or a nil UUID) registers <i>IfSpec</i> with a nil-type UUID.

### -param MgrEpv

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a <b>null</b> value. For more information, please see <a href="/windows/desktop/Rpc/rpc-mgr-epv">RPC_MGR_EPV</a>.

### -param Flags

Flags. For a list of flag values, see 
<a href="/windows/desktop/Rpc/interface-registration-flags">Interface Registration Flags</a>.

### -param MaxCalls

Maximum number of concurrent remote procedure call requests the server can accept on an auto-listen interface. The <i>MaxCalls</i> parameters is only applicable on an auto-listen interface, and is ignored on interfaces that are not auto-listen. The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. The actual number can be greater and can vary for each protocol sequence. 




Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> function call.

If the number of concurrent calls is not a concern, you can achieve slightly better server-side performance by specifying the default value using RPC_C_LISTEN_MAX_CALLS_DEFAULT. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.

### -param IfCallback

Security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function. See Remarks for more details.

## -returns

Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The parameters and effects of 
<b>RpcServerRegisterIfEx</b> subsume those of 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>. The difference is the ability to register an auto-listen interface and to specify a security-callback function.

The server application code calls 
<b>RpcServerRegisterIfEx</b> to register an interface. To register an interface, the server provides the following information:

<ul>
<li>Interface specification 


The interface specification is a data structure that the MIDL compiler generates.

</li>
<li>Manager type UUID and manager EPV 


The manager type UUID and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client. For each implementation of an interface offered by a server, it must register a separate manager EPV.

Note that when specifying a non-nil, manager type UUID, the server must also call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a> to register objects of this non-nil type.

</li>
</ul>
Specifying the RPC_IF_AUTOLISTEN flags marks the interface as an auto-listen interface. The run time begins listening for calls as soon as the interface is registered, and stops listening when the interface is unregistered. A call to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a> for this interface will wait for the completion of all pending calls on this interface. Calls to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a> will not affect the interface, nor will a call to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a> with <i>IfSpec</i> == <b>NULL</b>. This allows a DLL to register RPC interfaces or remove them from the registry without changing the main application's RPC state.

Specifying a security-callback function allows the server application to restrict access to its interfaces on a per-client basis. Remember that, by default, security is optional; the server run time will dispatch unsecured calls even if the server has called 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>. If the server wants to accept only authenticated clients, an interface callback function must call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient">RpcBindingInqAuthClient</a> or 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient">RpcGetAuthorizationContextForClient</a> function to retrieve the security level, or attempt to impersonate the client with 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>. It can also specify the RPC_IF_ALLOW_SECURE_ONLY flag in the interface flags.

When a server application specifies a security-callback function for its interface(s), the RPC run time automatically rejects unauthenticated calls to that interface. In addition, the run-time records the interfaces that each client has used. When a client makes an RPC to an interface that it has not used during the current communication session, the RPC run-time library will call the interface's security-callback function. Specifying RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH flag will prevent the automatic rejection of unauthenticated clients.

For the signature for the callback function, see 
<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_if_callback_fn">RPC_IF_CALLBACK_FN</a>.

The callback function should return RPC_S_OK if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception RPC_S_ACCESS_DENIED.

In some cases, the RPC run time may call the security-callback function more than once per client–per interface. Be sure your callback function can handle this possibility.

## -see-also

<a href="/windows/desktop/Rpc/registering-interfaces">Registering Interfaces</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient">RpcGetAuthorizationContextForClient</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif2">RpcServerRegisterIf2</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif3">RpcServerRegisterIf3</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterifex">RpcServerUnregisterIfEx</a>