---
UID: NF:wincrypt.CryptSignAndEncryptMessage
title: CryptSignAndEncryptMessage function
author: windows-sdk-content
description: The CryptSignAndEncryptMessage function creates a hash of the specified content, signs the hash, encrypts the content, hashes the encrypted contents and the signed hash, and then encodes both the encrypted content and the signed hash.
old-location: security\cryptsignandencryptmessage.htm
tech.root: seccrypto
ms.assetid: 0ab234f2-a681-463f-8ba8-b23b05cf2626
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CryptSignAndEncryptMessage, CryptSignAndEncryptMessage function [Security], _crypto2_cryptsignandencryptmessage, security.cryptsignandencryptmessage, wincrypt/CryptSignAndEncryptMessage
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
 - CryptSignAndEncryptMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSignAndEncryptMessage function


## -description


The <b>CryptSignAndEncryptMessage</b> function creates a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the specified content, signs the hash, encrypts the content, hashes the encrypted contents and the signed hash, and then encodes both the encrypted content and the signed hash. The result is the same as if the hash were first signed and then encrypted.


## -parameters




### -param pSignPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/1601d860-6054-4650-a033-ea088655b7e4">CRYPT_SIGN_MESSAGE_PARA</a> structure that contains the signature parameters.


### -param pEncryptPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/c683c515-3061-48e3-a64a-2798bd1245b0">CRYPT_ENCRYPT_MESSAGE_PARA</a> structure containing encryption parameters.


### -param cRecipientCert [in]

Number of array elements in <i>rgpRecipientCert</i>.
					


### -param rgpRecipientCert [in]

Array of pointers to 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structures. Each structure is the certificate of an intended recipients of the message.


### -param pbToBeSignedAndEncrypted [in]

A pointer to a buffer containing the content to be signed and encrypted.


### -param cbToBeSignedAndEncrypted [in]

The size, in bytes, of the <i>pbToBeSignedAndEncrypted</i> buffer.


### -param pbSignedAndEncryptedBlob [out]

A pointer to a buffer to receive the encrypted and encoded message. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbSignedAndEncryptedBlob [in, out]

A pointer to <b>DWORD</b> specifying the size, in bytes, of the buffer pointed to by <i>pbSignedAndEncryptedBlob</i>. When the function returns, this variable contains the size, in bytes, of the signed and encrypted message copied to *<i>pbSignedAndEncryptedBlob</i>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

The following lists the error code most commonly returned by the 
		       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

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
If the buffer specified by the <i>pbSignedAndEncryptedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbSignedAndEncryptedBlob</i>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/f14f7c7b-14ac-40a7-9a49-d1a899ecc52a">CryptSignMessage</a> and 
<a href="https://msdn.microsoft.com/927f2e9a-96cf-4744-bd57-420b5034d28d">CryptEncryptMessage</a> might be propagated to this function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/f14f7c7b-14ac-40a7-9a49-d1a899ecc52a">CryptSignMessage</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

