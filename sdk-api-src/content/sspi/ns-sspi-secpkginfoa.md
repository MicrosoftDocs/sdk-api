---
UID: NS:sspi._SecPkgInfoA
title: SecPkgInfoA (sspi.h)
description: The SecPkgInfo structure provides general information about a security package, such as its name and capabilities. (ANSI)
helpviewer_keywords: ["*PSecPkgInfoA","PSecPkgInfo","PSecPkgInfo structure pointer [Security]","SECPKG_CALLFLAGS_APPCONTAINER","SECPKG_CALLFLAGS_AUTHCAPABLE","SECPKG_CALLFLAGS_FORCE_SUPPLIED","SECPKG_FLAG_ACCEPT_WIN32_NAME","SECPKG_FLAG_APPCONTAINER_CHECKS","SECPKG_FLAG_APPCONTAINER_PASSTHROUGH","SECPKG_FLAG_ASCII_BUFFERS","SECPKG_FLAG_CLIENT_ONLY","SECPKG_FLAG_CONNECTION","SECPKG_FLAG_DATAGRAM","SECPKG_FLAG_DELEGATION","SECPKG_FLAG_EXTENDED_ERROR","SECPKG_FLAG_FRAGMENT","SECPKG_FLAG_GSS_COMPATIBLE","SECPKG_FLAG_IMPERSONATION","SECPKG_FLAG_INTEGRITY","SECPKG_FLAG_LOGON","SECPKG_FLAG_MULTI_REQUIRED","SECPKG_FLAG_MUTUAL_AUTH","SECPKG_FLAG_NEGOTIABLE","SECPKG_FLAG_NEGOTIABLE2","SECPKG_FLAG_NEGO_EXTENDER","SECPKG_FLAG_PRIVACY","SECPKG_FLAG_READONLY_WITH_CHECKSUM","SECPKG_FLAG_RESTRICTED_TOKENS","SECPKG_FLAG_STREAM","SECPKG_FLAG_TOKEN_ONLY","SecPkgInfo","SecPkgInfo structure [Security]","SecPkgInfoA","SecPkgInfoW","_ssp_secpkginfo","security.secpkginfo","sspi/PSecPkgInfo","sspi/SecPkgInfo","sspi/SecPkgInfoA","sspi/SecPkgInfoW"]
old-location: security\secpkginfo.htm
tech.root: security
ms.assetid: d0bff3d8-63f1-4a4e-851f-177040af6bd2
ms.date: 12/05/2018
ms.keywords: '*PSecPkgInfoA, PSecPkgInfo, PSecPkgInfo structure pointer [Security], SECPKG_CALLFLAGS_APPCONTAINER, SECPKG_CALLFLAGS_AUTHCAPABLE, SECPKG_CALLFLAGS_FORCE_SUPPLIED, SECPKG_FLAG_ACCEPT_WIN32_NAME, SECPKG_FLAG_APPCONTAINER_CHECKS, SECPKG_FLAG_APPCONTAINER_PASSTHROUGH, SECPKG_FLAG_ASCII_BUFFERS, SECPKG_FLAG_CLIENT_ONLY, SECPKG_FLAG_CONNECTION, SECPKG_FLAG_DATAGRAM, SECPKG_FLAG_DELEGATION, SECPKG_FLAG_EXTENDED_ERROR, SECPKG_FLAG_FRAGMENT, SECPKG_FLAG_GSS_COMPATIBLE, SECPKG_FLAG_IMPERSONATION, SECPKG_FLAG_INTEGRITY, SECPKG_FLAG_LOGON, SECPKG_FLAG_MULTI_REQUIRED, SECPKG_FLAG_MUTUAL_AUTH, SECPKG_FLAG_NEGOTIABLE, SECPKG_FLAG_NEGOTIABLE2, SECPKG_FLAG_NEGO_EXTENDER, SECPKG_FLAG_PRIVACY, SECPKG_FLAG_READONLY_WITH_CHECKSUM, SECPKG_FLAG_RESTRICTED_TOKENS, SECPKG_FLAG_STREAM, SECPKG_FLAG_TOKEN_ONLY, SecPkgInfo, SecPkgInfo structure [Security], SecPkgInfoA, SecPkgInfoW, _ssp_secpkginfo, security.secpkginfo, sspi/PSecPkgInfo, sspi/SecPkgInfo, sspi/SecPkgInfoA, sspi/SecPkgInfoW'
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
targetos: Windows
req.typenames: SecPkgInfoA, *PSecPkgInfoA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgInfoA
 - sspi/_SecPkgInfoA
 - PSecPkgInfoA
 - sspi/PSecPkgInfoA
 - SecPkgInfoA
 - sspi/SecPkgInfoA
dev_langs:
 - c++
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
---

# SecPkgInfoA structure


## -description

The <b>SecPkgInfo</b> structure provides general information about a <a href="/windows/desktop/SecGloss/s-gly">security package</a>, such as its name and capabilities.

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
The security package supports the <a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> and <a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_PRIVACY"></a><a id="secpkg_flag_privacy"></a><dl>
<dt><b>SECPKG_FLAG_PRIVACY</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The security package supports the <a href="/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage (General)</a> and <a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (General)</a> functions.

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
Supports <a href="/windows/desktop/SecGloss/d-gly">datagram</a>-style authentication. For more information, see 
<a href="/windows/desktop/SecAuthN/sspi-context-semantics">SSPI Context Semantics</a>.

<div class="alert"><b>Important</b>  The <a href="/windows/desktop/SecAuthN/microsoft-kerberos">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</div>
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
<a href="/windows/desktop/SecAuthN/sspi-context-semantics">SSPI Context Semantics</a>.

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
<a href="/windows/desktop/SecAuthN/extended-error-information">Extended Error Information</a>.

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
<a href="/windows/desktop/SecAuthN/sspi-context-semantics">SSPI Context Semantics</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_FLAG_NEGOTIABLE"></a><a id="secpkg_flag_negotiable"></a><dl>
<dt><b>SECPKG_FLAG_NEGOTIABLE</b></dt>
<dt>0X800</dt>
</dl>
</td>
<td width="60%">
Can be used by the <a href="/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a> security package.

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
Supports <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.

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
Supports separating large tokens into smaller buffers so that applications can make repeated calls to <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> and <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> with the smaller buffers to complete authentication.

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
The security package supports using a checksum instead of in-place encryption when calling the <a href="/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage</a> function.

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
The security package extends the <a href="/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a> security package. There can be at most one package of this type.

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

<a href="/windows/desktop/api/sspi/nf-sspi-enumeratesecuritypackagesa">EnumerateSecurityPackages</a>



<a href="/windows/desktop/api/sspi/nf-sspi-querysecuritypackageinfoa">QuerySecurityPackageInfo</a>

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
