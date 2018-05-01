---
UID: NF:wincrypt.CryptMsgVerifyCountersignatureEncoded
title: CryptMsgVerifyCountersignatureEncoded function
author: windows-driver-content
description: Verifies a countersignature in terms of the SignerInfo structure (as defined by PKCS #7).
old-location: security\cryptmsgverifycountersignatureencoded.htm
old-project: SecCrypto
ms.assetid: b0332360-a737-4b48-b592-0c55d493a02d
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CryptMsgVerifyCountersignatureEncoded, CryptMsgVerifyCountersignatureEncoded function [Security], _crypto2_cryptmsgverifycountersignatureencoded, security.cryptmsgverifycountersignatureencoded, wincrypt/CryptMsgVerifyCountersignatureEncoded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
-	CryptMsgVerifyCountersignatureEncoded
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMsgVerifyCountersignatureEncoded function


## -description



			The <b>CryptMsgVerifyCountersignatureEncoded</b> function verifies a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">countersignature</a> in terms of the SignerInfo structure (as defined by PKCS #7).


## -parameters




### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b><b>NULL</b> or the handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic provider</a> to use to <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> the encryptedDigest field of <i>pbSignerInfo</i>.This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, pass <b>NULL</b> to cause the default RSA or DSS provider to be used.




### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pbSignerInfo [in]

A pointer to the encoded <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains the signer of the contents of a message to be countersigned.


### -param cbSignerInfo [in]

Count, in bytes, of the encoded BLOB for the signer of the contents.


### -param pbSignerInfoCountersignature [in]

A pointer to the encoded BLOB containing the countersigner information.


### -param cbSignerInfoCountersignature [in]

Count, in bytes, of the encoded BLOB for the countersigner of the message.


### -param pciCountersigner [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> that includes with the issuer and serial number of the countersigner. For more information, see Remarks.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_AUTH_ATTR_MISSING</b></dt>
</dl>
</td>
<td width="60%">
The message does not contain an expected authenticated attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_HASH_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The hash value is not correct.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
</dl>
</td>
<td width="60%">
The cryptographic algorithm is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
</table>
 

Propagated errors from the following functions might be returned.

<ul>
<li>
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3119eabc-90ff-42c6-b3fa-e8be625f6d1e">CryptVerifySignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>
</li>
</ul>
If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



Countersigner verification is done using the PKCS #7 <b>SIGNERINFO</b> structure. The signature must contain the encrypted hash of the encryptedDigest field of <i>pbSignerInfo</i>.

The issuer and serial number of the countersigner must match the countersigner information from <i>pbSignerInfoCountersignature</i>. The only fields referenced from <i>pciCountersigner</i> are SerialNumber, Issuer, and SubjectPublicKeyInfo. The SubjectPublicKeyInfo is used to access the public key that is then used to encrypt the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> from the <i>pciCountersigner</i> so compare it with the hash from the <i>pbSignerInfo</i>.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/12930d4d-2ea5-4d95-b9cf-4f0dd351ce05">Example C Program: Encoding and Decoding a CounterSigned Message</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ebf76664-bca6-462d-b519-2b60f435d8ef">CryptMsgCountersign</a>



<a href="https://msdn.microsoft.com/d9fd734b-e14d-4392-ac88-5565aefbedb4">CryptMsgCountersignEncoded</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

