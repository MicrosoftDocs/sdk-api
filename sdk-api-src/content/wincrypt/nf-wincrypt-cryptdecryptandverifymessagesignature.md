---
UID: NF:wincrypt.CryptDecryptAndVerifyMessageSignature
title: CryptDecryptAndVerifyMessageSignature function
author: windows-sdk-content
description: The CryptDecryptAndVerifyMessageSignature function decrypts a message and verifies its signature.
old-location: security\cryptdecryptandverifymessagesignature.htm
tech.root: seccrypto
ms.assetid: 0864a187-617f-4a21-9809-d2dbbc54ab9c
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CryptDecryptAndVerifyMessageSignature, CryptDecryptAndVerifyMessageSignature function [Security], _crypto2_cryptdecryptandverifymessagesignature, security.cryptdecryptandverifymessagesignature, wincrypt/CryptDecryptAndVerifyMessageSignature
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
 - CryptDecryptAndVerifyMessageSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptDecryptAndVerifyMessageSignature function


## -description


The <b>CryptDecryptAndVerifyMessageSignature</b> function decrypts a message and verifies its signature.


## -parameters




### -param pDecryptPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/67e136cd-12e3-4a31-9d8b-b53e1129e940">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains decryption parameters.


### -param pVerifyPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure that contains  verification parameters.


### -param dwSignerIndex [in]

Identifies a particular signer of the message. A message can be signed by more than one signer and this function can be called multiple times changing this parameter to check for several signers. It is set to zero for the first signer. If the function returns <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call received the last signer of the message.


### -param pbEncryptedBlob [in]

A pointer to the signed, encoded, and encrypted message to be decrypted and verified.


### -param cbEncryptedBlob [in]

The size, in bytes, of the encrypted message.


### -param pbDecrypted [out, optional]

A pointer to a buffer to receive the decrypted message. 




This parameter can be <b>NULL</b> if the decrypted message is not required or to set the size of the decrypted message for memory allocation purposes. A decrypted message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbDecrypted [in, out, optional]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecrypted</i> parameter. When the function returns, it contains the size of the decrypted message copied to <i>pbDecrypted</i>. 




<div class="alert"><b>Note</b>  When processing the data returned in the <i>pbDecrypted</i> buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified in <i>pcbDecrypted</i> on input. On output, the variable pointed to by this parameter is set to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> that corresponds to the private <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key</a> needed to decrypt the message.


### -param ppSignerCert [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of the certificate of the signer.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a> and 
<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a> might be propagated to this function.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the following error code most often.

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
If the buffer specified by the <i>pbDecrypted</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbDecrypted</i>.

</td>
</tr>
</table>
 




## -remarks



For a successfully <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">decrypted</a> and verified message, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> pointers pointed to by <i>ppXchgCert</i> and <i>ppSignerCert</i> are updated. They must be freed by calling 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. If the function fails, they are set to <b>NULL</b>.

To indicate that the caller is not interested in the exchange certificate or the signer <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, set the <i>ppXchgCert</i> and <i>ppSignerCert</i> parameters to <b>NULL</b>.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/f2863e4a-d22a-4ff0-91d8-052eeaade14e">Example C Program: Sending and Receiving a Signed and Encrypted Message</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>



<a href="https://msdn.microsoft.com/0ab234f2-a681-463f-8ba8-b23b05cf2626">CryptSignAndEncryptMessage</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

