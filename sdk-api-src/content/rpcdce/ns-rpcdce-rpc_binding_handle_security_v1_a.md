---
UID: NS:rpcdce._RPC_BINDING_HANDLE_SECURITY_V1_A
title: RPC_BINDING_HANDLE_SECURITY_V1_A (rpcdce.h)
description: Contains the basic security options with which to create an RPC binding handle. (ANSI)
helpviewer_keywords: ["*PRPC_BINDING_HANDLE_SECURITY_V1_A","RPC_BINDING_HANDLE_SECURITY","RPC_BINDING_HANDLE_SECURITY structure [RPC]","RPC_BINDING_HANDLE_SECURITY_V1","RPC_BINDING_HANDLE_SECURITY_V1 structure [RPC]","RPC_BINDING_HANDLE_SECURITY_V1_A","RPC_BINDING_HANDLE_SECURITY_V1_W","_RPC_BINDING_HANDLE_SECURITY_V1_A","_RPC_BINDING_HANDLE_SECURITY_V1_W","rpc.rpc_binding_handle_security_v1","rpcdce/RPC_BINDING_HANDLE_SECURITY","rpcdce/RPC_BINDING_HANDLE_SECURITY_V1"]
old-location: rpc\rpc_binding_handle_security_v1.htm
tech.root: Rpc
ms.assetid: b8ea2e96-2e7e-428c-a5cd-dfe9dd341063
ms.date: 12/05/2018
ms.keywords: '*PRPC_BINDING_HANDLE_SECURITY_V1_A, RPC_BINDING_HANDLE_SECURITY, RPC_BINDING_HANDLE_SECURITY structure [RPC], RPC_BINDING_HANDLE_SECURITY_V1, RPC_BINDING_HANDLE_SECURITY_V1 structure [RPC], RPC_BINDING_HANDLE_SECURITY_V1_A, RPC_BINDING_HANDLE_SECURITY_V1_W, _RPC_BINDING_HANDLE_SECURITY_V1_A, _RPC_BINDING_HANDLE_SECURITY_V1_W, rpc.rpc_binding_handle_security_v1, rpcdce/RPC_BINDING_HANDLE_SECURITY, rpcdce/RPC_BINDING_HANDLE_SECURITY_V1'
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_BINDING_HANDLE_SECURITY_V1_A, *PRPC_BINDING_HANDLE_SECURITY_V1_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_BINDING_HANDLE_SECURITY_V1_A
 - rpcdce/_RPC_BINDING_HANDLE_SECURITY_V1_A
 - PRPC_BINDING_HANDLE_SECURITY_V1_A
 - rpcdce/PRPC_BINDING_HANDLE_SECURITY_V1_A
 - RPC_BINDING_HANDLE_SECURITY_V1_A
 - rpcdce/RPC_BINDING_HANDLE_SECURITY_V1_A
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
 - RPC_BINDING_HANDLE_SECURITY_V1
 - RPC_BINDING_HANDLE_SECURITY_V1_A
 - RPC_BINDING_HANDLE_SECURITY_V1_W
---

# RPC_BINDING_HANDLE_SECURITY_V1_A structure


## -description

The <b>RPC_BINDING_HANDLE_SECURITY_V1</b> structure contains the basic security options with which to create an RPC binding handle.

## -struct-fields

### -field Version

The version of this structure. For <b>RPC_BINDING_HANDLE_SECURITY_V1</b> this must be set to 1.

### -field ServerPrincName

Pointer to a string that contains the server principal name referenced by the binding handle. The content of the name and its syntax are defined by the authentication service in use.

### -field AuthnLevel

Level of authentication to be performed on remote procedure calls made using this binding handle. For a list of the RPC-supported authentication levels, see 
<a href="/windows/desktop/Rpc/authentication-level-constants">Authentication-Level Constants</a>.

If <i>AuthnSvc</i> is set to RPC_C_AUTHN_NONE, this member must likewise be set to RPC_C_AUTHN_NONE.

### -field AuthnSvc

Authentication service to use when binding. 




Specify RPC_C_AUTHN_NONE to turn off authentication for remote procedure calls made using the binding handle.

If RPC_C_AUTHN_DEFAULT is specified, the RPC run-time library uses the RPC_C_AUTHN_WINNT authentication service for remote procedure calls made using the binding handle.

If <i>AuthnLevel</i> is set to RPC_C_AUTHN_NONE, this member must likewise be set to RPC_C_AUTHN_NONE.

### -field AuthIdentity

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure that contains the client's authentication and authorization credentials appropriate for the selected authentication and authorization service.

### -field SecurityQos

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a> structure that contains the security quality-of-service settings for the binding handle. 




<div class="alert"><b>Note</b>  For a list of the RPC-supported authentication services, see 
<a href="/windows/desktop/Rpc/authentication-service-constants">Authentication-Service Constants</a>.</div>
<div> </div>

## -remarks

If this structure is not passed to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a> -- that is, if the <i>Security</i> parameter of <b>RpcBindingCreate</b> is set to <b>NULL</b> -- then the following default security behaviors are assumed:


<ul>
<li>For the protocol sequence ncalrpc (local RPC), RPC will use transport-level security. This means that RPC will use the security mechanisms offered by the Windows kernel to provide security, and RPC will not authenticate the server since it connects using the current thread identity. In this case, the identity tracking is static, the impersonation type is set to "Impersonate", and the authentication level is set to "Privacy".</li>
<li>For the protocol sequence ncacn_np, RPC will also use transport-level security. If the call is remote, RPC uses the security mechanisms provided by the Windows file system redirector and there is no mutual authentication. In this case, the identity is the current thread identity, the identity tracking state is static, the impersonation type is set to "Impersonate", and the authentication level is determined by the policies of the remote machine.

If the call is local, RPC uses the security mechanisms provided by the Named Pipe File System (NPFS), and there is also no mutual authentication. In this case, the identity is the current thread identity or any identity established through the "net use" command for the server. The identity tracking state is dynamic, the impersonation type is set to "Impersonate", and the authentication level is set to "Privacy".

</li>
<li>For the protocol sequences ncacn_ip_tcp, ncacn_ip_udp  and ncacn_http, no security is used when <i>Security</i> is set to <b>NULL</b>. The server will not perform impersonation, and all data will be sent as clear text. To provide maximum protection for data, the application must always provide security data.</li>
</ul>


The following table summarizes the default security settings for the different protocol sequences if the <i>Security</i> parameter of <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a> is set to <b>NULL</b>.

<table>
<tr>
<th>Default Security Settings</th>
<th>ncalrpc</th>
<th>local ncacn_np</th>
<th>remote ncacn_np</th>
<th>ncacn_ip_tcp, ncacn_ip_udp, and ncacn_http</th>
</tr>
<tr>
<th>Security Mechanism</th>
<td>Windows Kernel</td>
<td>NPFS</td>
<td>File system redirector</td>
<td>None</td>
</tr>
<tr>
<th>Authentication Level</th>
<td>Privacy</td>
<td>Privacy</td>
<td>Server policy dependent</td>
<td>None</td>
</tr>
<tr>
<th>Mutual Authentication?</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>Impersonation Type</th>
<td>Impersonate</td>
<td>Impersonate</td>
<td>Impersonate</td>
<td>N/A</td>
</tr>
<tr>
<th>Identity Tracking Type</th>
<td>Static</td>
<td>Dynamic</td>
<td>Static</td>
<td>N/A</td>
</tr>
<tr>
<th>Effective Only?</th>
<td>Yes</td>
<td>No</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr>
<th>Call Identity</th>
<td>Current thread</td>
<td>Current thread</td>
<td>Current thread or "net use" settings</td>
<td>N/A</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you create your binding handle by calling the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a> API, the default identity tracking for ncalrpc in the absence of specific security settings is dynamic. <p class="note">If you create a fast binding handle by calling the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a> API, the default identity tracking for ncalrpc in the absence of specific security settings is static.

<p class="note">You should be aware of the differences in these two APIs if you are switching between them in your application.

<p class="note">After the binding handle is created, the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> and <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a> APIs can be used to change the settings of the binding handle set with this structure.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingbind">RpcBindingBind</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a>
