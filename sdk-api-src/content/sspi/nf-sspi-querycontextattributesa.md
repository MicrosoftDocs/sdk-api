---
UID: NF:sspi.QueryContextAttributesA
title: QueryContextAttributesA function (sspi.h)
description: Lets a transport application query the Credential Security Support Provider (CredSSP) security package for certain attributes of a security context. (ANSI)
helpviewer_keywords: ["QueryContextAttributesA", "SECPKG_ATTR_CERT_TRUST_STATUS", "SECPKG_ATTR_CREDS", "SECPKG_ATTR_CREDS_2", "SECPKG_ATTR_C_ACCESS_TOKEN", "SECPKG_ATTR_C_FULL_ACCESS_TOKEN", "SECPKG_ATTR_NEGOTIATION_PACKAGE", "SECPKG_ATTR_PACKAGE_INFO", "SECPKG_ATTR_SERVER_AUTH_FLAGS", "SECPKG_ATTR_SIZES", "SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES", "sspi/QueryContextAttributesA"]
old-location: security\querycontextattributes__credssp_.htm
tech.root: security
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
ms.date: 12/05/2018
ms.keywords: QueryContextAttributes, QueryContextAttributes (CredSSP), QueryContextAttributes function [Security], QueryContextAttributesA, QueryContextAttributesW, SECPKG_ATTR_CERT_TRUST_STATUS, SECPKG_ATTR_CREDS, SECPKG_ATTR_CREDS_2, SECPKG_ATTR_C_ACCESS_TOKEN, SECPKG_ATTR_C_FULL_ACCESS_TOKEN, SECPKG_ATTR_NEGOTIATION_PACKAGE, SECPKG_ATTR_PACKAGE_INFO, SECPKG_ATTR_SERVER_AUTH_FLAGS, SECPKG_ATTR_SIZES, SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES, security.querycontextattributes__credssp_, sspi/QueryContextAttributes, sspi/QueryContextAttributesA, sspi/QueryContextAttributesW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryContextAttributesW (Unicode) and QueryContextAttributesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryContextAttributesA
 - sspi/QueryContextAttributesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
 - schannel.dll
api_name:
 - QueryContextAttributes
 - QueryContextAttributesA
 - QueryContextAttributesW
---

# QueryContextAttributesA function


## -description

The <b>QueryContextAttributes (CredSSP)</b> function lets a transport application query the Credential Security Support Provider (CredSSP) <a href="/windows/desktop/SecGloss/s-gly">security package</a> for certain <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of a <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

## -parameters

### -param phContext [in]

A  handle to the security context to be queried.

### -param ulAttribute [in]

The attribute of the context to be returned. This parameter can be one of the following values. Unless otherwise specified, the attributes are applicable to both client and server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_C_ACCESS_TOKEN"></a><a id="secpkg_attr_c_access_token"></a><dl>
<dt><b>SECPKG_ATTR_C_ACCESS_TOKEN</b></dt>
<dt>0x80000012</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_accesstoken">SecPkgContext_AccessToken</a> structure that specifies the access token for the current security context.

This attribute is supported only on the server.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></a><a id="secpkg_attr_c_full_access_token"></a><dl>
<dt><b>SECPKG_ATTR_C_FULL_ACCESS_TOKEN</b></dt>
<dt>0x80000082</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_accesstoken">SecPkgContext_AccessToken</a> structure that specifies the access token for the current security context.

This attribute is supported only on the server.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CERT_TRUST_STATUS"></a><a id="secpkg_attr_cert_trust_status"></a><dl>
<dt><b>SECPKG_ATTR_CERT_TRUST_STATUS</b></dt>
<dt>0x80000084</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a> structure that specifies trust information about the certificate.

This attribute is supported only on the client.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CREDS"></a><a id="secpkg_attr_creds"></a><dl>
<dt><b>SECPKG_ATTR_CREDS</b></dt>
<dt>0x80000080</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/credssp/ns-credssp-secpkgcontext_clientcreds">SecPkgContext_ClientCreds</a> structure that specifies client credentials.

The client credentials can be either user name and password or user name and smart card PIN.

This attribute is supported only on the server.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CREDS_2"></a><a id="secpkg_attr_creds_2"></a><dl>
<dt><b>SECPKG_ATTR_CREDS_2</b></dt>
<dt>0x80000086</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/credssp/ns-credssp-secpkgcontext_clientcreds">SecPkgContext_ClientCreds</a> structure that specifies client credentials. 

If the client credential is user name and password, the buffer is a packed <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a> structure.

If the client credential is user name and smart card PIN, the buffer is a packed 	<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a> structure.

If the client credential is an online identity credential, the buffer is a marshaled <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure.

This attribute is supported only on the CredSSP server.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></a><a id="secpkg_attr_negotiation_package"></a><dl>
<dt><b>SECPKG_ATTR_NEGOTIATION_PACKAGE</b></dt>
<dt>0x80000081</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/win32/api/sspi/ns-sspi-secpkginfoa">SecPkgContext_PackageInfo">SecPkgContext_PackageInfo</a> structure that specifies the name of the authentication package negotiated by the <a href="/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a> provider.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_PACKAGE_INFO"></a><a id="secpkg_attr_package_info"></a><dl>
<dt><b>SECPKG_ATTR_PACKAGE_INFO</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/win32/api/sspi/ns-sspi-secpkginfoa">SecPkgContext_PackageInfo">SecPkgContext_PackageInfo</a> structure.

Returns information on the SSP in use.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></a><a id="secpkg_attr_server_auth_flags"></a><dl>
<dt><b>SECPKG_ATTR_SERVER_AUTH_FLAGS</b></dt>
<dt>0x80000083</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_flags">SecPkgContext_Flags</a> structure that specifies information about the flags in the current security context.

This attribute is supported only on the client.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SIZES"></a><a id="secpkg_attr_sizes"></a><dl>
<dt><b>SECPKG_ATTR_SIZES</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a> structure.

Queries the sizes of the structures used in the per-message functions and authentication exchanges.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></a><a id="secpkg_attr_subject_security_attributes"></a><dl>
<dt><b>SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES</b></dt>
<dt>124</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_subjectattributes">SecPkgContext_SubjectAttributes</a> structure.

This value returns information about  the security attributes for the connection.

This value is supported only on the CredSSP server.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pBuffer [out]

A pointer to a structure that receives the attributes. The structure type depends on the value of the <i>ulAttribute</i> parameter.

## -returns

If the function succeeds, it returns SEC_E_OK.

If the function fails, it can return the following error codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
<dt>0x80100003</dt>
</dl>
</td>
<td width="60%">
The function failed. The <i>phContext</i> parameter specifies a handle to an incomplete context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
<dt>0x80090302</dt>
</dl>
</td>
<td width="60%">
The function failed. The value of the <i>ulAttribute</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

The structure pointed to by the <i>pBuffer</i> parameter varies depending on the attribute being queried.

While  the caller must allocate the <i>pBuffer</i> structure itself, the SSP allocates any memory required to hold variable-sized members of the <i>pBuffer</i> structure. Memory allocated by the SSP must be freed by calling the <a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.





> [!NOTE]
> The sspi.h header defines QueryContextAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/credssp/ns-credssp-secpkgcontext_clientcreds">SecPkgContext_ClientCreds</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a>
