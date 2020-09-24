---
UID: NF:wincrypt.CryptVerifyCertificateSignature
title: CryptVerifyCertificateSignature function (wincrypt.h)
description: Verifies the signature of a certificate, certificate revocation list (CRL), or certificate request by using the public key in a CERT_PUBLIC_KEY_INFO structure.
helpviewer_keywords: ["CryptVerifyCertificateSignature","CryptVerifyCertificateSignature function [Security]","X509_ASN_ENCODING","_crypto2_cryptverifycertificatesignature","security.cryptverifycertificatesignature","wincrypt/CryptVerifyCertificateSignature"]
old-location: security\cryptverifycertificatesignature.htm
tech.root: security
ms.assetid: ac13a1dd-3ca9-470e-8d8f-d79d7d057f45
ms.date: 12/05/2018
ms.keywords: CryptVerifyCertificateSignature, CryptVerifyCertificateSignature function [Security], X509_ASN_ENCODING, _crypto2_cryptverifycertificatesignature, security.cryptverifycertificatesignature, wincrypt/CryptVerifyCertificateSignature
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
 - CryptVerifyCertificateSignature
 - wincrypt/CryptVerifyCertificateSignature
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
 - CryptVerifyCertificateSignature
---

# CryptVerifyCertificateSignature function


## -description

The <b>CryptVerifyCertificateSignature</b> function verifies the signature of a certificate, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), or <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>  by using the <a href="/windows/desktop/SecGloss/p-gly">public key</a> in a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure. The function does not require access to a <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

## -parameters

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) used to verify the signature.This parameter's data type is <b>HCRYPTPROV</b>.

<b>NULL</b> is passed unless there is a strong reason for passing in a specific cryptographic provider. Passing in <b>NULL</b> causes the default RSA or DSS provider to be acquired.

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a> that was used to encrypt the subject. The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


This parameter can be the following currently defined certificate encoding type.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
</table>

### -param pbEncoded [in]

A pointer to an encoded <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_signed_content_info">CERT_SIGNED_CONTENT_INFO</a> content on which the signature is to be verified.

### -param cbEncoded [in]

The size, in bytes, of the encoded content in <i>pbEncoded</i>.

### -param pPublicKey [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key to use when verifying the signature.

## -returns

Returns nonzero if successful or zero otherwise.
						

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> may be propagated to this function.</div>
<div> </div>
On failure, this function will cause the following error codes to be returned from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only <b>X509_ASN_ENCODING</b> is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The signature algorithm's <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) does not map to a known or supported <a href="/windows/desktop/SecGloss/h-gly">hash</a> algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The signature was not valid.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

This function currently calls the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifycertificatesignatureex">CryptVerifyCertificateSignatureEx</a> function to perform the verification.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifycertificatesignatureex">CryptVerifyCertificateSignatureEx</a>