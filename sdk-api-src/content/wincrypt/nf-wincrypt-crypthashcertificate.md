---
UID: NF:wincrypt.CryptHashCertificate
title: CryptHashCertificate function (wincrypt.h)
description: The CryptHashCertificate function hashes the entire encoded content of a certificate including its signature.
helpviewer_keywords: ["CryptHashCertificate","CryptHashCertificate function [Security]","_crypto2_crypthashcertificate","security.crypthashcertificate","wincrypt/CryptHashCertificate"]
old-location: security\crypthashcertificate.htm
tech.root: security
ms.assetid: a5beba30-f32b-4d57-8a54-7d9096459c50
ms.date: 12/05/2018
ms.keywords: CryptHashCertificate, CryptHashCertificate function [Security], _crypto2_crypthashcertificate, security.crypthashcertificate, wincrypt/CryptHashCertificate
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
 - CryptHashCertificate
 - wincrypt/CryptHashCertificate
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
 - CryptHashCertificate
---

# CryptHashCertificate function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptHashCertificate</b> function <a href="/windows/desktop/SecGloss/h-gly">hashes</a> the entire encoded content of a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> including its signature.

## -parameters

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use to compute the hash. 


This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific CSP in <i>hCryptProv</i>, zero is passed in. Passing in zero causes the default <a href="/windows/desktop/SecGloss/r-gly">RSA</a> or <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Standard</a> (DSS) provider to be acquired before doing hash, signature verification, or recipient encryption operations.

### -param Algid [in]

An 
						<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> structure that specifies the <a href="/windows/desktop/SecGloss/h-gly">hash algorithm</a> to use. If <i>Algid</i> is zero, the default hash algorithm, SHA1, is used.

### -param dwFlags [in]

Value to be passed to the hash API. For details, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>.

### -param pbEncoded [in]

Address of the encoded content to be hashed.

### -param cbEncoded [in]

The size, in bytes, of the encoded content.

### -param pbComputedHash [out]

A pointer to a buffer to receive the computed hash. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbComputedHash [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbComputedHash</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> might be propagated to this function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashpublickeyinfo">CryptHashPublicKeyInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>