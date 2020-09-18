---
UID: NF:wincrypt.CertIsStrongHashToSign
title: CertIsStrongHashToSign function (wincrypt.h)
description: Determines whether the specified hash algorithm and the public key in the signing certificate can be used to perform strong signing.
helpviewer_keywords: ["CertIsStrongHashToSign","CertIsStrongHashToSign function [Security]","security.certisstronghashtosign","wincrypt/CertIsStrongHashToSign"]
old-location: security\certisstronghashtosign.htm
tech.root: security
ms.assetid: B498C1F0-1EFF-49AF-9CD4-A447F79256F1
ms.date: 12/05/2018
ms.keywords: CertIsStrongHashToSign, CertIsStrongHashToSign function [Security], security.certisstronghashtosign, wincrypt/CertIsStrongHashToSign
req.header: wincrypt.h
req.include-header: 
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertIsStrongHashToSign
 - wincrypt/CertIsStrongHashToSign
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertIsStrongHashToSign
---

# CertIsStrongHashToSign function


## -description

Determines whether the specified hash algorithm and the public key in the signing certificate can be used to perform strong signing.

## -parameters

### -param pStrongSignPara [in]

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure that contains information about supported signing and hashing algorithms.

### -param pwszCNGHashAlgid [in]

Pointer to a Unicode string that contains the name of the hashing algorithm. The following algorithms are supported:

<ul>
<li>L"MD5" (BCRYPT_MD5_ALGORITHM)</li>
<li>L"SHA1" (BCRYPT_SHA1_ALGORITHM)</li>
<li>L"SHA256" (BCRYPT_SHA256_ALGORITHM)</li>
<li>L"SHA256" (BCRYPT_SHA256_ALGORITHM)</li>
<li>L"SHA512" (BCRYPT_SHA512_ALGORITHM)</li>
</ul>

### -param pSigningCert [in, optional]

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that  contains the signing certificate. The public key algorithm in the signing certificate is checked for strength. The public key (asymmetric) algorithm is used for signing. The following signature algorithms are supported:

<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>
This parameter can be <b>NULL</b> if you want to check only whether the hashing algorithm is strong.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.
For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. This function has the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input arguments is not correct.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
A specified algorithm is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a>