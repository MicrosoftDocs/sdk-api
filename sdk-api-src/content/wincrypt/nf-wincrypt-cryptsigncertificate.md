---
UID: NF:wincrypt.CryptSignCertificate
title: CryptSignCertificate function (wincrypt.h)
description: The CryptSignCertificate function signs the &quot;to be signed&quot; information in the encoded signed content.
helpviewer_keywords: ["CryptSignCertificate","CryptSignCertificate function [Security]","_crypto2_cryptsigncertificate","security.cryptsigncertificate","wincrypt/CryptSignCertificate"]
old-location: security\cryptsigncertificate.htm
tech.root: security
ms.assetid: 27578149-e5c0-47e5-8309-0d0ed7075d13
ms.date: 12/05/2018
ms.keywords: CryptSignCertificate, CryptSignCertificate function [Security], _crypto2_cryptsigncertificate, security.cryptsigncertificate, wincrypt/CryptSignCertificate
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
 - CryptSignCertificate
 - wincrypt/CryptSignCertificate
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
 - CryptSignCertificate
---

# CryptSignCertificate function


## -description

The <b>CryptSignCertificate</b> function signs the "to be signed" information in the encoded signed content.

## -parameters

### -param hBCryptKey [in]

Handle of the <a href="/windows/desktop/SecGloss/c-gly">CSP</a> that does the signature. This handle must be an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle that has been created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should always pass in the <b>NCRYPT_KEY_HANDLE</b> handle of a CNG CSP.

### -param dwKeySpec [in]

Identifies the private key to use from the provider's container. It can be AT_KEYEXCHANGE or AT_SIGNATURE. This parameter is ignored if an <b>NCRYPT_KEY_HANDLE</b> is used in the <i>hCryptProvOrNCryptKey</i> parameter.

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbEncodedToBeSigned [in]

A pointer to the encoded content to be signed.

### -param cbEncodedToBeSigned [in]

The size, in bytes, of the encoded content, <i>pbEncodedToBeSigned</i>.

### -param pSignatureAlgorithm [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure with a <b>pszObjId</b> member set to one of the following:

<ul>
<li>szOID_RSA_MD5RSA</li>
<li>szOID_RSA_SHA1RSA</li>
<li>szOID_X957_SHA1DSA</li>
<li>szOID_RSA_SSA_PSS</li>
<li>szOID_ECDSA_SPECIFIED</li>
</ul>
If the signature algorithm is a hash algorithm, the signature contains only the un-encrypted hash octets. A private key is not used to encrypt the hash. <i>dwKeySpec</i> is not used and <i>hCryptProvOrNCryptKey</i> can be <b>NULL</b> if an appropriate default CSP can be used for hashing.

### -param pvHashAuxInfo [in]

Not currently used. Must be <b>NULL</b>.

### -param pbSignature [out]

A pointer to a buffer to receive the signed <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the content.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbSignature [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbSignature</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> might be propagated to this function.</div>
<div> </div>
This function has the following error codes.

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
If the buffer specified by the <i>pbSignature</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbSignature</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The signature algorithm's <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) does not map to a known or supported hash algorithm.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencodecertificate">CryptSignAndEncodeCertificate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>