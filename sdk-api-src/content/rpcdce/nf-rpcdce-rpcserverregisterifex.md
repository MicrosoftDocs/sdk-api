---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a <b>null</b> value. For more information, please see <a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a>.


### -param Flags

Flags. For a list of flag values, see 
<a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">Interface Registration Flags</a>.


### -param MaxCalls

Maximum number of concurrent remote procedure call requests the server can accept on an auto-listen interface. The <i>MaxCalls</i> parameters is only applicable on an auto-listen interface, and is ignored on interfaces that are not auto-listen. The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. The actual number can be greater and can vary for each protocol sequence. 




Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> function call.

If the number of concurrent calls is not a concern, you can achieve slightly better server-side performance by specifying the default value using RPC_C_LISTEN_MAX_CALLS_DEFAULT. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.


### -param IfCallback

Security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function. See Remarks for more details.


## -returns



Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The parameters and effects of 
<b>RpcServerRegisterIfEx</b> subsume those of 
<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>. The difference is the ability to register an auto-listen interface and to specify a security-callback function.

The server application code calls 
<b>RpcServerRegisterIfEx</b> to register an interface. To register an interface, the server provides the following information:

<ul>
<li>Interface specification 


The interface specification is a data structure that the MIDL compiler generates.

</li>
<li>Manager type UUID and manager EPV 


The manager type UUID and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client. For each implementation of an interface offered by a server, it must register a separate manager EPV.

Note that when specifying a non-nil, manager type UUID, the server must also call 
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a> to register objects of this non-nil type.

</li>
</ul>
Specifying the RPC_IF_AUTOLISTEN flags marks the interface as an auto-listen interface. The run time begins listening for calls as soon as the interface is registered, and stops listening when the interface is unregistered. A call to 
<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> for this interface will wait for the completion of all pending calls on this interface. Calls to 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> and 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> will not affect the interface, nor will a call to 
<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> with <i>IfSpec</i> == <b>NULL</b>. This allows a DLL to register RPC interfaces or remove them from the registry without changing the main application's RPC state.

Specifying a security-callback function allows the server application to restrict access to its interfaces on a per-client basis. Remember that, by default, security is optional; the server run time will dispatch unsecured calls even if the server has called 
<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>. If the server wants to accept only authenticated clients, an interface callback function must call the 
<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a> or 
<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a> function to retrieve the security level, or attempt to impersonate the client with 
<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>. It can also specify the RPC_IF_ALLOW_SECURE_ONLY flag in the interface flags.

When a server application specifies a security-callback function for its interface(s), the RPC run time automatically rejects unauthenticated calls to that interface. In addition, the run-time records the interfaces that each client has used. When a client makes an RPC to an interface that it has not used during the current communication session, the RPC run-time library will call the interface's security-callback function. Specifying RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH flag will prevent the automatic rejection of unauthenticated clients.

For the signature for the callback function, see 
<a href="https://msdn.microsoft.com/6c2239db-4a01-4ba1-b8ea-1c4b3467e326">RPC_IF_CALLBACK_FN</a>.

The callback function should return RPC_S_OK if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception RPC_S_ACCESS_DENIED.

In some cases, the RPC run time may call the security-callback function more than once per client–per interface. Be sure your callback function can handle this possibility.




## -see-also




<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>



<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a>



<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>



<a href="https://msdn.microsoft.com/c89d04d7-f607-48cc-8cb6-b6aebab41671">RpcNsBindingExport</a>



<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>



<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a>



<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>



<a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>



<a href="https://msdn.microsoft.com/D685B7A6-7E22-419F-B476-F0372836D16A">RpcServerRegisterIf3</a>



<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>



<a href="https://msdn.microsoft.com/f01eab2c-cd33-4427-9f0c-903e4d3474e9">RpcServerUnregisterIfEx</a>
 

 

