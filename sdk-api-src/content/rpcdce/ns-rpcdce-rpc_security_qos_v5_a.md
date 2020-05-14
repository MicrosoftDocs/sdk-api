---
UID: NS:rpcdce._RPC_SECURITY_QOS_V5_A
title: RPC_SECURITY_QOS_V5_A (rpcdce.h)
description: The RPC_SECURITY_QOS_V5 structure defines version 5 security quality-of-service settings on a binding handle. See Remarks for version availability on Windows editions.helpviewer_keywords: ["*PRPC_SECURITY_QOS_V5_A","0","PRPC_SECURITY_QOS_V5","PRPC_SECURITY_QOS_V5 structure pointer [RPC]","RPC_C_AUTHN_INFO_TYPE_HTTP","RPC_C_IMP_LEVEL_ANONYMOUS","RPC_C_IMP_LEVEL_DEFAULT","RPC_C_IMP_LEVEL_DELEGATE","RPC_C_IMP_LEVEL_IDENTIFY","RPC_C_IMP_LEVEL_IMPERSONATE","RPC_C_QOS_CAPABILITIES_ANY_AUTHORITY","RPC_C_QOS_CAPABILITIES_DEFAULT","RPC_C_QOS_CAPABILITIES_IGNORE_DELEGATE_FAILURE","RPC_C_QOS_CAPABILITIES_LOCAL_MA_HINT","RPC_C_QOS_CAPABILITIES_MAKE_FULLSIC","RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH","RPC_C_QOS_IDENTITY_DYNAMIC","RPC_C_QOS_IDENTITY_STATIC","RPC_SECURITY_QOS_V5","RPC_SECURITY_QOS_V5 structure [RPC]","RPC_SECURITY_QOS_V5_A","RPC_SECURITY_QOS_V5_W","_RPC_SECURITY_QOS_V5_A","_RPC_SECURITY_QOS_V5_W","rpc.rpc_security_qos_v5","rpcdce/PRPC_SECURITY_QOS_V5","rpcdce/RPC_SECURITY_QOS_V5"]
old-location: rpc\rpc_security_qos_v5.htm
tech.root: Rpc
ms.assetid: 7032ECE6-1D38-4DB8-990D-2FA6F08371C1
ms.date: 12/05/2018
ms.keywords: '*PRPC_SECURITY_QOS_V5_A, 0, PRPC_SECURITY_QOS_V5, PRPC_SECURITY_QOS_V5 structure pointer [RPC], RPC_C_AUTHN_INFO_TYPE_HTTP, RPC_C_IMP_LEVEL_ANONYMOUS, RPC_C_IMP_LEVEL_DEFAULT, RPC_C_IMP_LEVEL_DELEGATE, RPC_C_IMP_LEVEL_IDENTIFY, RPC_C_IMP_LEVEL_IMPERSONATE, RPC_C_QOS_CAPABILITIES_ANY_AUTHORITY, RPC_C_QOS_CAPABILITIES_DEFAULT, RPC_C_QOS_CAPABILITIES_IGNORE_DELEGATE_FAILURE, RPC_C_QOS_CAPABILITIES_LOCAL_MA_HINT, RPC_C_QOS_CAPABILITIES_MAKE_FULLSIC, RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH, RPC_C_QOS_IDENTITY_DYNAMIC, RPC_C_QOS_IDENTITY_STATIC, RPC_SECURITY_QOS_V5, RPC_SECURITY_QOS_V5 structure [RPC], RPC_SECURITY_QOS_V5_A, RPC_SECURITY_QOS_V5_W, _RPC_SECURITY_QOS_V5_A, _RPC_SECURITY_QOS_V5_W, rpc.rpc_security_qos_v5, rpcdce/PRPC_SECURITY_QOS_V5, rpcdce/RPC_SECURITY_QOS_V5'
f1_keywords:
- rpcdce/RPC_SECURITY_QOS_V5
dev_langs:
- c++
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Rpcdce.h
api_name:
- RPC_SECURITY_QOS_V5
- RPC_SECURITY_QOS_V5_A
- RPC_SECURITY_QOS_V5_W
targetos: Windows
req.typenames: RPC_SECURITY_QOS_V5_A, *PRPC_SECURITY_QOS_V5_A
req.redist: 
ms.custom: 19H1
---

# RPC_SECURITY_QOS_V5_A structure


## -description


The <b>RPC_SECURITY_QOS_V5</b> structure defines version 5  security quality-of-service settings on a binding handle. See Remarks for version availability on Windows editions.


## -struct-fields




### -field Version

Version of the <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a> structure being used. This topic documents version 5 of the <b>RPC_SECURITY_QOS</b> structure. See <b>RPC_SECURITY_QOS</b>, <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v2_a">RPC_SECURITY_QOS_V2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v3_a">RPC_SECURITY_QOS_V3</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v4_a">RPC_SECURITY_QOS_V4</a> for other versions.


### -field Capabilities

Security services being provided to the application. <i>Capabilities</i> is a set of flags that can be combined using the bitwise OR operator.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_DEFAULT"></a><a id="rpc_c_qos_capabilities_default"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
No provider-specific capabilities are needed.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH"></a><a id="rpc_c_qos_capabilities_mutual_auth"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The RPC run time  requests mutual authentication from the security provider. Some security providers do not support mutual authentication. If the security provider does not support mutual authentication, or the identity of the server cannot be established, a remote procedure call to such server fails with error RPC_S_SEC_PKG_ERROR.

<div class="alert"><b>Note</b>  RPC relies on the SSP to indicate which security options were successfully negotiated; in turn an RPC call fails if the SSP reports  it could not negotiate an option. However, some security providers are known to report the successful negotiation of an option even when the option was not successfully negotiated. For example, NTLM will report successful negotiation of mutual authentication for backward compatibility reasons, even though it does not support mutual authentication. Check with the particular SSP being used to determine its behavior with respect to security options.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_MAKE_FULLSIC"></a><a id="rpc_c_qos_capabilities_make_fullsic"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_MAKE_FULLSIC</b></dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_ANY_AUTHORITY"></a><a id="rpc_c_qos_capabilities_any_authority"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_ANY_AUTHORITY</b></dt>
</dl>
</td>
<td width="60%">
Accepts the client's credentials even if the certificate authority (CA) is not in the server's list of trusted CAs. This constant is used only by the SCHANNEL SSP.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_IGNORE_DELEGATE_FAILURE"></a><a id="rpc_c_qos_capabilities_ignore_delegate_failure"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_IGNORE_DELEGATE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The RPC runtime on the client ignores an error to establish a security context that supports delegation. Normally, if the client asks for delegation and the security system cannot establish a security context that supports delegation, error RPC_S_SEC_PKG_ERROR is returned; when this flag is specified, no error is returned.

<div class="alert"><b>Note</b>  Unsupported on Windows XP and earlier client editions, unsupported on Windows 2000 and earlier server editions.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_CAPABILITIES_LOCAL_MA_HINT"></a><a id="rpc_c_qos_capabilities_local_ma_hint"></a><dl>
<dt><b>RPC_C_QOS_CAPABILITIES_LOCAL_MA_HINT</b></dt>
</dl>
</td>
<td width="60%">
The server is local to the machine making the RPC call. In this situation RPC instructs the endpoint mapper to pick up only endpoints registered by the principal specified in the <b>ServerPrincName</b> or <b>Sid</b> members (these members are available in <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v3_a">RPC_SECURITY_QOS_V3</a>, <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v4_a">RPC_SECURITY_QOS_V4</a>, and <b>RPC_SECURITY_QOS_V5</b> only). See Remarks for more information.

<div class="alert"><b>Note</b>  Unsupported on Windows XP and earlier client editions, unsupported on Windows 2000 and earlier server editions.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field IdentityTracking

The context tracking mode as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_IDENTITY_STATIC"></a><a id="rpc_c_qos_identity_static"></a><dl>
<dt><b>RPC_C_QOS_IDENTITY_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The security context is created only once and is never revised during the entire communication, even if the client side changes it. This is the default behavior if <b>RPC_SECURITY_QOS_V5</b> is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_QOS_IDENTITY_DYNAMIC"></a><a id="rpc_c_qos_identity_dynamic"></a><dl>
<dt><b>RPC_C_QOS_IDENTITY_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
The Security context is revised whenever the ModifiedId in the client's token is changed. All protocols use the ModifiedId (see note).

<b>Windows 2000:  </b>All remote protocols (all protocols other than <a href="https://docs.microsoft.com/windows/desktop/Midl/ncalrpc">ncalrpc</a>) use the AuthenticationID, also known as the LogonId, to track changes in the client's identity. The <b>ncalrpc</b> protocol uses  ModifiedId.

</td>
</tr>
</table>
 


### -field ImpersonationType

The level at which the server process can impersonate the client. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_IMP_LEVEL_DEFAULT"></a><a id="rpc_c_imp_level_default"></a><dl>
<dt><b>RPC_C_IMP_LEVEL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Uses the default impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_IMP_LEVEL_ANONYMOUS"></a><a id="rpc_c_imp_level_anonymous"></a><dl>
<dt><b>RPC_C_IMP_LEVEL_ANONYMOUS</b></dt>
</dl>
</td>
<td width="60%">
The client does not provide identification information to the server. The server cannot impersonate the client or identify the client. Many servers reject calls with this impersonation type.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_IMP_LEVEL_IDENTIFY"></a><a id="rpc_c_imp_level_identify"></a><dl>
<dt><b>RPC_C_IMP_LEVEL_IDENTIFY</b></dt>
</dl>
</td>
<td width="60%">
The server can obtain the client's identity, and impersonate the client to perform Access Control List (ACL) checks, but cannot impersonate the client.  See <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/impersonation-levels">Impersonation Levels</a> for more information.

<div class="alert"><b>Note</b>  Some security providers may treat this impersonation type as equivalent to RPC_C_IMP_LEVEL_IMPERSONATE. </div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_IMP_LEVEL_IMPERSONATE"></a><a id="rpc_c_imp_level_impersonate"></a><dl>
<dt><b>RPC_C_IMP_LEVEL_IMPERSONATE</b></dt>
</dl>
</td>
<td width="60%">
The server can impersonate the client's security context on its local system, but not on remote systems.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_IMP_LEVEL_DELEGATE"></a><a id="rpc_c_imp_level_delegate"></a><dl>
<dt><b>RPC_C_IMP_LEVEL_DELEGATE</b></dt>
</dl>
</td>
<td width="60%">
The server can impersonate the client's security context while acting on behalf of the client. The server can also make outgoing calls to other servers while acting on behalf of the client. The server may use the client's security context on other machines to access local and remote resources as the client.

</td>
</tr>
</table>
 


### -field AdditionalSecurityInfoType

The type of additional credentials present in the <b>u</b> union. The following constants are supported:

<table>
<tr>
<th>Supported Constants</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
No additional credentials are passed in the <b>u</b> union.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_AUTHN_INFO_TYPE_HTTP"></a><a id="rpc_c_authn_info_type_http"></a><dl>
<dt><b>RPC_C_AUTHN_INFO_TYPE_HTTP</b></dt>
</dl>
</td>
<td width="60%">
The <b>HttpCredentials</b> member of the <b>u</b> union points to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_a">RPC_HTTP_TRANSPORT_CREDENTIALS</a> structure. This value can be used only when the protocol sequence is <a href="https://msdn.microsoft.com/">ncacn_http</a>. Any other protocol sequence returns RPC_S_INVALID_ARG.

</td>
</tr>
</table>
 


### -field u


### -field u.HttpCredentials

Additional set of credentials to pass to RPC, in the form of an <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_a">RPC_HTTP_TRANSPORT_CREDENTIALS</a> structure. Used when the  <b>AdditionalSecurityInfoType</b> member is set to RPC_C_AUTHN_INFO_TYPE_HTTP.


### -field Sid

Pointer to a security identifier (SID). The SID is an alternative to the <b>ServerPrincName</b> member, and only one can be specified. The <b>Sid</b> member cannot be set to non-<b>NULL</b> if the security provider is the SCHANNEL SSP. Some protocol sequences use  <b>Sid</b> internally for security, and some use a <b>ServerPrincName</b>. For example, <a href="https://docs.microsoft.com/windows/desktop/Midl/ncalrpc">ncalrpc</a> uses a <b>Sid</b> internally, and if the caller knows both the SID and the <b>ServerPrincName</b>, a call using <b>ncalrpc</b> can complete much faster in some cases if the SID is passed. In contrast, the <b>ncacn_*</b> and <b>ncadg_*</b> protocol sequences use a <b>ServerPrincName</b> internally, and therefore can execute calls faster when provided the <b>ServerPrincName</b>.


### -field EffectiveOnly

If set, only enabled privileges are seen by the server.


### -field ServerSecurityDescriptor

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> that identifies the server. It is required for mutual authentication.


## -remarks



The following listing defines the availability of QOS versions on various Windows operating systems:

<ul>
<li>Version 1: Windows 2000 and later.</li>
<li>Version 2: Windows XP with Service Pack 1 (SP1) and later.</li>
<li>Version 3: Windows Server 2003 and later.</li>
<li>Version 4: Windows Vista and later.</li>
<li>Version 5: Windows 8 and later.</li>
</ul>
Windows editions support downlevel versions as well. For example, Windows Server 2003 supports version 3, but also supports versions 1 and 2. 

The client-side security functions 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa">RpcBindingInqAuthInfoEx</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> use the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a> structure to inquire about, or to set, the security quality of service for a binding handle.

RPC supports the RPC_C_QOS_CAPABILITIES_LOCAL_MA_HINT hint (unsupported on Windows XP and earlier client editions, unsupported on Windows 2000 and earlier server editions). This hint is used only when dynamic endpoints and mutual authentication are used. Furthermore, it is not supported for the <b>ncadg_*</b> protocol sequences. If this flag is used for a <b>ncadg_*</b> protocol sequence, or without using mutual authentication, RPC_S_INVALID_ARG is returned from the <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a> function call.
This flag is designed to prevent a Denial of Service Attack. Using this flag forces the RPC Runtime to ask the endpoint mapper only for endpoints registered by the principal specified in the <b>ServerPrincName</b> or <b>Sid</b> members. This prevents an attacker on the local machine from trying to trick your RPC client to connect to a spoof endpoint it has registered in the endpoint mapper. Note that since the attack is local only (such as from a terminal server machine with many users), the flag also works only for RPC calls made locally.


<div class="alert"><b>Note</b>  Some security providers, such as Kerberos, support delegation-impersonation type. On Windows editions that support delegation-impersonation type, if the client has asked for delegation but the security provider is unable to provide it, the call fails with PRC_S_SEC_PKG_ERROR unless the RPC_C_QOS_CAPABILITIES_IGNORE_DELEGATE_FAILURE flag is specified.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a">RPC_BINDING_HANDLE_SECURITY_V1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_a">RPC_HTTP_TRANSPORT_CREDENTIALS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v2_a">RPC_SECURITY_QOS_V2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v3_a">RPC_SECURITY_QOS_V3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v4_a">RPC_SECURITY_QOS_V4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa">RpcBindingInqAuthInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a>
 

 

