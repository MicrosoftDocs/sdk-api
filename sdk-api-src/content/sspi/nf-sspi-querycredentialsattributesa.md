---
UID: NF:sspi.QueryCredentialsAttributesA
title: QueryCredentialsAttributesA function (sspi.h)
description: Retrieves the attributes of a credential, such as the name associated with the credential. (ANSI)
helpviewer_keywords: ["QueryCredentialsAttributesA", "sspi/QueryCredentialsAttributesA"]
old-location: security\querycredentialsattributes.htm
tech.root: security
ms.assetid: a8ba6f73-8469-431b-b185-183b45b2c533
ms.date: 12/05/2018
ms.keywords: QueryCredentialsAttributes, QueryCredentialsAttributes function [Security], QueryCredentialsAttributesA, QueryCredentialsAttributesW, _ssp_querycredentialsattributes, security.querycredentialsattributes, sspi/QueryCredentialsAttributes, sspi/QueryCredentialsAttributesA, sspi/QueryCredentialsAttributesW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryCredentialsAttributesW (Unicode) and QueryCredentialsAttributesA (ANSI)
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
 - QueryCredentialsAttributesA
 - sspi/QueryCredentialsAttributesA
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
 - QueryCredentialsAttributes
 - QueryCredentialsAttributesA
 - QueryCredentialsAttributesW
---

# QueryCredentialsAttributesA function


## -description

Retrieves the <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of a <a href="/windows/desktop/SecGloss/c-gly">credential</a>, such as the name associated with the credential. The information is valid for any <a href="/windows/desktop/SecGloss/s-gly">security context</a> created with the specified credential.

## -parameters

### -param phCredential [in]

A handle of the credentials to be queried.

### -param ulAttribute [in]

Specifies the <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to query. This parameter can be any of the following attributes. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_CERT</dt>
</dl>
</td>
<td width="60%">
Returns the certificate thumbprint in a <i>pbuffer</i> of type <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_cert">SecPkgCredentials_Cert</a>.

This attribute is only supported by Kerberos.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This attribute is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_NAMES</dt>
</dl>
</td>
<td width="60%">
Returns the name of a credential in a <i>pbuffer</i> of type <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_namesa">SecPkgCredentials_Names</a>.

This attribute is not supported by Schannel in WOW64 mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_SUPPORTED_ALGS</dt>
</dl>
</td>
<td width="60%">
Returns the supported algorithms in a <i>pbuffer</i> of type <a href="/previous-versions/windows/desktop/legacy/aa380102(v=vs.85)">SecPkgCred_SupportedAlgs</a>. All supported algorithms are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

This attribute is supported only by Schannel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_CIPHER_STRENGTHS</dt>
</dl>
</td>
<td width="60%">
Returns the cipher strengths in a <i>pbuffer</i> of type <a href="/previous-versions/windows/desktop/legacy/aa380101(v=vs.85)">SecPkgCred_CipherStrengths</a>.

This attribute is supported only by Schannel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_SUPPORTED_PROTOCOLS</dt>
</dl>
</td>
<td width="60%">
Returns the supported algorithms in a <i>pbuffer</i> of type <a href="/previous-versions/windows/desktop/legacy/aa380103(v=vs.85)">SecPkgCred_SupportedProtocols</a>. All supported protocols are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

This attribute is supported only by Schannel.

</td>
</tr>
</table>

### -param pBuffer [out]

A pointer to a buffer that receives the requested attribute. The type of structure returned depends on the value of <i>ulAttribute</i>.

## -returns

If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value may be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The specified <a href="/windows/desktop/SecGloss/a-gly">attribute</a> is not supported by Schannel. This return value will only be returned when the Schannel SSP is being used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory that is available is not sufficient to complete the request.

</td>
</tr>
</table>

## -remarks

The <b>QueryCredentialsAttributes</b> function allows an application to determine several characteristics of a credential, including the name associated with the specified credentials.

Querying the SECPKG_ATTR_CIPHER_STRENGTHS attribute returns a 
<a href="/previous-versions/windows/desktop/legacy/aa380101(v=vs.85)">SecPkgCred_CipherStrengths</a> structure. The cipher strength in this structure is the same as the cipher strength in the 
<a href="../schannel/ns-schannel-sch_credentials.md">SCH_CREDENTIALS</a> structure used when a credential was created.

<div class="alert"><b>Note</b>  An application can find the system default cipher strength by querying this attribute with a default credential. A default credential is created by calling 
<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> with a <b>NULL</b> <i>pAuthData</i> parameter.</div>
<div> </div>
Querying the SECPKG_ATTR_SUPPORTED_ALGS attribute returns a 
<a href="/previous-versions/windows/desktop/legacy/aa380102(v=vs.85)">SecPkgCred_SupportedAlgs</a> structure. The algorithms in this structure are compatible with those indicated in the <a href="../schannel/ns-schannel-sch_credentials.md">SCH_CREDENTIALS</a> structure used when a credential was created.

Querying the SECPKG_ATTR_SUPPORTED_PROTOCOLS attribute returns a 
<a href="/previous-versions/windows/desktop/legacy/aa380103(v=vs.85)">SecPkgCred_SupportedProtocols</a> structure that contains a bit array compatible with the <i>grbitEnabledProtocols</i> field of the <a href="../schannel/ns-schannel-sch_credentials.md">SCH_CREDENTIALS</a> structure.

The caller must allocate the structure pointed to by the <i>pBuffer</i> parameter. The <a href="/windows/desktop/SecGloss/s-gly">security package</a> allocates the buffer for any pointer returned in the <i>pBuffer</i> structure. The caller can call the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function to free any pointers allocated by the security package.





> [!NOTE]
> The sspi.h header defines QueryCredentialsAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="../schannel/ns-schannel-sch_credentials.md">SCH_CREDENTIALS</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa380101(v=vs.85)">SecPkgCred_CipherStrengths</a>



<a href="/previous-versions/windows/desktop/legacy/aa380102(v=vs.85)">SecPkgCred_SupportedAlgs</a>



<a href="/previous-versions/windows/desktop/legacy/aa380103(v=vs.85)">SecPkgCred_SupportedProtocols</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_namesa">SecPkgCredentials_Names</a>
