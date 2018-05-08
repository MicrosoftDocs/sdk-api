---
UID: NF:rpcdce.RpcServerRegisterIf2
title: RpcServerRegisterIf2 function
author: windows-driver-content
description: The RpcServerRegisterIf2 function registers an interface with the RPC run-time library.
old-location: rpc\rpcserverregisterif2.htm
old-project: Rpc
ms.assetid: 0c05ec68-4f1f-4a54-b6cd-776e9993b7da
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcServerRegisterIf2, RpcServerRegisterIf2 function [RPC], _rpc_rpcserverregisterif2, rpc.rpcserverregisterif2, rpcdce/RpcServerRegisterIf2
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
-	RpcServerRegisterIf2
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcServerRegisterIf2 function


## -description



			The 
<b>RpcServerRegisterIf2</b> function registers an interface with the RPC run-time library.


## -parameters




### -param IfSpec

MIDL-generated structure indicating the interface to register.


### -param MgrTypeUuid

Pointer to a type <b>UUID</b> to associate with the <i>MgrEpv</i> parameter. Specifying a <b>null</b> parameter value (or a nil <b>UUID</b>) registers <i>IfSpec</i> with a nil-type <b>UUID</b>.


### -param MgrEpv

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a <b>null</b> value. For more information, please see <a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a>.


### -param Flags

Flags. For a list of flag values, see 
<a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">Interface Registration Flags</a>.


### -param MaxCalls

Maximum number of concurrent remote procedure call requests the server can accept on an <b>auto-listen</b> interface. The <i>MaxCalls</i> parameter is only applicable on an <b>auto-listen</b> interface, and is ignored on interfaces that are not <b>auto-listen</b>. The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. The actual number can be greater and can vary for each protocol sequence. 




Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> function call.

If the number of concurrent calls is not a concern, you can achieve slightly better server-side performance by specifying the default value using RPC_C_LISTEN_MAX_CALLS_DEFAULT. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.


### -param MaxRpcSize

Maximum size of incoming data blocks, in bytes. This parameter may be used to help prevent malicious denial-of-service attacks. If the data block of a remote procedure call is larger than <i>MaxRpcSize</i>, the RPC run-time library rejects the call and sends an RPC_S_ACCESS_DENIED error to the client. Specifying a value of (unsigned int) –1 for this parameter removes the limit on the size of incoming data blocks. This parameter has no effect on calls made over the <a href="https://msdn.microsoft.com/0009f794-5c14-4484-9023-cb20c7030dc5">ncalrpc</a> protocol.


### -param IfCallbackFn

Security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function. See Remarks.


## -returns




						Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The parameters and effects of the 
<b>RpcServerRegisterIf2</b> function extend those of the 
<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a> function. The difference is the ability to register an <b>auto-listen</b> interface and to specify a security-callback function.

The server application code calls 
<b>RpcServerRegisterIf2</b> to register an interface. To register an interface, the server provides the following information:

<ul>
<li>Interface specification 


The interface specification is a data structure that the MIDL compiler generates.

</li>
<li>Manager type <b>UUID</b> and manager EPV 


The manager type <b>UUID</b> and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client. For each implementation of an interface offered by a server, it must register a separate manager EPV.

Note that when specifying a non-nil, manager type <b>UUID</b>, the server must also call 
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a> to register objects of this non-nil type.

</li>
</ul>
Specifying the RPC_IF_AUTOLISTEN flags marks the interface as an <b>auto-listen</b> interface. The run time begins listening for calls as soon as the interface is registered, and stops listening when the interface is unregistered. A call to 
<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> for this interface waits for the completion of all pending calls on this interface. Calls to the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> and the 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> functions do not affect the interface, nor does a call to the 
<b>RpcServerUnregisterIf</b> function with <i>IfSpec</i> set to the value <b>NULL</b>. This allows a DLL to register RPC interfaces or remove them from the registry without changing the main application's RPC state.

Specifying a security-callback function allows the server application to restrict access to its interfaces on an individual client basis. That is, by default, security is optional; the server run-time will dispatch unsecured calls even if the server has called the 
<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a> function. If the server wants to accept only authenticated clients, an interface callback function must call the 
<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a>, <a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>, or <a href="https://msdn.microsoft.com/563b70ed-bc9a-40be-a77b-17b993cc64f3">RpcServerInqCallAttributes</a> function to retrieve the security level, or attempt to impersonate the client with the 
<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a> function. It can also specify the RPC_IF_ALLOW_SECURE_ONLY flag in the interface flags to reject unauthenticated calls.

When a server application specifies a security-callback function for its interface(s), the RPC run time automatically rejects calls without authentication information to that interface. In addition, the run-time records the interfaces  each client has used. When a client makes an RPC to an interface that it has not used during the current communication session, the RPC run-time library  calls the interface's security-callback function. Specifying RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH flag will prevent the automatic rejection of unauthenticated clients. Note that calls on the so-called <b>NULL</b> security session can have authentication information, even though they come from anonymous clients. Thus the existence of a callback alone is not sufficient to prevent anonymous clients from connecting. Either the security callback function must check for that, or the RPC_IF_ALLOW_SECURE_ONLY flag must be used. RPC_IF_ALLOW_SECURE_ONLY rejects <b>null</b> session calls only on Windows XP and later versions of Windows.

For the signature for the callback function, see 
<a href="https://msdn.microsoft.com/6c2239db-4a01-4ba1-b8ea-1c4b3467e326">RPC_IF_CALLBACK_FN</a>.

The callback function should return RPC_S_OK, if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception RPC_S_ACCESS_DENIED.

In some cases, the RPC run time may call the security-callback function more than once per client, per interface. Be sure your callback function can handle this possibility.




## -see-also




<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>



<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>



<a href="https://msdn.microsoft.com/D685B7A6-7E22-419F-B476-F0372836D16A">RpcServerRegisterIf3</a>



<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>



<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>



<a href="https://msdn.microsoft.com/f01eab2c-cd33-4427-9f0c-903e4d3474e9">RpcServerUnregisterIfEx</a>
 

 

