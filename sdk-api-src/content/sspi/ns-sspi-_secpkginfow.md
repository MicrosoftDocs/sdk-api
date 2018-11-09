---
UID: NS:sspi._SecPkgInfoW
title: "_SecPkgInfoW"
author: windows-sdk-content
description: The SecPkgInfo structure provides general information about a security package, such as its name and capabilities.
old-location: security\secpkginfo.htm
tech.root: secauthn
ms.assetid: d0bff3d8-63f1-4a4e-851f-177040af6bd2
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PSecPkgInfoW, PSecPkgInfo, PSecPkgInfo structure pointer [Security], SECPKG_CALLFLAGS_APPCONTAINER, SECPKG_CALLFLAGS_AUTHCAPABLE, SECPKG_CALLFLAGS_FORCE_SUPPLIED, SECPKG_FLAG_ACCEPT_WIN32_NAME, SECPKG_FLAG_APPCONTAINER_CHECKS, SECPKG_FLAG_APPCONTAINER_PASSTHROUGH, SECPKG_FLAG_ASCII_BUFFERS, SECPKG_FLAG_CLIENT_ONLY, SECPKG_FLAG_CONNECTION, SECPKG_FLAG_DATAGRAM, SECPKG_FLAG_DELEGATION, SECPKG_FLAG_EXTENDED_ERROR, SECPKG_FLAG_FRAGMENT, SECPKG_FLAG_GSS_COMPATIBLE, SECPKG_FLAG_IMPERSONATION, SECPKG_FLAG_INTEGRITY, SECPKG_FLAG_LOGON, SECPKG_FLAG_MULTI_REQUIRED, SECPKG_FLAG_MUTUAL_AUTH, SECPKG_FLAG_NEGOTIABLE, SECPKG_FLAG_NEGOTIABLE2, SECPKG_FLAG_NEGO_EXTENDER, SECPKG_FLAG_PRIVACY, SECPKG_FLAG_READONLY_WITH_CHECKSUM, SECPKG_FLAG_RESTRICTED_TOKENS, SECPKG_FLAG_STREAM, SECPKG_FLAG_TOKEN_ONLY, SecPkgInfo, SecPkgInfo structure [Security], SecPkgInfoA, SecPkgInfoW, _SecPkgInfoW, _ssp_secpkginfo, security.secpkginfo, sspi/PSecPkgInfo, sspi/SecPkgInfo, sspi/SecPkgInfoA, sspi/SecPkgInfoW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgInfoW (Unicode) and SecPkgInfoA (ANSI)
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
 - Sspi.h
api_name:
 - SecPkgInfo
 - SecPkgInfoA
 - SecPkgInfoW
product: Windows
targetos: Windows
req.typenames: SecPkgInfoW, *PSecPkgInfoW
req.redist: 
---

# _SecPkgInfoW structure


## -description


The <b>SecPkgInfo</b> structure provides general information about a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>, such as its name and capabilities.


## -struct-fields




### -field fCapabilities

Set of bit flags that describes the capabilities of the security package. This member can be a combination of the following flags. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_INTEGRITY"></a><a id="secpkg_flag_integrity"></a><dl>
<dt><b>SECPKG_FLAG_INTEGRITY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The security package supports the <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> and <a href="https://msdn.microsoft.com/bebeef92-1d6e-4879-846f-12d706db0653">VerifySignature</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_PRIVACY"></a><a id="secpkg_flag_privacy"></a><dl>
<dt><b>SECPKG_FLAG_PRIVACY</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The security package supports the <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage (General)</a> and <a href="https://msdn.microsoft.com/ea271d0c-9167-41c5-8919-09611206fc71">DecryptMessage (General)</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_TOKEN_ONLY"></a><a id="secpkg_flag_token_only"></a><dl>
<dt><b>SECPKG_FLAG_TOKEN_ONLY</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The package is interested only in the security-token portion of messages, and will ignore any other buffers. This is a performance-related issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_DATAGRAM"></a><a id="secpkg_flag_datagram"></a><dl>
<dt><b>SECPKG_FLAG_DATAGRAM</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Supports <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">datagram</a>-style authentication. For more information, see 
<a href="https://msdn.microsoft.com/6c87448b-5b8d-4694-ac3f-be83a258fbb0">SSPI Context Semantics</a>.

<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/e7870e72-1386-4818-bf6f-73430ae942a8">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_CONNECTION"></a><a id="secpkg_flag_connection"></a><dl>
<dt><b>SECPKG_FLAG_CONNECTION</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Supports connection-oriented style authentication. For more information, see 
<a href="https://msdn.microsoft.com/6c87448b-5b8d-4694-ac3f-be83a258fbb0">SSPI Context Semantics</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_MULTI_REQUIRED"></a><a id="secpkg_flag_multi_required"></a><dl>
<dt><b>SECPKG_FLAG_MULTI_REQUIRED</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Multiple legs are required for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_CLIENT_ONLY"></a><a id="secpkg_flag_client_only"></a><dl>
<dt><b>SECPKG_FLAG_CLIENT_ONLY</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Server authentication support is not provided.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_EXTENDED_ERROR"></a><a id="secpkg_flag_extended_error"></a><dl>
<dt><b>SECPKG_FLAG_EXTENDED_ERROR</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Supports extended error handling. For more information, see 
<a href="https://msdn.microsoft.com/a15c61f0-03cc-462f-b5c1-8e7f062e9523">Extended Error Information</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_IMPERSONATION"></a><a id="secpkg_flag_impersonation"></a><dl>
<dt><b>SECPKG_FLAG_IMPERSONATION</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
Supports Windows impersonation in server contexts.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_ACCEPT_WIN32_NAME"></a><a id="secpkg_flag_accept_win32_name"></a><dl>
<dt><b>SECPKG_FLAG_ACCEPT_WIN32_NAME</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Understands Windows principal and target names.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_STREAM"></a><a id="secpkg_flag_stream"></a><dl>
<dt><b>SECPKG_FLAG_STREAM</b></dt>
<dt>0x400</dt>
</dl>
</td>
<td width="60%">
Supports stream semantics. For more information, see 
<a href="https://msdn.microsoft.com/6c87448b-5b8d-4694-ac3f-be83a258fbb0">SSPI Context Semantics</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_NEGOTIABLE"></a><a id="secpkg_flag_negotiable"></a><dl>
<dt><b>SECPKG_FLAG_NEGOTIABLE</b></dt>
<dt>0X800</dt>
</dl>
</td>
<td width="60%">
Can be used by the <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a> security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_GSS_COMPATIBLE"></a><a id="secpkg_flag_gss_compatible"></a><dl>
<dt><b>SECPKG_FLAG_GSS_COMPATIBLE</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Supports GSS compatibility.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_LOGON"></a><a id="secpkg_flag_logon"></a><dl>
<dt><b>SECPKG_FLAG_LOGON</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Supports <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_ASCII_BUFFERS"></a><a id="secpkg_flag_ascii_buffers"></a><dl>
<dt><b>SECPKG_FLAG_ASCII_BUFFERS</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Token buffers are in ASCII characters format.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_FRAGMENT"></a><a id="secpkg_flag_fragment"></a><dl>
<dt><b>SECPKG_FLAG_FRAGMENT</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Supports separating large tokens into smaller buffers so that applications can make repeated calls to <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> and <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> with the smaller buffers to complete authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_MUTUAL_AUTH"></a><a id="secpkg_flag_mutual_auth"></a><dl>
<dt><b>SECPKG_FLAG_MUTUAL_AUTH</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
Supports mutual authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_DELEGATION"></a><a id="secpkg_flag_delegation"></a><dl>
<dt><b>SECPKG_FLAG_DELEGATION</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
Supports delegation.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_READONLY_WITH_CHECKSUM"></a><a id="secpkg_flag_readonly_with_checksum"></a><dl>
<dt><b>SECPKG_FLAG_READONLY_WITH_CHECKSUM</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
The security package supports using a checksum instead of in-place encryption when calling the <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_RESTRICTED_TOKENS"></a><a id="secpkg_flag_restricted_tokens"></a><dl>
<dt><b>SECPKG_FLAG_RESTRICTED_TOKENS</b></dt>
<dt>0x80000</dt>
</dl>
</td>
<td width="60%">
Supports callers with restricted tokens.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_NEGO_EXTENDER"></a><a id="secpkg_flag_nego_extender"></a><dl>
<dt><b>SECPKG_FLAG_NEGO_EXTENDER</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The security package extends the <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a> security package. There can be at most one package of this type.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_NEGOTIABLE2"></a><a id="secpkg_flag_negotiable2"></a><dl>
<dt><b>SECPKG_FLAG_NEGOTIABLE2</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
This package is negotiated by the package of type <b>SECPKG_FLAG_NEGO_EXTENDER</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_APPCONTAINER_PASSTHROUGH"></a><a id="secpkg_flag_appcontainer_passthrough"></a><dl>
<dt><b>SECPKG_FLAG_APPCONTAINER_PASSTHROUGH</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
This package receives all calls from app container apps. 

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_APPCONTAINER_CHECKS"></a><a id="secpkg_flag_appcontainer_checks"></a><dl>
<dt><b>SECPKG_FLAG_APPCONTAINER_CHECKS</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
This package receives calls from app container apps if one of the following checks succeeds. 

<ul>
<li>Caller has default credentials capability.</li>
<li>The target is a proxy server.</li>
<li>The caller has supplied credentials.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALLFLAGS_APPCONTAINER"></a><a id="secpkg_callflags_appcontainer"></a><dl>
<dt><b>SECPKG_CALLFLAGS_APPCONTAINER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The caller is an app container.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALLFLAGS_AUTHCAPABLE"></a><a id="secpkg_callflags_authcapable"></a><dl>
<dt><b>SECPKG_CALLFLAGS_AUTHCAPABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The caller can use default credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALLFLAGS_FORCE_SUPPLIED"></a><a id="secpkg_callflags_force_supplied"></a><dl>
<dt><b>SECPKG_CALLFLAGS_FORCE_SUPPLIED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The caller can only use supplied credentials.

</td>
</tr>
</table>
 


### -field wVersion

Specifies the version of the package protocol. Must be 1.


### -field wRPCID

Specifies a DCE RPC identifier, if appropriate. If the package does not implement one of the DCE registered security systems, the reserved value SECPKG_ID_NONE is used.


### -field cbMaxToken

Specifies the maximum size, in bytes, of the token.


### -field Name

Pointer to a null-terminated string that contains the name of the security package.


### -field Name.string

 


### -field Comment

Pointer to a null-terminated string. This can be any additional string passed back by the package.


### -field Comment.string

 




## -see-also




<a href="https://msdn.microsoft.com/900790a6-111d-43f5-9316-e85aab03a3bc">EnumerateSecurityPackages</a>



<a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a>
 

 

