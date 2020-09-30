---
UID: NF:wincrypt.CryptSignAndEncodeCertificate
title: CryptSignAndEncodeCertificate function (wincrypt.h)
description: Encodes and signs a certificate, certificate revocation list (CRL), certificate trust list (CTL), or certificate request.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","CryptSignAndEncodeCertificate","CryptSignAndEncodeCertificate function [Security]","X509_ASN_ENCODING","X509_CERT_CRL_TO_BE_SIGNED","X509_CERT_REQUEST_TO_BE_SIGNED","X509_CERT_TO_BE_SIGNED","X509_KEYGEN_REQUEST_TO_BE_SIGNED","_crypto2_cryptsignandencodecertificate","security.cryptsignandencodecertificate","wincrypt/CryptSignAndEncodeCertificate"]
old-location: security\cryptsignandencodecertificate.htm
tech.root: security
ms.assetid: ee138918-ed7c-4980-8b18-64004a0dd7df
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CryptSignAndEncodeCertificate, CryptSignAndEncodeCertificate function [Security], X509_ASN_ENCODING, X509_CERT_CRL_TO_BE_SIGNED, X509_CERT_REQUEST_TO_BE_SIGNED, X509_CERT_TO_BE_SIGNED, X509_KEYGEN_REQUEST_TO_BE_SIGNED, _crypto2_cryptsignandencodecertificate, security.cryptsignandencodecertificate, wincrypt/CryptSignAndEncodeCertificate
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
 - CryptSignAndEncodeCertificate
 - wincrypt/CryptSignAndEncodeCertificate
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
 - CryptSignAndEncodeCertificate
---

# CryptSignAndEncodeCertificate function


## -description

The <b>CryptSignAndEncodeCertificate</b> function encodes and signs a certificate, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL), or <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

This function performs the following operations:
<ul>
<li>Calls 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> using <i>lpszStructType</i> to encode the "to be signed" information.</li>
<li>Calls 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsigncertificate">CryptSignCertificate</a> to sign this encoded information.</li>
<li>Calls <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> again, with <i>lpszStructType</i> set to X509_CERT, to further encode the resulting signed, encoded information.</li>
</ul>

## -parameters

### -param hBCryptKey [in]

A handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to do the signature. This handle is an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle that has been created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should always pass in a <b>NCRYPT_KEY_HANDLE</b> handle of a CNG CSP.

### -param dwKeySpec [in]

Identifies the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use from the provider's container. This must be one of the following values. This parameter is ignored if a CNG key is passed in the <i>hCryptProvOrNCryptKey</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Use the key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Use the digital signature key.

</td>
</tr>
</table>

### -param dwCertEncodingType [in]

Specifies the encoding type used. This can be the following value.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
</table>

### -param lpszStructType [in]

A pointer to a null-terminated ANSI string that contains the type of data to be encoded and signed. The following predefined <i>lpszStructType</i> constants are used with encode operations.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_CRL_TO_BE_SIGNED"></a><a id="x509_cert_crl_to_be_signed"></a><dl>
<dt><b>X509_CERT_CRL_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_REQUEST_TO_BE_SIGNED"></a><a id="x509_cert_request_to_be_signed"></a><dl>
<dt><b>X509_CERT_REQUEST_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_TO_BE_SIGNED"></a><a id="x509_cert_to_be_signed"></a><dl>
<dt><b>X509_CERT_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_KEYGEN_REQUEST_TO_BE_SIGNED"></a><a id="x509_keygen_request_to_be_signed"></a><dl>
<dt><b>X509_KEYGEN_REQUEST_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_keygen_request_info">CERT_KEYGEN_REQUEST_INFO</a> structure.

</td>
</tr>
</table>

### -param pvStructInfo [in]

The address of a structure that contains the data to be signed and encoded. The format of this structure is determined by the <i>lpszStructType</i> parameter.

### -param pSignatureAlgorithm [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the signature algorithm and any additional parameters needed. This function uses the following algorithm OIDs:

<ul>
<li>szOID_RSA_MD5RSA</li>
<li>szOID_RSA_SHA1RSA</li>
<li>szOID_X957_SHA1DSA</li>
</ul>
If the signature algorithm is a <a href="/windows/desktop/SecGloss/h-gly">hash</a> algorithm, the signature contains only the unencrypted hash octets. A private key is not used to encrypt the hash. <i>dwKeySpec</i> is not used and <i>hCryptProvOrNCryptKey</i> can be <b>NULL</b> if an appropriate default CSP can be used for hashing.

### -param pvHashAuxInfo [in]

Reserved. Must be <b>NULL</b>.

### -param pbEncoded [out]

A pointer to a buffer to receive the signed and encoded output.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbEncoded</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
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
Possible error codes include, but are not limited to, the following.

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
If the buffer specified by the <i>pbEncoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbEncoded</i>.

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
The signature algorithm's OID does not map to a known or supported hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_BAD_ENCODE</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered while encoding or decoding. The most likely cause of this error is the improper initialization of the fields in the structure pointed to by <i>pvStructInfo</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsigncertificate">CryptSignCertificate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>