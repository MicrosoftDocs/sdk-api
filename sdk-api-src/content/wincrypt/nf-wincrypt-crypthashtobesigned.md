---
UID: NF:wincrypt.CryptHashToBeSigned
title: CryptHashToBeSigned function (wincrypt.h)
description: Important  This API is deprecated. (CryptHashToBeSigned)
helpviewer_keywords: ["CryptHashToBeSigned","CryptHashToBeSigned function [Security]","_crypto2_crypthashtobesigned","security.crypthashtobesigned","wincrypt/CryptHashToBeSigned"]
old-location: security\crypthashtobesigned.htm
tech.root: security
ms.assetid: 84477054-dd76-4dde-b465-9edeaf192714
ms.date: 12/05/2018
ms.keywords: CryptHashToBeSigned, CryptHashToBeSigned function [Security], _crypto2_crypthashtobesigned, security.crypthashtobesigned, wincrypt/CryptHashToBeSigned
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CryptHashToBeSigned
 - wincrypt/CryptHashToBeSigned
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
 - CryptHashToBeSigned
---

# CryptHashToBeSigned function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptHashToBeSigned</b> function computes the <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the encoded content from a signed and encoded <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. The hash is performed on only the "to be signed" encoded content and its signature.

## -parameters

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use to compute the hash.This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, zero is passed in. Passing in zero causes the default <a href="/windows/desktop/SecGloss/r-gly">RSA</a> or <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Standard</a> (DSS) provider to be acquired before doing hash, <a href="/windows/desktop/SecGloss/s-gly">signature verification</a>, or recipient <a href="/windows/desktop/SecGloss/e-gly">encryption</a> operations.

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbEncoded [in]

Address of a buffer that contains the content to be hashed. This is the encoded form of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_signed_content_info">CERT_SIGNED_CONTENT_INFO</a>.

### -param cbEncoded [in]

The size, in bytes, of the buffer.

### -param pbComputedHash [out]

A pointer to a buffer to receive the computed hash.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbComputedHash [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbComputedHash</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).
For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> might be propagated to this function. This function has the following error codes.</div>
<div> </div>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbComputedHash</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbComputedHash</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only X509_ASN_ENCODING is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the signature algorithm does not map to a known or supported hash algorithm.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashpublickeyinfo">CryptHashPublicKeyInfo</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
