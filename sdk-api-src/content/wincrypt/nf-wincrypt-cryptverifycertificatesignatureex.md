---
UID: NF:wincrypt.CryptVerifyCertificateSignatureEx
title: CryptVerifyCertificateSignatureEx function (wincrypt.h)
description: Verifies the signature of a subject certificate, certificate revocation list, certificate request, or keygen request by using the issuer's public key.
helpviewer_keywords: ["CRYPT_VERIFY_CERT_SIGN_DISABLE_MD2_MD4_FLAG","CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT","CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN","CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL","CRYPT_VERIFY_CERT_SIGN_ISSUER_PUBKEY","CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG","CRYPT_VERIFY_CERT_SIGN_SET_STRONG_PROPERTIES_FLAG","CRYPT_VERIFY_CERT_SIGN_SUBJECT_BLOB","CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT","CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL","CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE","CryptVerifyCertificateSignatureEx","CryptVerifyCertificateSignatureEx function [Security]","X509_ASN_ENCODING","_crypto2_cryptverifycertificatesignatureex","security.cryptverifycertificatesignatureex","wincrypt/CryptVerifyCertificateSignatureEx"]
old-location: security\cryptverifycertificatesignatureex.htm
tech.root: security
ms.assetid: 8a84af66-b174-4a3e-b1d7-6f218a52d877
ms.date: 12/05/2018
ms.keywords: CRYPT_VERIFY_CERT_SIGN_DISABLE_MD2_MD4_FLAG, CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT, CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN, CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL, CRYPT_VERIFY_CERT_SIGN_ISSUER_PUBKEY, CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG, CRYPT_VERIFY_CERT_SIGN_SET_STRONG_PROPERTIES_FLAG, CRYPT_VERIFY_CERT_SIGN_SUBJECT_BLOB, CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT, CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL, CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE, CryptVerifyCertificateSignatureEx, CryptVerifyCertificateSignatureEx function [Security], X509_ASN_ENCODING, _crypto2_cryptverifycertificatesignatureex, security.cryptverifycertificatesignatureex, wincrypt/CryptVerifyCertificateSignatureEx
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
 - CryptVerifyCertificateSignatureEx
 - wincrypt/CryptVerifyCertificateSignatureEx
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
 - CryptVerifyCertificateSignatureEx
---

# CryptVerifyCertificateSignatureEx function


## -description

The <b>CryptVerifyCertificateSignatureEx</b> function verifies the signature of a subject certificate, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>, or keygen request by using the issuer's <a href="/windows/desktop/SecGloss/p-gly">public key</a>. The function does not require access to a <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

## -parameters

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> used to verify the signature.This parameter's data type is <b>HCRYPTPROV</b>.

<b>NULL</b> is passed unless there is a strong reason for passing in a specific cryptographic provider. Passing in <b>NULL</b> causes the default RSA or DSS provider to be acquired.

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a>   that was used to encrypt the subject.
					 The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


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
Specifies X.509 certificate encoding.

</td>
</tr>
</table>

### -param dwSubjectType [in]

The subject type. This parameter can be one of the following subject types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_BLOB"></a><a id="crypt_verify_cert_sign_subject_blob"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_BLOB</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT"></a><a id="crypt_verify_cert_sign_subject_cert"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CCERT_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL"></a><a id="crypt_verify_cert_sign_subject_crl"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CCRL_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE"></a><a id="crypt_verify_cert_sign_subject_ocsp_basic_signed_response"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_signed_response_info">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This subject type is not supported.

</td>
</tr>
</table>

### -param pvSubject [in]

A pointer to a structure of the type indicated by <i>dwSubjectType</i> that contains the signature to be verified.

### -param dwIssuerType [in]

The issuer type. This parameter can be one of the following issuer types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_PUBKEY"></a><a id="crypt_verify_cert_sign_issuer_pubkey"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_PUBKEY</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT"></a><a id="crypt_verify_cert_sign_issuer_cert"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CCERT_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN"></a><a id="crypt_verify_cert_sign_issuer_chain"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CCERT_CHAIN_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL"></a><a id="crypt_verify_cert_sign_issuer_null"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> must be <b>NULL</b>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If <i>dwIssuerType</i> is <b>CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL</b> and the signature algorithm is a hashing algorithm, the signature is expected to contain only unencrypted hash octets. Only <b>CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL</b> can be specified in this nonencrypted signature case. If any other <i>dwIssuerType</i> is specified, verification fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns E_INVALIDARG.</div>
<div> </div>

### -param pvIssuer [in]

A pointer to a structure of the type indicated by the value of <i>dwIssuerType</i>. The structure contains access to the public key needed to verify the signature.

### -param dwFlags [in]

Flags that modify the function behavior. This can be zero or a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_DISABLE_MD2_MD4_FLAG"></a><a id="crypt_verify_cert_sign_disable_md2_md4_flag"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_DISABLE_MD2_MD4_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If you set this flag and <b>CryptVerifyCertificateSignatureEx</b> detects an MD2 or MD4 algorithm, the function returns <b>FALSE</b> and sets <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to <b>NTE_BAD_ALGID</b>. The signature is still verified, but this combination of errors enables the caller, now knowing that an MD2 or MD4 algorithm was used, to decide whether to trust or reject the signature.

<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SET_STRONG_PROPERTIES_FLAG"></a><a id="crypt_verify_cert_sign_set_strong_properties_flag"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SET_STRONG_PROPERTIES_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Sets strong signature properties, after successful verification, on the subject pointed to by the <i>pvSubject</i> parameter.

The following property is set on the certificate context:

<ul>
<li><b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b></li>
</ul>
The following properties are set on the CRL context:

<ul>
<li><b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b></li>
<li><b>CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID</b></li>
</ul>
<div class="alert"><b>Note</b>  This flag is only applicable if  <b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL</b> is specified in the <i>dwSubjectType</i> parameter.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG"></a><a id="crypt_verify_cert_sign_return_strong_properties_flag"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Returns a pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_verify_cert_sign_strong_properties_info">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure in the <i>pvExtra</i> parameter. The structure contains the length, in bits, of the public key and the  names of the signing and hashing algorithms used.

You must call <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_verify_cert_sign_strong_properties_info">CryptMemFree</a> to free the structure. If memory cannot be allocated for the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_cert_sign_strong_properties_info">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure, this function returns successfully but sets the <i>pvExtra</i> parameter to <b>NULL</b>.

<div class="alert"><b>Note</b>  This flag is only applicable if  <b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE</b> is specified in the <i>dwSubjectType</i> parameter.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>

### -param pvExtra [in, out, optional]

Pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_verify_cert_sign_strong_properties_info">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure if the <i>dwFlags</i> parameter is set to <b>CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG</b>.

You must call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> to free the structure.

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
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

The subject buffer can contain an encoded <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> or a context for a certificate or CRL. In the case of a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>, if the certificate's public key parameters are missing and if these parameters can be inherited from the certificate's issuer for example from the DSS public key parameter, the context's CERT_PUBKEY_ALG_PARA_PROP_ID property is updated with the issuer's public key algorithm parameters for a valid signature.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifycertificatesignature">CryptVerifyCertificateSignature</a>