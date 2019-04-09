---
UID: NF:wincrypt.CryptVerifyCertificateSignatureEx
title: CryptVerifyCertificateSignatureEx function (wincrypt.h)
author: windows-sdk-content
description: Verifies the signature of a subject certificate, certificate revocation list, certificate request, or keygen request by using the issuer's public key.
old-location: security\cryptverifycertificatesignatureex.htm
tech.root: SecCrypto
ms.assetid: 8a84af66-b174-4a3e-b1d7-6f218a52d877
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CRYPT_VERIFY_CERT_SIGN_DISABLE_MD2_MD4_FLAG, CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT, CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN, CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL, CRYPT_VERIFY_CERT_SIGN_ISSUER_PUBKEY, CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG, CRYPT_VERIFY_CERT_SIGN_SET_STRONG_PROPERTIES_FLAG, CRYPT_VERIFY_CERT_SIGN_SUBJECT_BLOB, CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT, CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL, CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE, CryptVerifyCertificateSignatureEx, CryptVerifyCertificateSignatureEx function [Security], X509_ASN_ENCODING, _crypto2_cryptverifycertificatesignatureex, security.cryptverifycertificatesignatureex, wincrypt/CryptVerifyCertificateSignatureEx
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptVerifyCertificateSignatureEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptVerifyCertificateSignatureEx function


## -description


The <b>CryptVerifyCertificateSignatureEx</b> function verifies the signature of a subject certificate, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>, or keygen request by using the issuer's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>. The function does not require access to a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.


## -parameters




### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> used to verify the signature.This parameter's data type is <b>HCRYPTPROV</b>.

<b>NULL</b> is passed unless there is a strong reason for passing in a specific cryptographic provider. Passing in <b>NULL</b> causes the default RSA or DSS provider to be acquired.




### -param dwCertEncodingType [in]

The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate encoding type</a>   that was used to encrypt the subject.
					 The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


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
<i>pvSubject</i> is a pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a>structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT"></a><a id="crypt_verify_cert_sign_subject_cert"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_CERT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CCERT_CONTEXT</a>structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL"></a><a id="crypt_verify_cert_sign_subject_crl"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_CRL</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to a <a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CCRL_CONTEXT</a>structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE"></a><a id="crypt_verify_cert_sign_subject_ocsp_basic_signed_response"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> is a pointer to an <a href="https://msdn.microsoft.com/4b88a946-030f-490a-b46a-c42507e1268d">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> structure.

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
<i>pvIssuer</i> is a pointer to a <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT"></a><a id="crypt_verify_cert_sign_issuer_cert"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_CERT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> is a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CCERT_CONTEXT</a>structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN"></a><a id="crypt_verify_cert_sign_issuer_chain"></a><dl>
<dt><b>CRYPT_VERIFY_CERT_SIGN_ISSUER_CHAIN</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
<i>pvIssuer</i> is a pointer to a <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CCERT_CHAIN_CONTEXT</a>structure.

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
 

<div class="alert"><b>Note</b>  If <i>dwIssuerType</i> is <b>CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL</b> and the signature algorithm is a hashing algorithm, the signature is expected to contain only unencrypted hash octets. Only <b>CRYPT_VERIFY_CERT_SIGN_ISSUER_NULL</b> can be specified in this nonencrypted signature case. If any other <i>dwIssuerType</i> is specified, verification fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns E_INVALIDARG.</div>
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
If you set this flag and <b>CryptVerifyCertificateSignatureEx</b> detects an MD2 or MD4 algorithm, the function returns <b>FALSE</b> and sets <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to <b>NTE_BAD_ALGID</b>. The signature is still verified, but this combination of errors enables the caller, now knowing that an MD2 or MD4 algorithm was used, to decide whether to trust or reject the signature.

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
Returns a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Hh870264(v=VS.85).aspx">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure in the <i>pvExtra</i> parameter. The structure contains the length, in bits, of the public key and the  names of the signing and hashing algorithms used.

You must call <a href="https://msdn.microsoft.com/fb5c10ba-da8e-4a34-9302-67586a0a9624">CryptMemFree</a> to free the structure. If memory cannot be allocated for the <a href="https://msdn.microsoft.com/en-us/library/Hh870264(v=VS.85).aspx">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure, this function returns successfully but sets the <i>pvExtra</i> parameter to <b>NULL</b>.

<div class="alert"><b>Note</b>  This flag is only applicable if  <b>CRYPT_VERIFY_CERT_SIGN_SUBJECT_OCSP_BASIC_SIGNED_RESPONSE</b> is specified in the <i>dwSubjectType</i> parameter.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>
 


### -param pvExtra [in, out, optional]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Hh870264(v=VS.85).aspx">CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO</a> structure if the <i>dwFlags</i> parameter is set to <b>CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG</b>.

You must call <a href="https://msdn.microsoft.com/fb5c10ba-da8e-4a34-9302-67586a0a9624">CryptMemFree</a> to free the structure.


## -returns



Returns nonzero if successful or zero otherwise. 
						
						
						

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>, 
<a href="https://msdn.microsoft.com/3119eabc-90ff-42c6-b3fa-e8be625f6d1e">CryptVerifySignature</a>, and 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> may be propagated to this function.</div>
<div> </div>
On failure, this function will cause the following error codes to be returned from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
The signature algorithm's <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) does not map to a known or supported <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> algorithm.

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
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -remarks



The subject buffer can contain an encoded <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> or a context for a certificate or CRL. In the case of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, if the certificate's public key parameters are missing and if these parameters can be inherited from the certificate's issuer for example from the DSS public key parameter, the context's CERT_PUBKEY_ALG_PARA_PROP_ID property is updated with the issuer's public key algorithm parameters for a valid signature.




## -see-also




<a href="https://msdn.microsoft.com/ac13a1dd-3ca9-470e-8d8f-d79d7d057f45">CryptVerifyCertificateSignature</a>
 

 

