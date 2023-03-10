---
UID: NF:wincrypt.CryptSignAndEncryptMessage
title: CryptSignAndEncryptMessage function (wincrypt.h)
description: The CryptSignAndEncryptMessage function creates a hash of the specified content, signs the hash, encrypts the content, hashes the encrypted contents and the signed hash, and then encodes both the encrypted content and the signed hash.
helpviewer_keywords: ["CryptSignAndEncryptMessage","CryptSignAndEncryptMessage function [Security]","_crypto2_cryptsignandencryptmessage","security.cryptsignandencryptmessage","wincrypt/CryptSignAndEncryptMessage"]
old-location: security\cryptsignandencryptmessage.htm
tech.root: security
ms.assetid: 0ab234f2-a681-463f-8ba8-b23b05cf2626
ms.date: 12/05/2018
ms.keywords: CryptSignAndEncryptMessage, CryptSignAndEncryptMessage function [Security], _crypto2_cryptsignandencryptmessage, security.cryptsignandencryptmessage, wincrypt/CryptSignAndEncryptMessage
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
 - CryptSignAndEncryptMessage
 - wincrypt/CryptSignAndEncryptMessage
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
 - CryptSignAndEncryptMessage
---

# CryptSignAndEncryptMessage function


## -description

The <b>CryptSignAndEncryptMessage</b> function creates a <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the specified content, signs the hash, encrypts the content, hashes the encrypted contents and the signed hash, and then encodes both the encrypted content and the signed hash. The result is the same as if the hash were first signed and then encrypted.

## -parameters

### -param pSignPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_sign_message_para">CRYPT_SIGN_MESSAGE_PARA</a> structure that contains the signature parameters.

### -param pEncryptPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encrypt_message_para">CRYPT_ENCRYPT_MESSAGE_PARA</a> structure containing encryption parameters.

### -param cRecipientCert [in]

Number of array elements in <i>rgpRecipientCert</i>.

### -param rgpRecipientCert [in]

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures. Each structure is the certificate of an intended recipients of the message.

### -param pbToBeSignedAndEncrypted [in]

A pointer to a buffer containing the content to be signed and encrypted.

### -param cbToBeSignedAndEncrypted [in]

The size, in bytes, of the <i>pbToBeSignedAndEncrypted</i> buffer.

### -param pbSignedAndEncryptedBlob [out]

A pointer to a buffer to receive the encrypted and encoded message. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbSignedAndEncryptedBlob [in, out]

A pointer to <b>DWORD</b> specifying the size, in bytes, of the buffer pointed to by <i>pbSignedAndEncryptedBlob</i>. When the function returns, this variable contains the size, in bytes, of the signed and encrypted message copied to *<i>pbSignedAndEncryptedBlob</i>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

The following lists the error code most commonly returned by the 
		       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignmessage">CryptSignMessage</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencryptmessage">CryptEncryptMessage</a> might be propagated to this function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignmessage">CryptSignMessage</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>