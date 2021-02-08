---
UID: NC:wincrypt.PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC
title: PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC (wincrypt.h)
description: Called to sign and encode a computed hash.
helpviewer_keywords: ["PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC","PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC callback","PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC callback function [Security]","security.pfn_crypt_sign_and_encode_hash_func","wincrypt/PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC"]
old-location: security\pfn_crypt_sign_and_encode_hash_func.htm
tech.root: security
ms.assetid: d393a092-64a2-47b7-90a4-5144b99cd6b5
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC, PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC callback, PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC callback function [Security], security.pfn_crypt_sign_and_encode_hash_func, wincrypt/PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC
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
 - PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC
 - wincrypt/PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC
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
 - PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC
---

# PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC callback function


## -description

The <b>PFN_CRYPT_SIGN_AND_ENCODE_HASH_FUNC</b> callback function is called to sign and encode a computed hash.

## -parameters

### -param hKey [in]

A handle to the Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use to sign the hash.

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pSignatureAlgorithm [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and its optional encoded parameters.

### -param pvDecodedSignPara [in]

An optional pointer to the decoded signature parameters data structure previously returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func">PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC</a>  function.

### -param pwszCNGPubKeyAlgid [in]

A Unicode string that contains the CNG <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a> identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b>.

### -param pwszCNGHashAlgid [in]

A Unicode string that contains the CNG hash algorithm identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b> or to a hash algorithm identifier in <i>pvDecodedSignPara</i>.

### -param pbComputedHash [in]

A pointer to the computed hash bytes returned by the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function that corresponds to <i>pwszCNGHashAlgid</i>.

### -param cbComputedHash [in]

A value that represents the length, in bytes, of the computed hash.

### -param pbSignature [out]

A pointer to the encoded signature bytes.

### -param pcbSignature [in, out]

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
<td>CRYPT_OID_SIGN_AND_ENCODE_HASH_FUNC</td>
<td>"CryptDllSignAndEncodeHash"</td>
</tr>
</table>
