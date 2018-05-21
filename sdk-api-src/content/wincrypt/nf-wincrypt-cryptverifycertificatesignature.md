---
UID: NF:wincrypt.CryptVerifyCertificateSignature
title: CryptVerifyCertificateSignature function
author: windows-driver-content
description: Verifies the signature of a certificate, certificate revocation list (CRL), or certificate request by using the public key in a CERT_PUBLIC_KEY_INFO structure.
old-location: security\cryptverifycertificatesignature.htm
old-project: SecCrypto
ms.assetid: ac13a1dd-3ca9-470e-8d8f-d79d7d057f45
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CryptVerifyCertificateSignature, CryptVerifyCertificateSignature function [Security], X509_ASN_ENCODING, _crypto2_cryptverifycertificatesignature, security.cryptverifycertificatesignature, wincrypt/CryptVerifyCertificateSignature
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptVerifyCertificateSignature
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptVerifyCertificateSignature function


## -description



			The <b>CryptVerifyCertificateSignature</b> function verifies the signature of a certificate, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL), or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>  by using the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> in a 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure. The function does not require access to a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.


## -parameters




### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) used to verify the signature.This parameter's data type is <b>HCRYPTPROV</b>.

<b>NULL</b> is passed unless there is a strong reason for passing in a specific cryptographic provider. Passing in <b>NULL</b> causes the default RSA or DSS provider to be acquired.




### -param dwCertEncodingType [in]

The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate encoding type</a> that was used to encrypt the subject. The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


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
Specifies <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate encoding.

</td>
</tr>
</table>
 


### -param pbEncoded [in]

A pointer to an encoded <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> of <a href="https://msdn.microsoft.com/f650765e-7a72-42a3-baf7-29779fd04adc">CERT_SIGNED_CONTENT_INFO</a> content on which the signature is to be verified.


### -param cbEncoded [in]

The size, in bytes, of the encoded content in <i>pbEncoded</i>.


### -param pPublicKey [in]

A pointer to a 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key to use when verifying the signature.


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
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>  may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -remarks



This function currently calls the 
<a href="https://msdn.microsoft.com/8a84af66-b174-4a3e-b1d7-6f218a52d877">CryptVerifyCertificateSignatureEx</a> function to perform the verification.




## -see-also




<a href="https://msdn.microsoft.com/8a84af66-b174-4a3e-b1d7-6f218a52d877">CryptVerifyCertificateSignatureEx</a>
 

 

