---
UID: NF:sspi.QueryContextAttributesExW
title: QueryContextAttributesExW function
author: windows-sdk-content
description: Enables a transport application to query a security package for certain attributes of a security context.
old-location: security\querycontextattributesex.htm
old-project: secauthn
ms.assetid: FD91EE99-F94E-44CE-9331-933D0CAA5F75
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: QueryContextAttributesEx, QueryContextAttributesEx function [Security], QueryContextAttributesExA, QueryContextAttributesExW, SECPKG_ATTR_ACCESS_TOKEN, SECPKG_ATTR_APP_DATA, SECPKG_ATTR_AUTHORITY, SECPKG_ATTR_CLIENT_SPECIFIED_TARGET, SECPKG_ATTR_CONNECTION_INFO, SECPKG_ATTR_CREDS_2, SECPKG_ATTR_DCE_INFO, SECPKG_ATTR_EAP_KEY_BLOCK, SECPKG_ATTR_ENDPOINT_BINDINGS, SECPKG_ATTR_FLAGS, SECPKG_ATTR_ISSUER_LIST_EX, SECPKG_ATTR_KEY_INFO, SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS, SECPKG_ATTR_LIFESPAN, SECPKG_ATTR_LOCAL_CERT_CONTEXT, SECPKG_ATTR_LOCAL_CRED, SECPKG_ATTR_NAMES, SECPKG_ATTR_NATIVE_NAMES, SECPKG_ATTR_NEGOTIATION_INFO, SECPKG_ATTR_PACKAGE_INFO, SECPKG_ATTR_PASSWORD_EXPIRY, SECPKG_ATTR_REMOTE_CERT_CONTEXT, SECPKG_ATTR_ROOT_STORE, SECPKG_ATTR_SESSION_INFO, SECPKG_ATTR_SESSION_KEY, SECPKG_ATTR_SIZES, SECPKG_ATTR_STREAM_SIZES, SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES, SECPKG_ATTR_SUPPORTED_SIGNATURES, SECPKG_ATTR_TARGET_INFORMATION, SECPKG_ATTR_UNIQUE_BINDINGS, security.querycontextattributesex, sspi/QueryContextAttributesEx, sspi/QueryContextAttributesExA, sspi/QueryContextAttributesExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
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
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# QueryContextAttributesExW function


## -description


Enables a transport application to query a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> for certain <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of a security <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>.


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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/4dc11cbd-7f28-4cb9-aaea-6e5a89ac91f0">SecPkgContext_AccessToken</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/7bda791a-dd60-4651-bfe8-13333017d6a3">SecPkgContext_SessionAppData</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/619bf16b-c439-48e7-b013-3622e2f3bbc4">SecPkgContext_Authority</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/67536f69-a1fc-4f26-84dc-872635bafa3b">SecPkgContext_ClientSpecifiedTarget</a> structure that represents the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">service principal name</a> (SPN) of the initial target supplied by the client. 

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/5380c03b-d2c5-4a0d-96a1-c39305b9c9ac">SecPkgContext_ConnectionInfo</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3">SecPkgContext_ClientCreds</a> structure that specifies client credentials. 

If the client credential is user name and password, the buffer is a packed <a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a> structure.

If the client credential is user name and smart card PIN, the buffer is a packed 	<a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> structure.

If the client credential is an online identity credential, the buffer is a marshaled <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/490688d0-efdd-4a40-88b9-eb53ff592d2a">SecPkgContext_DceInfo</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/6823cc31-acd3-4d67-92c6-65ff4d1c6aed">SecPkgContext_Bindings</a> structure that specifies channel binding information.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/c1b1f1d1-20f9-4a16-a279-b9cc95ff4e64">SecPkgContext_EapKeyBlock</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/0be0e945-4048-4748-a9fd-15d08fb7ff3e">SecPkgContext_Flags</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/cf1ccd40-36bf-4597-b34f-d26cef63d800">SecPkgContext_IssuerListInfoEx</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/ec146329-6789-460c-ae62-629a1765a4c1">SecPkgContext_KeyInfo</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/ccb2bb4e-3c65-4305-95ad-b9111f3936b5">SecPkgContext_LastClientTokenStatus</a> structure that specifies whether the token from the most recent call to the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> function is the last token from the client.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/7ef45795-f6af-4dac-a498-c6f8c915a168">SecPkgContext_Lifespan</a> structure.


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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a>
							structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/9df0bf7c-ad5f-4cb8-8934-76062789735f">SecPkgContext_Names</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/f935093f-5661-4ced-94f1-c4b21c3b9f69">SecPkgContext_NativeNames</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/3af724b8-fbe5-4a75-b128-9efe65381f2f">SecPkgContext_NegotiationInfo</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/94c21f22-d974-4ae5-beef-d4567e6ea7e1">SecPkgContext_PackageInfo</a>
							structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/f45dde88-1520-4e65-8fae-8407dfaa0850">SecPkgContext_PasswordExpiry</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a>
							structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/88cf437e-3be0-4f12-9058-ad078deed6a1">SecPkgContext_SessionKey</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/d7725803-1f4c-4d5d-8c53-81ec24d5a9d8">SecPkgContext_SessionInfo</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/75e5fc96-56cc-4713-a34f-fca687798ad6">SecPkgContext_StreamSizes</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/548E972F-EB94-4BBD-94F2-FA38184D179A">SecPkgContext_SubjectAttributes</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/b4b58175-1367-4c91-8680-523a4b125c76">SecPkgContext_SupportedSignatures</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/8a5a6bd6-8678-4544-a631-5ee4347bc685">SecPkgContext_TargetInformation</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/6823cc31-acd3-4d67-92c6-65ff4d1c6aed">SecPkgContext_Bindings</a> structure that specifies channel binding information.

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




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/619bf16b-c439-48e7-b013-3622e2f3bbc4">SecPkgContext_Authority</a>



<a href="https://msdn.microsoft.com/5380c03b-d2c5-4a0d-96a1-c39305b9c9ac">SecPkgContext_ConnectionInfo</a>



<a href="https://msdn.microsoft.com/490688d0-efdd-4a40-88b9-eb53ff592d2a">SecPkgContext_DceInfo</a>



<a href="https://msdn.microsoft.com/cf1ccd40-36bf-4597-b34f-d26cef63d800">SecPkgContext_IssuerListInfoEx</a>



<a href="https://msdn.microsoft.com/ec146329-6789-460c-ae62-629a1765a4c1">SecPkgContext_KeyInfo</a>



<a href="https://msdn.microsoft.com/7ef45795-f6af-4dac-a498-c6f8c915a168">SecPkgContext_Lifespan</a>



<a href="https://msdn.microsoft.com/9df0bf7c-ad5f-4cb8-8934-76062789735f">SecPkgContext_Names</a>



<a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a>



<a href="https://msdn.microsoft.com/75e5fc96-56cc-4713-a34f-fca687798ad6">SecPkgContext_StreamSizes</a>
 

 

