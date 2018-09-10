---
UID: NS:rpcdce.RPC_INTERFACE_TEMPLATE
title: RPC_INTERFACE_TEMPLATE
author: windows-sdk-content
description: Defines an RPC interface group server interface.
old-location: rpc\rpc_interface_template.htm
tech.root: Rpc
ms.assetid: 4DBD0B43-659B-4074-954B-FE9ABB0DCE63
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PRPC_INTERFACE_TEMPLATE, PRPC_INTERFACE_TEMPLATE, PRPC_INTERFACE_TEMPLATE structure pointer [RPC], RPC_INTERFACE_TEMPLATE, RPC_INTERFACE_TEMPLATE structure [RPC], RPC_INTERFACE_TEMPLATEA, RPC_INTERFACE_TEMPLATEW, rpc.rpc_interface_template, rpcdce/PRPC_INTERFACE_TEMPLATE, rpcdce/RPC_INTERFACE_TEMPLATE, rpcdce/RPC_INTERFACE_TEMPLATEA, rpcdce/RPC_INTERFACE_TEMPLATEW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_INTERFACE_TEMPLATEW (Unicode) and RPC_INTERFACE_TEMPLATEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_INTERFACE_TEMPLATE
 - RPC_INTERFACE_TEMPLATEA
 - RPC_INTERFACE_TEMPLATEW
product: Windows
targetos: Windows
req.typenames: RPC_INTERFACE_TEMPLATE, *PRPC_INTERFACE_TEMPLATE
req.redist: 
---

# RPC_INTERFACE_TEMPLATE structure


## -description


The <b>RPC_INTERFACE_TEMPLATE</b> structure defines an RPC interface group server interface.


## -struct-fields




### -field Version

This field is reserved and must be set to 0.


### -field IfSpec

MIDL-generated structure that defines the interface to register.


### -field MgrTypeUuid

Pointer to a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to associate with <i>MgrEpv</i>. <b>NULL</b> or a nil <b>UUID</b> registers <i>IfSpec</i> with a nil <b>UUID</b>.


### -field MgrEpv

Pointer to a <a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a> structure that contains the manager routines' entry-point vector (EPV). If <b>NULL</b>,the MIDL-generated default EPV is used.


### -field Flags

Flags. For a list of flag values, see <a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">Interface Registration Flags</a>. Interface group interfaces are always treated as <b>auto-listen</b>.


### -field MaxCalls

Maximum number of concurrent remote procedure call requests the server can accept on this interface.  The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. However, the actual number can be greater than <i>MaxCalls</i> and can vary for each protocol sequence.

Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in <a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>.

If the number of concurrent calls is not a concern, slightly better server-side performance can be achieved by specifying the default value using <b>RPC_C_LISTEN_MAX_CALLS_DEFAULT</b>. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.


### -field MaxRpcSize

Maximum size, in bytes, of incoming data blocks. <i>MaxRpcSize</i> may be used to help prevent malicious denial-of-service attacks. If the data block of a remote procedure call is larger than <i>MaxRpcSize</i>, the RPC run-time library rejects the call and sends an <b>RPC_S_ACCESS_DENIED</b> error to the client. Specifying a value of (unsigned int) –1 in <i>MaxRpcSize</i> removes the limit on the size of incoming data blocks. This parameter has no effect on calls made over the <a href="https://msdn.microsoft.com/51284532-b0ac-4bf2-b322-91393b2b9dc6">ncalrpc</a> protocol.


### -field IfCallback

A pointer to a <a href="https://msdn.microsoft.com/D34F2902-80EE-4011-A837-2A8C21E5A136">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a> security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function.


### -field UuidVector

Pointer to a vector of object <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUIDs</a> offered by the server to be registered with the RPC endpoint mapper. The server application constructs this vector.  <b>NULL</b> indicates there are no object <b>UUIDs</b> to register.


### -field Annotation

Pointer to the character-string comment applied to each cross-product element added to the local endpoint-map database. The string can be up to 64 characters long, including the null terminating character. Specify a null value or a null-terminated string ("\0") if there is no annotation string.

The annotation string is used by applications for information only. RPC does not use this string to determine which server instance a client communicates with or for enumerating elements in the endpoint-map database.


### -field SecurityDescriptor

Optional security descriptor describing which clients have the right to access the interface.


## -remarks



To register an interface, the server provides the following information:<ul>
<li>Interface specificationThe interface specification is a data structure that the MIDL compiler generates.

</li>
<li>Manager type <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> and manager EPVThe manager type <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client. For each implementation of an interface offered by a server, it must register a separate manager EPV.
Note that when specifying a non-nil, manager type <b>UUID</b>, the server must also call <a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a> to register objects of this non-nil type.

</li>
</ul>


All interface group interfaces are treated as <b>auto-listen</b>.  The runtime begins listening for calls as soon as the interface group is activated.  Calls to <a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> and <a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> do not affect the interface, nor does a call to <a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> with <i>IfSpec</i> set to <b>NULL</b>.

Specifying a security-callback function in <i>IfCallback</i> allows the server application to restrict access to its interfaces on an individual client basis. That is, by default, security is optional; the server run-time will dispatch unsecured calls even if the server has called <a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>. If the server wants to accept only authenticated clients, an interface callback function must call <a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a>, <a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>, or <a href="https://msdn.microsoft.com/563b70ed-bc9a-40be-a77b-17b993cc64f3">RpcServerInqCallAttributes</a> to retrieve the security level, or attempt to impersonate the client with <a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>. It can also specify the <a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">RPC_IF_ALLOW_SECURE_ONLY</a> flag in <i>Flags</i> to reject unauthenticated calls.

When a server application specifies a security-callback function for its interface(s) in <i>IfCallback</i>, the RPC run time automatically rejects calls without authentication information to that interface. In addition, the run-time records the interfaces each client has used. When a client makes an RPC to an interface that it has not used during the current communication session, the RPC run-time library calls the interface's security-callback function. Specifying <a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</a> in <i>Flags</i> will prevent the automatic rejection of unauthenticated clients. Note that calls on the <b>NULL</b> security session can have authentication information, even though they come from anonymous clients. Thus, the existence of a callback alone is not sufficient to prevent anonymous clients from connecting; either the security callback function must check for that, or the RPC_IF_ALLOW_SECURE_ONLY flag must be used. RPC_IF_ALLOW_SECURE_ONLY rejects null session calls only on Windows XP and later versions of Windows.

For the signature for the callback function, see <a href="https://msdn.microsoft.com/6c2239db-4a01-4ba1-b8ea-1c4b3467e326">RPC_IF_CALLBACK_FN</a>.

The callback function in <i>IfCallback</i> should return <b>RPC_S_OK</b> if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception <b>RPC_S_ACCESS_DENIED</b>.

In some cases, the RPC run time may call the security-callback function more than once per client, per interface. The callback function must be able to handle this possibility.




## -see-also




<a href="https://msdn.microsoft.com/D34F2902-80EE-4011-A837-2A8C21E5A136">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInqBindings</a>



<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>
 

 

