---
UID: NF:wincrypt.CryptDecryptMessage
title: CryptDecryptMessage function
author: windows-sdk-content
description: The CryptDecryptMessage function decodes and decrypts a message.
old-location: security\cryptdecryptmessage.htm
old-project: seccrypto
ms.assetid: e540b816-64e1-4c78-9020-2b221e813acc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptDecryptMessage, CryptDecryptMessage function [Security], _crypto2_cryptdecryptmessage, security.cryptdecryptmessage, wincrypt/CryptDecryptMessage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptDecryptMessage
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptDecryptMessage function


## -description


The <b>CryptDecryptMessage</b> function <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">decodes</a> and <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">decrypts</a> a message.


## -parameters




### -param pDecryptPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/67e136cd-12e3-4a31-9d8b-b53e1129e940">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains decryption parameters.


### -param pbEncryptedBlob [in]

A pointer to a buffer that contains the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encoded</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encrypted</a> message to be decrypted.


### -param cbEncryptedBlob [in]

The size, in bytes, of the encoded and encrypted message.


### -param pbDecrypted [out, optional]

A pointer to a buffer that receives the decrypted message. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. A decrypted message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbDecrypted [in, out, optional]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecrypted</i> parameter. When the function returns, this variable contains the size, in bytes, of the decrypted message copied to <i>pbDecrypted</i>.
						

<div class="alert"><b>Note</b>  When processing the data returned in the <i>pbDecrypted</i> buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified in <i>pcbDecrypted</i> on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the <b>DWORD</b> is updated to the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> that corresponds to the private <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key</a> needed to decrypt the message. To indicate that the function should not return the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> used to decrypt, set this parameter to <b>NULL</b>.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from calls to 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a> and 
<a href="https://msdn.microsoft.com/7c3d2838-6fd1-4f6c-9586-8b94b459a31a">CryptDecrypt</a> might be propagated to this function.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the following error codes most often.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid message and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate encoding types</a>. Currently only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING_TYPE are supported. Invalid <b>cbSize</b> in *<i>pDecryptPara</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enveloped</a> cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The message was encrypted by using an unknown or unsupported algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_DECRYPT_CERT</b></dt>
</dl>
</td>
<td width="60%">
No certificate was found having a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> property to use for decrypting.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



When <b>NULL</b> is passed for <i>pbDecrypted</i>, and <i>pcbDecrypted</i> is not <b>NULL</b>, <b>NULL</b> is returned for the address passed in <i>ppXchgCert</i>; otherwise, a pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> is returned. For a successfully decrypted message, this pointer to a <b>CERT_CONTEXT</b> points to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> used to decrypt the message. It must be freed by calling 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. If the function fails, the value at <i>ppXchgCert</i> is set to <b>NULL</b>.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/b1ad0f13-fb4d-421f-b054-a99c8ad9c83a">Example C Program: Using CryptEncryptMessage and CryptDecryptMessage</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

