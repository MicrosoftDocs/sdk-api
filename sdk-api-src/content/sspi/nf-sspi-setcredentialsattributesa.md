---
UID: NF:sspi.SetCredentialsAttributesA
title: SetCredentialsAttributesA function (sspi.h)
description: Sets the attributes of a credential, such as the name associated with the credential. (ANSI)
helpviewer_keywords: ["SetCredentialsAttributesA", "sspi/SetCredentialsAttributesA"]
old-location: security\setcredentialsattributes.htm
tech.root: security
ms.assetid: 419fb4f0-3dd1-4473-aeb2-8024355e0c1c
ms.date: 12/05/2018
ms.keywords: SetCredentialsAttributes, SetCredentialsAttributes function [Security], SetCredentialsAttributesA, SetCredentialsAttributesW, security.setcredentialsattributes, sspi/SetCredentialsAttributes, sspi/SetCredentialsAttributesA, sspi/SetCredentialsAttributesW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetCredentialsAttributesW (Unicode) and SetCredentialsAttributesA (ANSI)
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
 - SetCredentialsAttributesA
 - sspi/SetCredentialsAttributesA
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
 - SetCredentialsAttributes
 - SetCredentialsAttributesA
 - SetCredentialsAttributesW
---

# SetCredentialsAttributesA function


## -description

Sets the <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of a <a href="/windows/desktop/SecGloss/c-gly">credential</a>, such as the name associated with the credential. The information is valid for any <a href="/windows/desktop/SecGloss/s-gly">security context</a> created with the specified credential.

## -parameters

### -param phCredential [in]

A handle of the credentials to be set.

### -param ulAttribute [in]

Specifies the <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to set. This parameter can be any of the following attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_NAMES</dt>
</dl>
</td>
<td width="60%">
Sets the name of a credential in a <i>pBuffer</i> parameter of type <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_namesa">SecPkgCredentials_Names</a>.

This attribute is not supported by Schannel in WOW64 mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_KDC_PROXY_SETTINGS</dt>
</dl>
</td>
<td width="60%">
Sets the Kerberos proxy setting in a  <i>pBuffer</i> parameter of type <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_kdcproxysettingsw">SecPkgCredentials_KdcProxySettings</a>.

This attribute is only supported by Kerberos.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_SUPPORTED_ALGS</dt>
</dl>
</td>
<td width="60%">
Sets the supported algorithms in a  <i>pBuffer</i> parameter of type <a href="/previous-versions/windows/desktop/legacy/aa380102(v=vs.85)">SecPkgCred_SupportedAlgs</a>. All supported algorithms are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

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
Sets the cipher strengths in a <i>pBuffer</i> parameter of type <a href="/previous-versions/windows/desktop/legacy/aa380101(v=vs.85)">SecPkgCred_CipherStrengths</a>.

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
Sets the supported algorithms in a <i>pBuffer</i> parameter of type <a href="/previous-versions/windows/desktop/legacy/aa380103(v=vs.85)">SecPkgCred_SupportedProtocols</a>. All supported protocols are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

This attribute is supported only by Schannel.

</td>
</tr>
</table>

### -param pBuffer [in]

A pointer to a buffer that contains the new attribute value. The type of structure returned depends on the value of <i>ulAttribute</i>.

### -param cbBuffer

The size, in bytes, of the <i>pBuffer</i> buffer.

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
Not enough memory is available to complete the request.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="../schannel/ns-schannel-sch_credentials.md">SCH_CREDENTIALS</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa380101(v=vs.85)">SecPkgCred_CipherStrengths</a>



<a href="/previous-versions/windows/desktop/legacy/aa380102(v=vs.85)">SecPkgCred_SupportedAlgs</a>



<a href="/previous-versions/windows/desktop/legacy/aa380103(v=vs.85)">SecPkgCred_SupportedProtocols</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcredentials_namesa">SecPkgCredentials_Names</a>

## -remarks

> [!NOTE]
> The sspi.h header defines SetCredentialsAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
