---
UID: NC:wincrypt.PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
title: PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC (wincrypt.h)
description: Called to decrypt an encoded signature and compare it to a computed hash.
helpviewer_keywords: ["PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC","PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback","PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback function [Security]","security.pfn_crypt_verify_encoded_signature_func","wincrypt/PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC"]
old-location: security\pfn_crypt_verify_encoded_signature_func.htm
tech.root: security
ms.assetid: 0093ce11-8b72-403d-a3fd-3eaf2dc29d71
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC, PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback, PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback function [Security], security.pfn_crypt_verify_encoded_signature_func, wincrypt/PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
 - wincrypt/PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
---

# PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback function


## -description

The <b>PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC</b> callback function is called to decrypt an encoded signature and compare it to a computed hash.

## -parameters

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pPubKeyInfo [in]

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the <a href="/windows/desktop/SecGloss/p-gly">public key</a> to use to verify the signature. You can use this with <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2">CryptImportPublicKeyInfoEx2</a> to get a <b>BCRYPT_KEY_HANDLE</b>.

### -param pSignatureAlgorithm [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and its optional encoded parameters.

### -param pvDecodedSignPara [in, optional]

An optional pointer to the decoded signature parameters data structure previously returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func">PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC</a>  function.

### -param pwszCNGPubKeyAlgid [in]

A Unicode string that contains the Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a> identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b>.

### -param pwszCNGHashAlgid [in]

A Unicode string that contains the CNG <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b> or to a hash algorithm identifier in <i>pvDecodedSignPara</i>.

### -param pbComputedHash [in]

A pointer to the computed hash bytes returned by the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function that corresponds to <i>pwszCNGHashAlgid</i>.

### -param cbComputedHash [in]

A value that represents the length, in bytes, of the computed hash.

### -param pbSignature [in]

A pointer to the encoded signature bytes.

### -param cbSignature [in]

A value that represents the length, in bytes, of the encoded signature.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If this callback function does not support the signature algorithm, it must return <b>FALSE</b> and call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with <b>ERROR_NOT_SUPPORTED</b>.

## -remarks

You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_VERIFY_ENCODED_SIGNATURE_FUNC</td>
<td>"CryptDllVerifyEncodedSignature"</td>
</tr>
</table>
