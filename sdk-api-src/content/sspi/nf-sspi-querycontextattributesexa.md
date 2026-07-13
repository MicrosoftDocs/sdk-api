---
UID: NF:sspi.QueryContextAttributesExA
title: QueryContextAttributesExA function (sspi.h)
description: The QueryContextAttributesExA (ANSI) function (sspi.h) enables a transport application to query a security package for certain attributes of a security context.
helpviewer_keywords: ["QueryContextAttributesExA", "SECPKG_ATTR_ACCESS_TOKEN", "SECPKG_ATTR_APP_DATA", "SECPKG_ATTR_AUTHORITY", "SECPKG_ATTR_CLIENT_SPECIFIED_TARGET", "SECPKG_ATTR_CONNECTION_INFO", "SECPKG_ATTR_CREDS_2", "SECPKG_ATTR_DCE_INFO", "SECPKG_ATTR_EAP_KEY_BLOCK", "SECPKG_ATTR_ENDPOINT_BINDINGS", "SECPKG_ATTR_FLAGS", "SECPKG_ATTR_ISSUER_LIST_EX", "SECPKG_ATTR_KEY_INFO", "SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS", "SECPKG_ATTR_LIFESPAN", "SECPKG_ATTR_LOCAL_CERT_CONTEXT", "SECPKG_ATTR_LOCAL_CRED", "SECPKG_ATTR_NAMES", "SECPKG_ATTR_NATIVE_NAMES", "SECPKG_ATTR_NEGOTIATION_INFO", "SECPKG_ATTR_PACKAGE_INFO", "SECPKG_ATTR_PASSWORD_EXPIRY", "SECPKG_ATTR_REMOTE_CERT_CONTEXT", "SECPKG_ATTR_ROOT_STORE", "SECPKG_ATTR_SESSION_INFO", "SECPKG_ATTR_SESSION_KEY", "SECPKG_ATTR_SIZES", "SECPKG_ATTR_STREAM_SIZES", "SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES", "SECPKG_ATTR_SUPPORTED_SIGNATURES", "SECPKG_ATTR_TARGET_INFORMATION", "SECPKG_ATTR_UNIQUE_BINDINGS", "sspi/QueryContextAttributesExA"]
old-location: security\querycontextattributesex.htm
tech.root: security
ms.assetid: FD91EE99-F94E-44CE-9331-933D0CAA5F75
ms.date: 08/03/2022
ms.keywords: QueryContextAttributesEx, QueryContextAttributesEx function [Security], QueryContextAttributesExA, QueryContextAttributesExW, SECPKG_ATTR_ACCESS_TOKEN, SECPKG_ATTR_APP_DATA, SECPKG_ATTR_AUTHORITY, SECPKG_ATTR_CLIENT_SPECIFIED_TARGET, SECPKG_ATTR_CONNECTION_INFO, SECPKG_ATTR_CREDS_2, SECPKG_ATTR_DCE_INFO, SECPKG_ATTR_EAP_KEY_BLOCK, SECPKG_ATTR_ENDPOINT_BINDINGS, SECPKG_ATTR_FLAGS, SECPKG_ATTR_ISSUER_LIST_EX, SECPKG_ATTR_KEY_INFO, SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS, SECPKG_ATTR_LIFESPAN, SECPKG_ATTR_LOCAL_CERT_CONTEXT, SECPKG_ATTR_LOCAL_CRED, SECPKG_ATTR_NAMES, SECPKG_ATTR_NATIVE_NAMES, SECPKG_ATTR_NEGOTIATION_INFO, SECPKG_ATTR_PACKAGE_INFO, SECPKG_ATTR_PASSWORD_EXPIRY, SECPKG_ATTR_REMOTE_CERT_CONTEXT, SECPKG_ATTR_ROOT_STORE, SECPKG_ATTR_SESSION_INFO, SECPKG_ATTR_SESSION_KEY, SECPKG_ATTR_SIZES, SECPKG_ATTR_STREAM_SIZES, SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES, SECPKG_ATTR_SUPPORTED_SIGNATURES, SECPKG_ATTR_TARGET_INFORMATION, SECPKG_ATTR_UNIQUE_BINDINGS, security.querycontextattributesex, sspi/QueryContextAttributesEx, sspi/QueryContextAttributesExA, sspi/QueryContextAttributesExW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryContextAttributesExW (Unicode) and QueryContextAttributesExA (ANSI)
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
 - QueryContextAttributesExA
 - sspi/QueryContextAttributesExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - QueryContextAttributesEx
 - QueryContextAttributesExA
 - QueryContextAttributesExW
---

# QueryContextAttributesExA function


## -description

Enables a transport application to query a <a href="/windows/desktop/SecGloss/s-gly">security package</a> for certain <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of a security <a href="/windows/desktop/SecGloss/c-gly">context</a>.

## -parameters

### -param phContext [in]

A handle to the security context to be queried.

### -param ulAttribute [in]

Specifies the attribute of the context to be returned. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_ACCESS_TOKEN"></a><a id="secpkg_attr_access_token"></a><dl>
<dt><b>SECPKG_ATTR_ACCESS_TOKEN</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_accesstoken">SecPkgContext_AccessToken</a> structure.

Returns a handle to the access token.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_APP_DATA"></a><a id="secpkg_attr_app_data"></a><dl>
<dt><b>SECPKG_ATTR_APP_DATA</b></dt>
<dt>0x5e</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_sessionappdata">SecPkgContext_SessionAppData</a> structure.

Returns or specifies application data for the session.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_AUTHORITY"></a><a id="secpkg_attr_authority"></a><dl>
<dt><b>SECPKG_ATTR_AUTHORITY</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_authoritya">SecPkgContext_Authority</a> structure.

Queries the name of the authenticating authority.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></a><a id="secpkg_attr_client_specified_target"></a><dl>
<dt><b>SECPKG_ATTR_CLIENT_SPECIFIED_TARGET</b></dt>
<dt>27</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget">SecPkgContext_ClientSpecifiedTarget</a> structure that represents the <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN) of the initial target supplied by the client. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CONNECTION_INFO"></a><a id="secpkg_attr_connection_info"></a><dl>
<dt><b>SECPKG_ATTR_CONNECTION_INFO</b></dt>
<dt>0x5a</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo">SecPkgContext_ConnectionInfo</a> structure.

Returns detailed information on the established connection.

This attribute is supported only by the Schannel security package.

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
<td width="40%"><a id="SECPKG_ATTR_DCE_INFO"></a><a id="secpkg_attr_dce_info"></a><dl>
<dt><b>SECPKG_ATTR_DCE_INFO</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_dceinfo">SecPkgContext_DceInfo</a> structure.

Queries for authorization data used by DCE services.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_ENDPOINT_BINDINGS"></a><a id="secpkg_attr_endpoint_bindings"></a><dl>
<dt><b>SECPKG_ATTR_ENDPOINT_BINDINGS</b></dt>
<dt>26</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings">SecPkgContext_Bindings</a> structure that specifies channel binding information.

This attribute is supported only by the Schannel security package.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_EAP_KEY_BLOCK"></a><a id="secpkg_attr_eap_key_block"></a><dl>
<dt><b>SECPKG_ATTR_EAP_KEY_BLOCK</b></dt>
<dt>0x5b</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_eapkeyblock">SecPkgContext_EapKeyBlock</a> structure.

Queries for key data used by the EAP TLS protocol.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_FLAGS"></a><a id="secpkg_attr_flags"></a><dl>
<dt><b>SECPKG_ATTR_FLAGS</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_flags">SecPkgContext_Flags</a> structure.

Returns information about the negotiated context flags.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_ISSUER_LIST_EX"></a><a id="secpkg_attr_issuer_list_ex"></a><dl>
<dt><b>SECPKG_ATTR_ISSUER_LIST_EX</b></dt>
<dt>0x59</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex">SecPkgContext_IssuerListInfoEx</a> structure.

Returns a list of certificate issuers that are accepted by the server.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_KEY_INFO"></a><a id="secpkg_attr_key_info"></a><dl>
<dt><b>SECPKG_ATTR_KEY_INFO</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_keyinfoa">SecPkgContext_KeyInfo</a> structure.

Queries information about the keys used in a security context.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></a><a id="secpkg_attr_last_client_token_status"></a><dl>
<dt><b>SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS</b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus">SecPkgContext_LastClientTokenStatus</a> structure that specifies whether the token from the most recent call to the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> function is the last token from the client.

This value is supported only by the Negotiate, Kerberos, and NTLM security packages.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_LIFESPAN"></a><a id="secpkg_attr_lifespan"></a><dl>
<dt><b>SECPKG_ATTR_LIFESPAN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_lifespan">SecPkgContext_Lifespan</a> structure.

Queries the life span of the context.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_LOCAL_CERT_CONTEXT"></a><a id="secpkg_attr_local_cert_context"></a><dl>
<dt><b>SECPKG_ATTR_LOCAL_CERT_CONTEXT</b></dt>
<dt>0x54</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCCERT_CONTEXT</a> structure.

Finds a certificate context that contains a local end certificate.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_LOCAL_CRED"></a><a id="secpkg_attr_local_cred"></a><dl>
<dt><b>SECPKG_ATTR_LOCAL_CRED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <b>SecPkgContext_LocalCredentialInfo</b> structure. (obsolete)

Superseded by SECPKG_ATTR_LOCAL_CERT_CONTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_NAMES"></a><a id="secpkg_attr_names"></a><dl>
<dt><b>SECPKG_ATTR_NAMES</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_namesa">SecPkgContext_Names</a> structure.

Queries the name associated with the context.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_NATIVE_NAMES"></a><a id="secpkg_attr_native_names"></a><dl>
<dt><b>SECPKG_ATTR_NATIVE_NAMES</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-_secpkgcontext_nativenamesa">SecPkgContext_NativeNames</a> structure.

Returns the principal name (CNAME) from the outbound ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_NEGOTIATION_INFO"></a><a id="secpkg_attr_negotiation_info"></a><dl>
<dt><b>SECPKG_ATTR_NEGOTIATION_INFO</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa">SecPkgContext_NegotiationInfo</a> structure.

Returns information about the security package to be used with the negotiation process and the current state of the negotiation for the use of that package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_PACKAGE_INFO"></a><a id="secpkg_attr_package_info"></a><dl>
<dt><b>SECPKG_ATTR_PACKAGE_INFO</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/win32/api/sspi/ns-sspi-secpkgcontext_packageinfoa">SecPkgContext_PackageInfo</a> structure.


Returns information on the SSP in use.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_PASSWORD_EXPIRY"></a><a id="secpkg_attr_password_expiry"></a><dl>
<dt><b>SECPKG_ATTR_PASSWORD_EXPIRY</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_passwordexpiry">SecPkgContext_PasswordExpiry</a> structure.

Returns password expiration information.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_REMOTE_CERT_CONTEXT"></a><a id="secpkg_attr_remote_cert_context"></a><dl>
<dt><b>SECPKG_ATTR_REMOTE_CERT_CONTEXT</b></dt>
<dt>0x53</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCCERT_CONTEXT</a> structure.

Finds a certificate context that contains the end certificate supplied by the server.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_ROOT_STORE"></a><a id="secpkg_attr_root_store"></a><dl>
<dt><b>SECPKG_ATTR_ROOT_STORE</b></dt>
<dt>0x55</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <b>HCERTCONTEXT</b>.
							Finds a certificate context that contains a certificate supplied by the Root store.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SESSION_KEY"></a><a id="secpkg_attr_session_key"></a><dl>
<dt><b>SECPKG_ATTR_SESSION_KEY</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sessionkey">SecPkgContext_SessionKey</a> structure.

Returns information about the session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SESSION_INFO"></a><a id="secpkg_attr_session_info"></a><dl>
<dt><b>SECPKG_ATTR_SESSION_INFO</b></dt>
<dt>0x5d</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_sessioninfo">SecPkgContext_SessionInfo</a> structure.

Returns information about the session.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SIZES"></a><a id="secpkg_attr_sizes"></a><dl>
<dt><b>SECPKG_ATTR_SIZES</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a> structure.

Queries the sizes of the structures used in the per-message functions.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_STREAM_SIZES"></a><a id="secpkg_attr_stream_sizes"></a><dl>
<dt><b>SECPKG_ATTR_STREAM_SIZES</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_streamsizes">SecPkgContext_StreamSizes</a> structure.

Queries the sizes of the various parts of a stream used in the per-message functions.

This attribute is supported only by the Schannel security package.

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
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUPPORTED_SIGNATURES"></a><a id="secpkg_attr_supported_signatures"></a><dl>
<dt><b>SECPKG_ATTR_SUPPORTED_SIGNATURES</b></dt>
<dt>0x66</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/win32/api/schannel/ns-schannel-secpkgcontext_supportedsignatures">SecPkgContext_SupportedSignatures</a> structure.

This value returns information about  the signature types that are supported for the connection.

This value is supported only by the Schannel security package.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_TARGET_INFORMATION"></a><a id="secpkg_attr_target_information"></a><dl>
<dt><b>SECPKG_ATTR_TARGET_INFORMATION</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_targetinformation">SecPkgContext_TargetInformation</a> structure.

Returns information about the name of the remote server.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_UNIQUE_BINDINGS"></a><a id="secpkg_attr_unique_bindings"></a><dl>
<dt><b>SECPKG_ATTR_UNIQUE_BINDINGS</b></dt>
<dt>25</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings">SecPkgContext_Bindings</a> structure that specifies channel binding information.

This value is supported only by the Schannel security package.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pBuffer [out]

A pointer to a structure that receives the attributes. The type of structure pointed to depends on the value specified in the <i>ulAttribute</i> parameter.

### -param cbBuffer [in]

The size, in bytes, of the <i>pBuffer</i> parameter.

## -returns

If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value is a nonzero error code.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_authoritya">SecPkgContext_Authority</a>



<a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo">SecPkgContext_ConnectionInfo</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_dceinfo">SecPkgContext_DceInfo</a>



<a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex">SecPkgContext_IssuerListInfoEx</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_keyinfoa">SecPkgContext_KeyInfo</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_lifespan">SecPkgContext_Lifespan</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_namesa">SecPkgContext_Names</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_streamsizes">SecPkgContext_StreamSizes</a>

## -remarks

> [!NOTE]
> The sspi.h header defines QueryContextAttributesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
