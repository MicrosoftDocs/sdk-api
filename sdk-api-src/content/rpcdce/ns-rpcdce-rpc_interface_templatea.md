---
UID: NS:rpcdce.RPC_INTERFACE_TEMPLATEA
title: RPC_INTERFACE_TEMPLATEA (rpcdce.h)
description: Defines an RPC interface group server interface. (RPC_INTERFACE_TEMPLATEA)
helpviewer_keywords: ["*PRPC_INTERFACE_TEMPLATEA","PRPC_INTERFACE_TEMPLATE","PRPC_INTERFACE_TEMPLATE structure pointer [RPC]","RPC_INTERFACE_TEMPLATE","RPC_INTERFACE_TEMPLATE structure [RPC]","RPC_INTERFACE_TEMPLATEA","RPC_INTERFACE_TEMPLATEW","rpc.rpc_interface_template","rpcdce/PRPC_INTERFACE_TEMPLATE","rpcdce/RPC_INTERFACE_TEMPLATE","rpcdce/RPC_INTERFACE_TEMPLATEA","rpcdce/RPC_INTERFACE_TEMPLATEW"]
old-location: rpc\rpc_interface_template.htm
tech.root: Rpc
ms.assetid: 4DBD0B43-659B-4074-954B-FE9ABB0DCE63
ms.date: 12/05/2018
ms.keywords: '*PRPC_INTERFACE_TEMPLATEA, PRPC_INTERFACE_TEMPLATE, PRPC_INTERFACE_TEMPLATE structure pointer [RPC], RPC_INTERFACE_TEMPLATE, RPC_INTERFACE_TEMPLATE structure [RPC], RPC_INTERFACE_TEMPLATEA, RPC_INTERFACE_TEMPLATEW, rpc.rpc_interface_template, rpcdce/PRPC_INTERFACE_TEMPLATE, rpcdce/RPC_INTERFACE_TEMPLATE, rpcdce/RPC_INTERFACE_TEMPLATEA, rpcdce/RPC_INTERFACE_TEMPLATEW'
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
targetos: Windows
req.typenames: RPC_INTERFACE_TEMPLATEA, *PRPC_INTERFACE_TEMPLATEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PRPC_INTERFACE_TEMPLATEA
 - rpcdce/PRPC_INTERFACE_TEMPLATEA
 - RPC_INTERFACE_TEMPLATEA
 - rpcdce/RPC_INTERFACE_TEMPLATEA
dev_langs:
 - c++
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
---

# RPC_INTERFACE_TEMPLATEA structure


## -description

The <b>RPC_INTERFACE_TEMPLATE</b> structure defines an RPC interface group server interface.

## -struct-fields

### -field Version

This field is reserved and must be set to 0.

### -field IfSpec

MIDL-generated structure that defines the interface to register.

### -field MgrTypeUuid

Pointer to a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to associate with <i>MgrEpv</i>. <b>NULL</b> or a nil <b>UUID</b> registers <i>IfSpec</i> with a nil <b>UUID</b>.

### -field MgrEpv

Pointer to a <a href="/windows/desktop/Rpc/rpc-mgr-epv">RPC_MGR_EPV</a> structure that contains the manager routines' entry-point vector (EPV). If <b>NULL</b>,the MIDL-generated default EPV is used.

### -field Flags

Flags. For a list of flag values, see <a href="/windows/desktop/Rpc/interface-registration-flags">Interface Registration Flags</a>. Interface group interfaces are always treated as <b>auto-listen</b>.

### -field MaxCalls

Maximum number of concurrent remote procedure call requests the server can accept on this interface.  The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. However, the actual number can be greater than <i>MaxCalls</i> and can vary for each protocol sequence.

Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>.

If the number of concurrent calls is not a concern, slightly better server-side performance can be achieved by specifying the default value using <b>RPC_C_LISTEN_MAX_CALLS_DEFAULT</b>. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.

### -field MaxRpcSize

Maximum size, in bytes, of incoming data blocks. <i>MaxRpcSize</i> may be used to help prevent malicious denial-of-service attacks. If the data block of a remote procedure call is larger than <i>MaxRpcSize</i>, the RPC run-time library rejects the call and sends an <b>RPC_S_ACCESS_DENIED</b> error to the client. Specifying a value of (unsigned int) –1 in <i>MaxRpcSize</i> removes the limit on the size of incoming data blocks. This parameter has no effect on calls made over the <a href="/windows/desktop/Rpc/protocol-sequence-constants">ncalrpc</a> protocol.

### -field IfCallback

A pointer to a <a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_interface_group_idle_callback_fn">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a> security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function.

### -field UuidVector

Pointer to a vector of object <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUIDs</a> offered by the server to be registered with the RPC endpoint mapper. The server application constructs this vector.  <b>NULL</b> indicates there are no object <b>UUIDs</b> to register.

### -field Annotation

Pointer to the character-string comment applied to each cross-product element added to the local endpoint-map database. The string can be up to 64 characters long, including the null terminating character. Specify a null value or a null-terminated string ("\0") if there is no annotation string.

The annotation string is used by applications for information only. RPC does not use this string to determine which server instance a client communicates with or for enumerating elements in the endpoint-map database.

### -field SecurityDescriptor

Optional security descriptor describing which clients have the right to access the interface.

## -remarks

To register an interface, the server provides the following information:<ul>
<li>Interface specification The interface specification is a data structure that the MIDL compiler generates.

</li>
<li>Manager type <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> and manager EPV The manager type <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client. For each implementation of an interface offered by a server, it must register a separate manager EPV.
Note that when specifying a non-nil, manager type <b>UUID</b>, the server must also call <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a> to register objects of this non-nil type.

</li>
</ul>


All interface group interfaces are treated as <b>auto-listen</b>.  The runtime begins listening for calls as soon as the interface group is activated.  Calls to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> and <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a> do not affect the interface, nor does a call to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverunregisterif">RpcServerUnregisterIf</a> with <i>IfSpec</i> set to <b>NULL</b>.

Specifying a security-callback function in <i>IfCallback</i> allows the server application to restrict access to its interfaces on an individual client basis. That is, by default, security is optional; the server run-time will dispatch unsecured calls even if the server has called <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>. If the server wants to accept only authenticated clients, an interface callback function must call <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient">RpcBindingInqAuthClient</a>, <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient">RpcGetAuthorizationContextForClient</a>, or <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> to retrieve the security level, or attempt to impersonate the client with <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>. It can also specify the <a href="/windows/desktop/Rpc/interface-registration-flags">RPC_IF_ALLOW_SECURE_ONLY</a> flag in <i>Flags</i> to reject unauthenticated calls.

When a server application specifies a security-callback function for its interface(s) in <i>IfCallback</i>, the RPC run time automatically rejects calls without authentication information to that interface. In addition, the run-time records the interfaces each client has used. When a client makes an RPC to an interface that it has not used during the current communication session, the RPC run-time library calls the interface's security-callback function. Specifying <a href="/windows/desktop/Rpc/interface-registration-flags">RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</a> in <i>Flags</i> will prevent the automatic rejection of unauthenticated clients. Note that calls on the <b>NULL</b> security session can have authentication information, even though they come from anonymous clients. Thus, the existence of a callback alone is not sufficient to prevent anonymous clients from connecting; either the security callback function must check for that, or the RPC_IF_ALLOW_SECURE_ONLY flag must be used. RPC_IF_ALLOW_SECURE_ONLY rejects null session calls only on Windows XP and later versions of Windows.

For the signature for the callback function, see <a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_if_callback_fn">RPC_IF_CALLBACK_FN</a>.

The callback function in <i>IfCallback</i> should return <b>RPC_S_OK</b> if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception <b>RPC_S_ACCESS_DENIED</b>.

In some cases, the RPC run time may call the security-callback function more than once per client, per interface. The callback function must be able to handle this possibility.





> [!NOTE]
> The rpcdce.h header defines RPC_INTERFACE_TEMPLATE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_interface_group_idle_callback_fn">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInqBindings</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>

