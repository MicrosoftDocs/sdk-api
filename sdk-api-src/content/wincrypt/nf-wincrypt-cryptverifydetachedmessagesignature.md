---
UID: NF:wincrypt.CryptVerifyDetachedMessageSignature
title: CryptVerifyDetachedMessageSignature function
author: windows-driver-content
description: The CryptVerifyDetachedMessageSignature function verifies a signed message containing a detached signature or signatures.
old-location: security\cryptverifydetachedmessagesignature.htm
old-project: SecCrypto
ms.assetid: d437f6bf-eb56-4d29-bb91-eb8487e50219
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CryptVerifyDetachedMessageSignature, CryptVerifyDetachedMessageSignature function [Security], _crypto2_cryptverifydetachedmessagesignature, security.cryptverifydetachedmessagesignature, wincrypt/CryptVerifyDetachedMessageSignature
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
-	CryptVerifyDetachedMessageSignature
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptVerifyDetachedMessageSignature function


## -description


The <b>CryptVerifyDetachedMessageSignature</b> function verifies a signed message containing a detached signature or signatures.


## -parameters




### -param pVerifyPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure containing the verification parameters.


### -param dwSignerIndex [in]

Index of the signature to be verified. A message might have several signers and this function can be called repeatedly, changing <i>dwSignerIndex</i> to verify other signatures. If the function returns FALSE, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call received the last signer of the message.


### -param pbDetachedSignBlob [in]

A pointer to a BLOB containing the encoded message signatures.


### -param cbDetachedSignBlob [in]

The size, in bytes, of the detached signature.


### -param cToBeSigned [in]

Number of array elements in <i>rgpbToBeSigned</i> and <i>rgcbToBeSigned</i>.


### -param rgpbToBeSigned [in]

Array of pointers to buffers containing the contents to be <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashed</a>.


### -param rgcbToBeSigned [in]

Array of sizes, in bytes, for the content buffers pointed to in <i>rgpbToBeSigned</i>.


### -param ppSignerCert [out, optional]

A pointer to a 
pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of a signer certificate. When you have finished using the certificate context, free it by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function. A pointer to a <b>CERT_CONTEXT</b> structure will not be returned if this parameter is <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (<b>FALSE</b>).

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following lists the error codes most commonly returned by the 
		       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid message and certificate encoding types. Currently only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING_TYPE are supported. Invalid <b>cbSize</b> in *<i>pVerifyPara</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not a signed cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
The message does not have any signers or a signer for the specified <i>dwSignerIndex</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The message was hashed and signed by using an unknown or unsupported algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The message's signature was not verified.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>, 
<a href="https://msdn.microsoft.com/3119eabc-90ff-42c6-b3fa-e8be625f6d1e">CryptVerifySignature</a>, and 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a> might be propagated to this function.<p class="note">If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

