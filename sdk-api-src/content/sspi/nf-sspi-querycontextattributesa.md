---
UID: NF:sspi.QueryContextAttributesA
title: QueryContextAttributesA function
author: windows-sdk-content
description: Lets a transport application query the Credential Security Support Provider (CredSSP) security package for certain attributes of a security context.
old-location: security\querycontextattributes__credssp_.htm
tech.root: secauthn
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QueryContextAttributes, QueryContextAttributes (CredSSP), QueryContextAttributes function [Security], QueryContextAttributesA, QueryContextAttributesW, SECPKG_ATTR_CERT_TRUST_STATUS, SECPKG_ATTR_CREDS, SECPKG_ATTR_CREDS_2, SECPKG_ATTR_C_ACCESS_TOKEN, SECPKG_ATTR_C_FULL_ACCESS_TOKEN, SECPKG_ATTR_NEGOTIATION_PACKAGE, SECPKG_ATTR_PACKAGE_INFO, SECPKG_ATTR_SERVER_AUTH_FLAGS, SECPKG_ATTR_SIZES, SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES, security.querycontextattributes__credssp_, sspi/QueryContextAttributes, sspi/QueryContextAttributesA, sspi/QueryContextAttributesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - QueryContextAttributes
 - QueryContextAttributesA
 - QueryContextAttributesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryContextAttributesA function


## -description


The <b>QueryContextAttributes (CredSSP)</b> function lets a transport application query the Credential Security Support Provider (CredSSP) <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> for certain <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.


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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/4dc11cbd-7f28-4cb9-aaea-6e5a89ac91f0">SecPkgContext_AccessToken</a> structure that specifies the access token for the current security context.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/4dc11cbd-7f28-4cb9-aaea-6e5a89ac91f0">SecPkgContext_AccessToken</a> structure that specifies the access token for the current security context.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure that specifies trust information about the certificate.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3">SecPkgContext_ClientCreds</a> structure that specifies client credentials.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3">SecPkgContext_ClientCreds</a> structure that specifies client credentials. 

If the client credential is user name and password, the buffer is a packed <a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a> structure.

If the client credential is user name and smart card PIN, the buffer is a packed 	<a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> structure.

If the client credential is an online identity credential, the buffer is a marshaled <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/94c21f22-d974-4ae5-beef-d4567e6ea7e1">SecPkgContext_PackageInfo</a> structure that specifies the name of the authentication package negotiated by the <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a> provider.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_PACKAGE_INFO"></a><a id="secpkg_attr_package_info"></a><dl>
<dt><b>SECPKG_ATTR_PACKAGE_INFO</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/94c21f22-d974-4ae5-beef-d4567e6ea7e1">SecPkgContext_PackageInfo</a>structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/0be0e945-4048-4748-a9fd-15d08fb7ff3e">SecPkgContext_Flags</a> structure that specifies information about the flags in the current security context.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a> structure.

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
The <i>pBuffer</i> parameter contains a pointer to a <a href="https://msdn.microsoft.com/548E972F-EB94-4BBD-94F2-FA38184D179A">SecPkgContext_SubjectAttributes</a> structure.

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

While  the caller must allocate the <i>pBuffer</i> structure itself, the SSP allocates any memory required to hold variable-sized members of the <i>pBuffer</i> structure. Memory allocated by the SSP must be freed by calling the <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="authentication_functions.htm">SSPI Functions</a>



<a href="https://msdn.microsoft.com/85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3">SecPkgContext_ClientCreds</a>



<a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a>
 

 

